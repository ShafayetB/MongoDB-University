# Ticket: User Report


**Problem:**

**User Story**

"As an administrator, I want to be able to view the top 20 users by their number of comments."

---

**Task**

For this ticket, you'll be required to modify the **mostActiveCommenters** method in _CommentDao.java_. This method produces a report of the 20 most frequent commenters on the MFlix site.

**Hint**

> This report is meant to be run from the backend by a manager who is very particular about the accuracy of data. Ensure that the read concern used in this read, avoids any potential document rollback.

Remember to add the necessary changes in the pipeline to meet the requirements. More information can be found in the comments of the method.

---

**Testing and Running the Application**

If the application is already running, **stop the application** and run the unit tests for this ticket by executing the following command:

```
mvn test -Dtest=UserReportTest
```

Once the unit tests are passing, run the application with:

```
mvn spring-boot:run
```

Or run the _Application.java_ from your IDE.

Now proceed to the status page to run the full suite of integration tests and get your validation code.

To have the application use the changes that you implemented for this ticket, make sure to **restart the application** after you completed those changes. Also, only refresh the status page to see the new results of the tests, after the application has been restarted.

After passing the relevant tests, what is the validation code for **User Report?**
<details> 
  <summary>Click here for the solution</summary>
   Answer: 5accad3272455e5db79e4dad
</details>

