# DynamoDB MedicationInformation manager for Alexa Development in Final Year Project
- This is a skill that shows use of DynamoDB with Alexa. This skill uses the [Alexa Skills Kit for Node.js]

## What is included in this Alexa Skill
- DynamoDB execution permission to the Lambda.
- Creates a DynamoDB table with name dynamodb-starter and schema, userId as a Partition Key and medicationName as a sort key. 

## What are the main function for this patient medication information skill
- Add Medication to database
- Remove Medication from Database
- Request all of the medication that patient takes
- Request how many of each medication the patient should take a day
- I must: Allow patients to add how many times a day medication should be taken
- I must: Allow patients to remove or modify how many times a day medication should be taken
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