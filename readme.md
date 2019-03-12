# DynamoDB MedicationInformation manager for Alexa Development in Final Year Project
- This is a skill that shows use of DynamoDB with Alexa. This skill uses the [Alexa Skills Kit for Node.js]

## Instructions to execute this template 
- Provides DynamoDB execution permission to the Lambda.
- Creates a DynamoDB table with name dynamodb-starter and schema, userId as a Partition Key and medicationName as a sort key. 

```
{
    AttributeDefinitions: [
        {
            AttributeName: 'userId',
            AttributeType: 'S'
        },
        {
            AttributeName: 'medicationName',
            AttributeType: 'S'
        }
    ],
    KeySchema: [
        {
            AttributeName: 'userId',
            KeyType: 'HASH'
        },
        {
            AttributeName: 'medicationName',
            KeyType: 'RANGE'
        }
    ]
}
```
