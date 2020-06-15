# Quiz

## Describe auditing capabilities

**Problem:**

Which of the following are common reasons organizations enable auditing on MongoDB?

- [x] **To investigate suspecious activity**
- [ ] To increase database performance
- [x] **Accountability**
- [x] **To monitor specific database activities**

## Auditing output format

**Problem:**

Which of the following is/are valid MongoDB audit log top-level fields?

- [x] **result**
- [ ] action
- [ ] timestamp
- [ ] arg
- [ ] privileges
- [x] **local**
- [x] **remote**
- [x] **users**

## Configuring audit from command line

**Problem:**

Which of the following is a valid mongod command line configuration with auditing enabled?

- [x] **mongod --dbpath /data/db --auditDestination syslog**

- [x] **mongod --dbpath /data/db --auditDestination file \
       --auditFormat JSON --auditPath /data/db/auditLog.json**

- [ ] mongod --dbpath /data/db --auditDestination stdout

- [x] **mongod --dbpath /data/db --auditDestination file \
       --auditFormat BSON --auditPath /data/db/auditLog.bson**

## Definition of filters

**Problem:**

Which of the following are categories of operations that MongoDB's auditing system will record by default?

- [x] **Authentication & Authorization**
- [ ] CRUD Operations (DML)
- [x] **Schema (DDL)**
- [x] **Replica Set and Sharded Cluster**

## DDL operations definition

**Problem:**

Which of the following are DDL action types supported by MongoDB's auditing system?

- [ ] shutdown
- [ ] createDocument
- [x] **createIndex**
- [x] **dropCollection**
- [x] **createDatabase**

## Example of DDL audit filter

**Problem:**

Which of the following audit filters will allow us to monitor the creation of collections on databases that begin with "university"?

- [x] **{ atype: "createCollection", "param.ns": /^university.*/ }**
- [x] **{ atype: "createCollection", "param.ns": /^university/ }**
- [ ] { atype: "createCollection", "param.ns": /university.*/ }
- [ ] { atype: "createCollection", "param.ns": /university/ }

## DML operations definition

**Problem:**

Which action type is used by CRUD operations in MongoDB?

- **authCheck**
- authenticate
- CRUD
- DML

## Enabling auditAuthorizationSuccess

**Problem:**

What server parameter is used to enable the auditing of CRUD operations?

- auditDMLOperations
- **auditAuthorizationSuccess**
- auditAuthenticationSuccess
- auditCRUDOperations

## Log Redaction Introduction

**Problem:**

Why do we need to redact client data in the MongoDB log files?

- [ ] To ensure that we filter unusable debugging information from the logs
- [ ] To enforce profiling data to be accessible to users
- [x] **To prevent sensitive data from being written to system logs**
- [x] **Because system log data is not encrypted**

## Log Redaction Setup

**Problem:**

In the case of a replica set or shard cluster we need to:

- [ ] Running command db.adminCommand({setParameter:1, clientLogRedaction: 2}) forces all members of a cluster to redact their log client data.
- [x] **Setting the system flag security.redactClientLogData, in MongoDB configuration file, is the recommended setup guarantee that on reboot log redaction will be enabled.**
- [ ] Users can bypass log redaction by emitting write concern flag {r:0} in their write operations
- [x] **Enable log redaction on all data holding members and mongos elements**

## Security Checklists

**Problem:**

Which of the following are security checklist topics outlined in the lesson video?

- [x] **Encrypt and Protect Data**
- [x] **Run MongoDB with a Dedicated User**
- [x] **Enable Access Control and Enforce Authentication**
- [x] **Limit Network Exposure**
- [x] **Encrypt Communication**

## Security Reports

**Problem:**

What is the recommended communication method to report a vulnerability to MongoDB?

- Send a fax to MongoDB's NYC HQ
- **Submit a ticket in the SECURITY project on the MongoDB JIRA**
- Mail a letter to MongoDB's Palo Alto Office
- Send an email to security@mongodb.com
