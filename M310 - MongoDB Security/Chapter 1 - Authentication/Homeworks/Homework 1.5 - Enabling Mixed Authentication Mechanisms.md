# Homework 1.5: Enabling Mixed Authentication Mechanisms

**Problem:**

In this lab you're going to start your own replica set with a mix of SCRAM-SHA-1, X.509, and keyfile based authentication enabled.

We've provided you with the necessary certificates via the handout.

Your task is to create a three member replica set that uses X.509 certificates and SCRAM-SHA-1 for client authentication. You'll then use keyfile authentication for internal authentication. Below are the settings you should use for your replica set. Failure to comply with these parameters will result in incorrect results.

<table border="1" class="docutils">
<colgroup>
<col width="12%">
<col width="29%">
<col width="29%">
<col width="29%">
</colgroup>
<thead valign="bottom">
<tr><th class="head">Type</th>
<th class="head">Primary</th>
<th class="head">Secondary</th>
<th class="head">Secondary</th>
</tr>
</thead>
<tbody valign="top">
<tr><td>Port</td>
<td>31150</td>
<td>31151</td>
<td>31152</td>
</tr>
<tr><td>DBPath</td>
<td>~/M310-HW-1.5/r0</td>
<td>~/M310-HW-1.5/r1</td>
<td>~/M310-HW-1.5/r2</td>
</tr>
<tr><td>LogPath</td>
<td>~/M310-HW-1.5/r0/mongodb.log</td>
<td>~/M310-HW-1.5/r1/mongodb.log</td>
<td>~/M310-HW-1.5/r2/mongodb.log</td>
</tr>
</tbody>
</table>

Make sure to copy the certs folder directly to the m310-vagrant-env/shared folder. If the certificates are not in this location then your results will be incorrect. When SSHed into the database VM your home file structure should look similar to this:

```
~
`-- shared
    |-- certs
    |   |-- ca.pem
    |   |-- client.pem
    |   `-- server.pem
    `-- validate-hw-1.5.sh
```

After you have set up your replica set with all the mechanisms enabled then create a SCRAM-SHA-1 user named will with a password of $uperAdmin with the root role on the admin database.

After creating an account for Will then create another account for the client.pem certificate. Give this user the userAdminAnyDatabase role on the admin database.

After creating both users run the following validation script and copy the output into the submission area below.

```
$ cd ~/shared
$ ./validate-hw-1.5.sh
```

Note: If you've successfully enabled authentication on the replica set, then the validation script should output a JSON object with three keys: unauthorizedStatus, memberStatuses, and users. The first key confirms that authentication is enabled, the second verifies that all members are still up and running, and the last one validates the users you were supposed to create.


<details>
  <summary>Click here for the solution</summary>
    Answer: { unauthorizedStatus: { "ok" : 0, "errmsg" : "not authorized on admin to execute command { replSetGetStatus: 1.0 }", "code" : 13 }, memberStatuses: ["PRIMARY","SECONDARY","SECONDARY"], users: [{"_id":"admin.will","roles":[{"role":"root","db":"admin"}]},{"_id":"$external.C=US,ST=New York,L=New York City,O=MongoDB,OU=University2,CN=M310 Client","roles":[{"role":"userAdminAnyDatabase","db":"admin"}]}] }
</details>



