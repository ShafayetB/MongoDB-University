# Quiz

## Cursor Methods and Aggregation Equivalents

Which of the following aggregation stages have equivalent cursor methods?



- [x] **$skip**
- [ ] $out
- [x] **$sort**
- [ ] $sortByCount
- [x] **$limit**

## Basic Writes

Which of the following is true about InsertOneResult?



- [ ] It is a cursor.
- [x] **It contains the _id of an inserted document.**
- [x] **It can tell us whether the operation was acknowledged by the server.**
- [ ] It contains a copy of the inserted document.

## Write Concerns

Which of the following Write Concerns are valid in a 3-node replica set?



- [x] **w: 0**
- [x] **w: 1**
- [ ] w: 4
- [ ] w: 5
- [x] **w: majority**

## Basic Updates

Which of the following are valid update operators in Pymongo?



- [x] **$push**
- [ ] $remove
- [x] **$set**
- [ ] $update
- [x] **$inc**

## Basic Joins

Why did we use a let expression with expressive $lookup, when joining the comments and the movies collection?



- To store the output of the pipeline in the movie_comments field.
- **To use fields from the movies documents in the pipeline.**
- To use fields from the comments documents in the pipeline.
- To count the number of comments documents.

## Basic Deletes

Which of the following is true about deleting documents in Pymongo?



- [x] **delete_many() can delete any number of documents.**
- [ ] Pymongo can only delete one document at a time.
- [x] **DeleteResult objects contain the number of deleted documents.**
- [ ] delete_one() will not return a DeleteResult object.
- [x] **delete_one() can only delete one document.**
