# Chat-app
Working on it.

Using this is a log for now.

1. completed basic structuring for backend and created react app with vite. and connect to mongoDB was successfull.

2. Basic Back-end structure is done and used cloudinary api and setup its api-key and api-secret to use image uploading and be able to upload images. Otherwise just made the models,routes and controllers till auth and messages, we also made middleware protectRoute which we can put before using anything to make sure we are secure. Also made the models are basically where we define a mongoose Schema which is basically the way in which we will be storing the data on the mongoDB server, we need to do this because mongoDB is a noSQL data structure so we need to define the Schema ourselves. also made the auth routes and message routes files they basically are the API end-points for what we want to do and the functions which actually do the work which we use in these route files by name only as they are defined somewhere else, those functions are defined in what is called a controller file I have made two controller files so far one for auth api-points and one for message-api points.

So to keep it simple -> 

models -> Mongoose Schema because mongoDB is a noSQL database.
Routes -> Cluster where we store all the sub API points of this -> two API main points so far are /auth and /messages -> auth handles signup,login,updateProfile, logout, check -> message handles getMessage,sendMessage,getUsersForSideBar.

and where these end-points are handled are controllers namely -> auth.controller.js and the maessage.controller.js

Also the files in backend/lib so far are used for -> connecting to mongoose for storing and retreiving data
                                                  -> connecting to cloudinary for storing and retreiving images
                                                  -> generating jwt token by using jsonwebtoken and it is being used to confirm if our current session is valid or not and it is signed with a secret_key which is being stored in the .env file ans can be used to verify the authenticity of our data later on. In fact we are verifying it in the protectRoute (auth.middleware.js) it ensures that we are not getting dupped by a similar kind of token.
