# UpperCampus ECS Deployment preparation action
GitHub Action to perform preparations for deployments of UpperCampus ECS services.

This action generates a couple of outputs that are necessary for the use of [the AWS ECS deployment action](https://github.com/aws-actions/amazon-ecs-deploy-task-definition). It also generates two task definition files for use with the ecs action, already pre-filled with the correct image that has been passed as input to this action.

## inputs

| Name                          | Description                                                      | Required  | Default                   |
| ----------------------------- |:---------------------------------------------------------------- |:--------- |:--------------------------|
| short-service                 | Short name of the service used as search string for AWS outputs. | true      |-                          |
| image                         | Docker image to put into the task definition files.              | true      |-                          |
| stg-ecs-task-definition-file  | Staging ECS Task definition family filename.                     | false     | task-definition-stg.json  |
| prd-ecs-task-definition-file  | Production ECS Task definition family filename.                  | false     | task-definition-prd.json  |


## outputs


| Name                            | Description                                                      |
| :------------------------------ |:---------------------------------------------------------------- |
| stg-ecs-cluster                 | Staging ECS Cluster Name. |
| prd-ecs-cluster                 | Production ECS Cluster Name.              |
| stg-ecs-service                 | Staging ECS Service Name. |
| prd-ecs-service                 | Production ECS Service Name.              |
| stg-ecs-task-definition-family  | Staging ECS Task definition family name.                     |
| prd-ecs-task-definition-family  | Production ECS Task definition family name.                  |
| stg-ecs-task-definition-file    | Staging ECS Task definition family filename.                     |
| prd-ecs-task-definition-file    | Production ECS Task definition family filename.                  |



