# Ticket: Get Comments


**Problem:**

**User Story**

"As a user, I want to be able to view comments for a movie when I look at the movie detail page."

---

**Task**

For this ticket, you'll be required to extend the **getMovie** method in _MovieDao.java_ so that it also fetches the comments for a given movie. The comments should be returned in order from most recent to least recent using the _date_ key.

Movie comments are stored in the _comments_ collection, so this task can be accomplished by performing a _$lookup_. Refer to the Aggregation Quick Reference for the specific syntax.

---

**MFlix Functionality**

Once this ticket is completed, each movie's comments will be displayed on that movie's detail page.

---

**Testing and Running the Application**

If the application is already running, **stop the application** and run the unit tests for this ticket by executing the following command:

```
mvn test -Dtest=GetCommentsTest
```

Once the unit tests are passing, run the application with:

```
mvn spring-boot:run
```

Or run the _Application.java_ from your IDE.

Now proceed to the status page to run the full suite of integration tests and get your validation code.

To have the application use the changes that you implemented for this ticket, make sure to **restart the application** after you completed those changes. Also, only refresh the status page to see the new results of the tests, after the application has been restarted.

After passing the relevant tests, what is the validation code for **Get Comments?**
<details> 
  <summary>Click here for the solution</summary>
   Answer: 5ab5094fb526e43b570e4633
</details>



