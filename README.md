# serverless-lambda

This is a simple serverless application I built as project 4 for IDS 721 course.

### Basic workflow
![image](https://user-images.githubusercontent.com/61301108/114272661-96e7dd00-9a49-11eb-9df4-9302c2d9d776.png)

### Steps to build the project:

1. run `sam init` to create initial template of the lambda function
2. write the code in file `app.py`
3. run `sam build` to build the function
4. run `sam deploy --guided` for the fisrt deploy
5. set triggers for the two lambda functions
6. if the code changed, run
    ```
    sam build
    sam deploy
    ```
    to deploy the change 


### Sidework needed:
- build a ECR, which would be used in step 4
- build a SQS queue and match the name in the producer function
- build a S3 bucket and match the name in the consumer function
- build a DynamoDB table and match the name in the producer function

### Caveats&Potential Bug
- don't forget to change the requirements file
- don't forget to add permission to the lambda functions
- don't make mistakes when creating the primary key, for the key name cannot be changed once created!
