# Setting up MongoDb

This is a guide for setting up a free cloud Deployment of mongoDB using mlab. It can be used with your web-app while it is deployed on any cloud platform including the IBM Bluemix Platform.

## Set up an mLab account

1. Create an account on [mlab](https://mlab.com/).
2. Verify the account using the link sent to your email id.
3. Create a new MongoDB Deployment using the Create new button under the MongoDB Deployments.
4. You can choose any cloud provider, (although I have used AWS only, you can use that too to be on a safer side).
5. Choose the Sandbox Plan type.
6. Choose the server closest to you.
7. Give the database a name and submit the order.
8. Navigate to the page of the database you just created.
9. Add a new user under the users tab. You can use any username and password. I suggest that it should be different from your account credentials as your whole team would be using it.
10. Get the standard MongoDB URI. It should look something like -
  `mongodb://<dbuser>:<dbpassword>@ds012345.mlab.com:56789/mydb`
11. Replace your database user's credentials in place of <dbuser> and <dbpassword>.

Now, you can use this link to connect to the cloud database just as you do with a local instance of mongoDB server.

For eg.
With Node.js, if you use mongoose, you can use it like this -

```javascript
mongoose.connect('mongodb://<dbuser>:<dbpassword>@ds012345.mlab.com:56789/mydb');
```

For any kind of queries, you can raise an issue in this repository.
