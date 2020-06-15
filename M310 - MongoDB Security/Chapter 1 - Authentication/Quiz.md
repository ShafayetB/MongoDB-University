# Quiz

## Welcome to MongoDB Security

**Problem:**

Which topic(s) are we going to cover in this course?

- [ ] Aggregation
- [x] **Encryption**
- [x] **Auditing**
- [x] **Authorization**
- [ ] CRUD

## Authentication vs. Authorization

**Problem:**

Authentication is ...

- [ ] How we know what a user can do on a system.
- [x] **How we know who a user is on a system.**

## Authentication Mechanisms Overview

**Problem:**

Which authentication mechanism(s) is/are supported by MongoDB?

- [ ] LTPA
- [x] **Kerberos**
- [ ] RSA tokens
- [x] **SCRAM-SHA-1**
- [x] **LDAP**

## Authentication Mechanisms

**Problem:**

Which of the following statements is/are true in relation to authentication?

- [ ] Kerberos is an authentication and authorization protocol.
- [x] **X.509 can be used to authenticate members of a sharded cluster.**
- [ ] SCRAM-SHA-1 is a certificate-based authentication mechanism.
- [x] **MONGODB-CR is deprecated as of MongoDB 3.0.**
- [ ] A copy of a user's LDAP credentials are stored in MongoDB.

## The Localhost Exception

**Problem:**

Which of the following statements is/are false concerning the localhost exception?

- [x] **The localhost exception allows you to create one user per database.**
- [ ] The localhost exception is only applicable when connected to MongoDB via the localhost network interface.
- [x] **The localhost exception allows you to run show dbs.**

## Authentication Methods

**Problem:**

Which of these authentication methods will fail if a server is started with the following options?

```
$ mongod --auth
$ mongo
use admin
db.createUser({user: 'kirby', pwd: 'password', roles: ['root']})
```

- ```
    $ mongo -u kirby -p password
    ```
- ```
    $ mongo admin -u kirby -p password
    ```
- ```
    $ mongo 
    db.auth('kirby', 'password')
  ```
-  ```
    $ mongo
    use admin
    db.auth('kirby', 'password')
    ```
<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>$ mongo -u kirby -p password</li>
      <li>$ mongo
      db.auth('kirby', 'password')
      </li>
    </ul>
</details>


## Authentication on Sharded Clusters

**Problem:**

Authentication on a sharded cluster is achieved by...

- [ ] passing a --auth option to mongos
- [ ] passing a --auth option to each mongod
- [ ] passing a --auth option to each mongod and to mongos
- [x] **enabling internal authentication between members using keyfiles**
- [x] **enabling internal authentication between members using X.509 certificates**

## Enabling SCRAM-SHA-1

**Problem:**

SCRAM-SHA-1 is the default password authentication mechanism on MongoDB.

- **True.**
- False.

## Enabling X.509

**Problem:**

How does the mongod know the identity of the client?

- [x] **It obtains a certificate from the client when the TLS connection is established.**
- [x] **The certificate must be signed by the certificate authority file passed to the mongod.**
- [x] **The subject of the certificate must match the name of the user in the $external database.**

## Enabling LDAP

**Problem:**

Which of the following is/are true regarding LDAP authentication?

- [x] **MongoDB drivers authenticating to MongoDB with LDAP send LDAP credentials using SASL PLAIN which sends the username/password in clear text.**
- [x] **LDAP Authentication support is a MongoDB Enterprise only feature.**
- [ ] LDAP is more secure than Kerberos
- [x] **saslauthd is a proxy service used by mongod to talk to a LDAP server**

## LDAP Authorization Introduction

**Problem:**

With MongoDB 3.4 we are further strengthening the MongoDB security features by enabling:

- Kerberos authentication
- X509 certificates authorization
- **LDAP authorization**
- LDAP authentication

## LDAP Authorization Steps

**Problem:**

Which of the following is not an LDAP authorization step:

- Transform user credentials
- **Validate the mongod for authorized hostname and port**
- Provide user credentials to authorization server
- Validate user credentials for authentication purposes
- Query the LDAP server to validate user credentials

## LDAP Authorization User Transformations

**Problem:**

In order to match the credential formats between the authentication and authorization mechanisms, the user credentials may require a transformation step. This transformation is defined by the following format:

- **String value defining a JSON array of regular expression / substitution pairs**
- String enclosing a regular expression and optional substitution string
- JSON object defining an array of regular expressions / substitution pairs
- One regular expression / substitution pair

## LDAP Authorization Configuration Options

**Problem:**

Consider the following MongoDB configuration file snippet:

```
//...
security:
  ldap:
    servers: 'ldap.mongodb.university'
    authz:
      queryTemplate: '{USER}?memberOf?base'
    transportSecurity: 'tls'
    bind:
      method: 'simple'
    userToDNMapping: '[{match: "(.+)", substitution: "uid={0},ou=Users,dc=mongodb,dc=com"}]'
  authenticationMechanisms: 'GSSAPI'
  //...
```

Check all statements that are valid, given the above configuration:

- [ ] No transport security has been enabled between MongoDB and the authorization server
- [x] **LDAP authorization is enabled**
- [ ] MongoDB will be binding the operating system users for LDAP integration
- [ ] The configured LDAP server is running on secured.mongodb.com
- [x] **MongoDB will be using Kerberos for authentication purposes**

## MongoLDAP

**Problem:**

mongoldap enables us to validate:

- [ ] Validate LDIF files
- [ ] LDAP server TLS configuration
- [x] **Validate LDAP authorization individual configuration options**
- [x] **LDAP authorization options given a MongoDB configuration file**
- [ ] LDAP server user groups hierarchy

## LDAP Authorization Setup

**Problem:**

To enable the integration of LDAP for authorization purposes in MongoDB, we had to modify the localhost exception.

In what does this modification consists off?

- Allow the creation of more than one user
- **Extended the locahost host exception to allow the creation of a role**
- Allow user defined roles to inherit built-in roles
- Remove the locahost exception of MongoDB is configured for LDAP authorization

## Enabling Kerberos

**Problem:**

Which of the following statements is/are true?

- [x] **Kerberos and MongoDB have mutual trust through a shared key.**
- [x] **Kerberos principals are case-sensitive.**
- [x] **MongoDB uses the GSSAPI authentication mechanism for - Kerberos authentication.**
- [x] **Kerberos Authentication support is a MongoDB Enterprise only feature.**

## Enabling Internal Authentication

**Problem:**

Which of the following security mechanisms is/are supported by internal authentication with MongoDB?

- [ ] MONGODB-CR
- [x] **X.509**
- [ ] LDAP
- [ ] Kerberos
- [x] **Keyfile**

## Enabling Internal X.509 Authentication

**Problem:**

What is the option passed to mongod (including argument) to specify that X.509 certificates will be used for internal cluster authentication?

<details>
  <summary>Click here for the solution</summary>
    Answer: --clusterAuthMode x509
</details>


## Migrating MONGODB-CR to SCRAM-SHA-1

**Problem:**

Which of the following statements are true with respect to changing authentication mechanisms from MONGODB-CR to SCRAM-SHA-1?

- [x] **Updating drivers might be required.**
- [x] **MONGODB-CR will be disabled after the migration.**
- [x] **SCRAM-SHA-1 is more secure that MONGODB-CR.**
- [x] **On 3.0 before importing 2.6 user data new users are created with SCRAM-SHA-1.**
