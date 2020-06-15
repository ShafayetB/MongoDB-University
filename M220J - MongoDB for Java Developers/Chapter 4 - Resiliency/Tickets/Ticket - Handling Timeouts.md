# Ticket: Handling Timeouts


**Problem:**

**Task**

For this ticket, you'll be required to modify the connection information for **MongoClient** to set a write concern timeout of **2500** milliseconds.

The **MongoClient** in **mflix.config.MongoDBConfiguration** is initialized in the **mongoClient** bean method. There are a few other details in the Mongo Client section of the Java Driver documentation for your reference.

Aside from the write concern timeout, you are also tasked to set the **connectTimeoutMS** configuration option to **2000** milliseconds. This option should be set in the connection string. Check MongoDB URI options reference for more information.

The unit test **TimeoutsTest.java** will be asserting that these two configuration options are correctly set.

---

**Testing and Running the Application**

If the application is already running, **stop the application** and run the unit tests for this ticket by executing the following command:

```
mvn test -Dtest=TimeoutsTest
```

Once the unit tests are passing, run the application with:

```
mvn spring-boot:run
```

Or deploy the application from your IDE.

Now proceed to the status page to run the full suite of integration tests and get your validation code.

To have the application use the changes that you implemented for this ticket, make sure to **restart the application** after you completed those changes. Also, only refresh the status page to see the new results of the tests, after the application has been restarted.

After passing the relevant tests, what is the validation code for **Timeouts?**
<details> 
  <summary>Click here for the solution</summary>
   Answer: 5addf035498efdeb55e90b01
</details>

