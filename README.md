npm install express mongoose body-parser cors jsonwebtoken bcryptjs --save

###
– import express, body-parser and cors modules:

Express is for building the Rest apis
body-parser helps to parse the request and create the req.body object
cors provides Express middleware to enable CORS
– create an Express app, then add body-parser and cors middlewares using app.use() method. 

###
These Mongoose Models represents users & roles collections in MongoDB database.
User object will have a roles array that contains ids in roles collection as reference.

This kind is called Reference Data Models or Normalization.

###
After initializing Mongoose, we don’t need to write CRUD functions because Mongoose supports all of them:

create a new User: object.save()
find a User by id: User.findById(id)
find User by email: User.findOne({ email: … })
find User by username: User.findOne({ username: … })
find all Roles which name in given roles array: Role.find({ name: { $in: roles } })
These functions will be used in our Controllers and Middlewares.

###