# Quiz

## Welcome!

**Problem:**

What resources are available to help you complete this course?

- **An in-class discussion forum where you can ask questions and help your fellow learners**
- **Teaching assistants to field questions and provide guidance on the course**
- Instructor's email address

## Connecting to Our Class Atlas Cluster from the mongo Shell

**Problem:**

When connecting to an Atlas cluster using the shell, why do we provide the hostnames for all nodes when we launch mongo? Choose the best answer from the choices below.
- Because our authentication credentials are not stored on the primary, but on other nodes in our cluster.
- There really isn't a good reason
- To make it possible for all the nodes to communicate with each other
- **So that if the primary node goes down, the shell can connect to other nodes in the cluster instead**
- So that other nodes in the cluster can contact our client, if necessary

## Grading and Logistics

**Problem:**

Which of the following count toward your final grade?

- Quizzes
- **Labs (also called homework)**
- **Final exam**

## Understanding JSON

**Problem:**

According to the JSON spec, which of the following data types are directly supported by JSON?

- **String**
- **Array**
- **Object**
- **Boolean values (true and false)**
- **Floating-point number**
- **Null**
- Pointer
- Date
- Graph
- **Decimal number**

## Databases, Collections, and Documents

**Problem:**

Which of the following statements are true? Check all that apply.

- **Documents are stored in collections.**
- **A database may contain one or more collections.**
- **Each database and collection combination define a namespace.**
- We reference a namespace using the name of the database, followed by a comma, followed by the name of the collection, e.g., city,neighborhoods.
- **We won't talk about indexes too much in the course, but you can learn about indexes in M201: MongoDB Performance.**

## Documents: Scalar Value Types

**Problem:**

Based on the field depicted below, which of the following are true?

![](https://s3.amazonaws.com/edu-static.mongodb.com/lessons/M001/scalar_values_video_year_field.png)

- **Not all documents in this collection have the same value type for this field.**
- **Most of the documents in this collection contain int32 values for this field.**
- Some documents in this field have the value type Year

## MongoDB Documents: Geospatial Data

**Problem:**

Which of the following are types of data Compass (and MongoDB) recognizes and specifically supports?

- **documents**
- **arrays**
- **geospatial data**
- rainfall
- air pressure

## Filtering Collections with Queries

**Problem:**

Which of statements below best describes the following filter?

```
{"age": {"$gte": 21, "$lt": 70}}
```

- Find all documents for which the age field has a value that is >= 21 and <= 70.
- Find all documents for which the age field has a value that is either equal to 21 or equal to 70.
- **Find all documents for which the age field has a value that is >= 21 and < 70.**
- Find all documents for which the age field is < 70.
- None of the above.

