// Cloudformation-template

//Creating a DynamoDB table YAML 

AWSTemplateFormatVersion: '2010-09-09'
Description: Create a DynamoDB table

Resources:
  MyDynamoDBTable:
    Type: AWS::DynamoDB::Table
    Properties:
      TableName: MyTable
      AttributeDefinitions:
        - AttributeName: MyPartitionKey
          AttributeType: S
      KeySchema:
        - AttributeName: MyPartitionKey
          KeyType: HASH
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 5

        