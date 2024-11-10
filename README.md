# Databricks Settings AWS

This repository contains two files that allow to delete and create the NAT Gateway and Elastic IP of the associated Databricks workspace. These two ressources run 24/7 even if you stop the cluster in Databricks and generate costs. Therefore deleting them, when not using Databricks, will save those costs (1-2 USD per day).

The only information required is the following and must be added at the bottom of each script:

```
profile_name = "default"            # Replace with your AWS profile name
workspace_id = "4261785485859745"   # Replace with your Databricks workspace ID
region_name = "eu-west-1"           # Specify the AWS region
```

The databricks `workspace_id` can be found under VPCs in AWS Console and has the following format after its creation:

```
databricks-WorkerEnvId(workerenv-4261785485859745-d7fce5d2-3e6f-4673-9e7f-3155f9c7796f)
```
