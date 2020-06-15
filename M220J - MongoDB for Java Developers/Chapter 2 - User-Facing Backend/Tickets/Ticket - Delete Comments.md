# Ticket: Delete Comments


**Problem:**

**User Story**

"As a user, I want to be able to delete my own comments."

---

**Task**

For this ticket, you'll be required to modify the **deleteComment** method in _CommentDao.java_. Ensure the delete operation is limited so only the user can delete their own comments, but not anyone else's comments.

---

**MFlix Functionality**

Once this ticket is completed, users will be able to delete their own comments, but they won't be able to delete anyone else's comments.

---

**Testing and Running the Application**

If the application is already running, **stop the application** and run the unit tests for this ticket by executing the following command:

```
mvn test -Dtest=DeleteCommentTest
```

Once the unit tests are passing, run the application with:

```
mvn spring-boot:run
```

Or run the _Application.java_ from your IDE.

Now proceed to the status page to run the full suite of integration tests and get your validation code.

To have the application use the changes that you implemented for this ticket, make sure to **restart the application** after you completed those changes. Also, only refresh the status page to see the new results of the tests, after the application has been restarted.

After passing the relevant tests, what is the validation code for **Delete Comments?**
<details> 
  <summary>Click here for the solution</summary>
   Answer: 5ac25c280a80ed6e67e1cecb
</details>

