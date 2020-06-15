# Ticket: Durable Writes


For this ticket, you'll be required to increase the durability of the addUser method in UsersDAO.js from the default Write Concern of w: 1.

When a new user registers for MFlix, their information must be added to the database before they can do anything else. For this reason, we want to make sure that the data written by the addUser method will not be rolled back.

We can decrease the chances of a rollback by increasing the write durability of the addUser method.

Which of the following Write Concerns is more durable than the default?

- [x] **WriteConcern.MAJORITY**
- [ ] WriteConcern.UNACKNOWLEDGED
- [ ] WriteConcern.W1
- [x] **WriteConcern.W2**
