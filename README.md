## Amazon ECS "Deploy Task Definition" Action for GitHub Actions
forked from [aws-actions/amazon-ecs-deploy-task-definition](https://github.com/aws-actions/amazon-ecs-deploy-task-definition)


### WTF?
This action performs exactly the same tasks as the original, with one important modification:
You can directly pass an ARN into the task-definition input.

This is particularly useful when you manage/create your task definition using Terraform, CDK, the Serverless framework, or even CloudFormation itself.

Usage Example:
```yaml
    - name: Deploy to Amazon ECS
      uses: miltonhit/amazon-ecs-deploy-task-definition@V2.0.3
      with:
        task-definition: arn:aws:ecs:<region>:<aws_account_id>:task-definition/<task_definition_name>:<revision_number>
        service: my-service
        cluster: my-cluster
        wait-for-service-stability: true
```

I've opened a [PR on original repository](https://github.com/aws-actions/amazon-ecs-deploy-task-definition/pull/524). However, this has not been merged yet.

Enjoy :blush: