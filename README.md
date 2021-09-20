# MongoDB.Activities
Are you trying to integrate your MongoDB directly with your Automation processes?  This Custom Activities package allows you to directly interact with your MongoDB. You can perform various operations like Connect, GetCollection, Find, InsertOne (InsertOne and InsertOneAsync), DeleteMany (DeleteMany and DeleteManyAsync). 

## Please Go Through the InstallationGuide.docx .

### Overview

The component includes the following 5 Custom Activities to interact with MONGO DB:

1. Connect To Mongo:
Inputs:
    a. ConnectionString - Of type String
    b. DatabaseName - Of type String
Output:
   a. Database - Of type MongoDB.Driver.MongoDatabaseBase

2. Get Mongo Collection:
Inputs:
   a. CollectionName - Of type String
   b. DataBase - Of type MongoDB.Driver.MongoDatabaseBase
Output:
   a. Collection - Of type MongoDB.Driver.IMongoCollection<MongoDB.Bson.BsonDocument>

3 . Find Activity:
Inputs:
   a. Collection - Of type MongoDB.Driver.IMongoCollection<MongoDB.Bson.BsonDocument>
   b. FilterQuery - Of type MongoDB.Bson.BsonDocument
output:
   a. FindResult - Of type Systems.Collections.Generic.List<MongoDB.Bson.BsonDocument>

4. Inser One Activity:
Inputs:
   a. Collection - Of type MongoDB.Driver.IMongoCollection<MongoDB.Bson.BsonDocument>
   b. InsertElement - Of type MongoDB.Bson.BsonDocument
   c. InsertOneType - Select the type of required InsertOne command from the dropdown - InsertOne or InsertOneAsync 

5. Delete Many Activity:
Inputs:
   a. Collection - Of type MongoDB.Driver.IMongoCollection<MongoDB.Bson.BsonDocument>
   b. FilterQuery - Of type MongoDB.Bson.BsonDocument
   c. DeleteManyType - Select the type of required DeleteMany command from the dropdown - DeleteMany or DeleteManyAsync 
outputs:
output must be used as per the DeleteMany command type. 
   a. DeleteResult - Of type MongoDB.Driver.DeleteResult
   b. DeleteResultAsync - Of type System.Threading.Tasks.Task<MongoDB.Driver.DeleteResult>


Dependencies on MongoDB.Driver - In the Manage Packages (in UiPath Studio) - Search and install - MongoDB.Driver by author - MongoDB Inc. 
#### Package is also published at UiPath Marketplace - https://marketplace.uipath.com/listings/uipath-mongo-activities
