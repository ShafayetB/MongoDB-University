# Lab (Ungraded): Import Dataset

Note: There should be a section of the README.rst titled "Importing Data". If you imported data into Atlas during the README lesson, you can skip this lesson. If you used Load Sample Dataset, you can also skip this step.

Now that your Atlas cluster is configured correctly, let's populate it with some data. All the data required for MFlix is contained in the data directory in the handout.

The mongorestore command necessary to import the data is located below. Copy the command and use the Atlas SRV string to import the data (including username and password credentials).

You can retrieve this SRV string from the Atlas website:

Click Connect:

![](https://s3.amazonaws.com/university-courses/m220/atlas_connect.png)

Then click Connect Your Application:

![](https://s3.amazonaws.com/university-courses/m220/atlas_connect_application.png)

Then copy the SRV string to your clipboard:

![](https://s3.amazonaws.com/university-courses/m220/atlas_copy_uri.png)

Remember to replace <password> with your own password!

Once you have the SRV string, pass it to the --uri parameter:

```
mongorestore --drop --gzip --uri mongodb+srv://m220student:m220password@<YOUR_CLUSTER_URI> data
```

A few tips when running mongorestore:

- The --username and --password flags cannot be used with and SRV string. Instead, the username and password should be included in the SRV string (i.e. mongodb+srv://m220student:m220password@<your-cluster-address>)
- In order to work properly, this command must be run from the top-level of the mflix-<language>/ directory, where <language> is your chosen programming language.

You can verify that the data was imported by connecting to Atlas from the mongo shell:

```
mongo mongodb+srv://m220student:m220password@<YOUR_CLUSTER_URI>
```
