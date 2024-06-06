## About the connector
Google Compute Engine's tooling and workflow supports to create advanced networks on the regional levels and load balancing capabilities in cloud computing. This connector facilitates automated operation related to GCE operations.
<p>This document provides information about the Google Cloud Compute Connector, which facilitates automated interactions, with a Google Cloud Compute server using FortiSOAR&trade; playbooks. Add the Google Cloud Compute Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Google Cloud Compute.</p>
### Version information

Connector Version: 1.2.0


Authored By: Fortinet

Certified: No
## Release Notes for version 1.2.0
Following enhancements have been made to the Google Cloud Compute Connector in version 1.2.0:
<ul>
<li><p>Added the following new operations and playbooks:</p>

<ul>
<li>Disk Snapshot</li>
</ul></li>
</ul>
## Installing the connector
<p>Use the <strong>Content Hub</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.</p><p>You can also use the <code>yum</code> command as a root user to install the connector:</p>
<pre>yum install cyops-connector-google-cloud-compute</pre>

## Prerequisites to configuring the connector
- You must have the credentials of Google Cloud Compute server to which you will connect and perform automated operations.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Google Cloud Compute server.

## Minimum Permissions Required
- Not applicable

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Google Cloud Compute</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations</strong> tab enter the required configuration details:</p>
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Upload Service Account JSON File</td><td>The service account private key file.
</td>
</tr></tbody></table>
## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function</th><th>Description</th><th>Annotation and Category</th></tr></thead><tbody><tr><td>List Instances within Zone</td><td>Retrieves the list of instances contained within the specified zone.</td><td>list_instances_within_zone <br/>Investigation</td></tr>
<tr><td>Get Instance Details</td><td>Returns the specified Instance resource details.</td><td>describe_instance <br/>Investigation</td></tr>
<tr><td>Start Instance</td><td>Starts an instance that you have specified using the resource ID.</td><td>start_instance <br/>Miscellaneous</td></tr>
<tr><td>Stop Instance</td><td>Stops an instance that you have specified using the resource ID.</td><td>stop_instance <br/>Miscellaneous</td></tr>
<tr><td>Delete Instance</td><td>Deletes an instance resource that you have specified using the resource ID.</td><td>delete_instance <br/>Miscellaneous</td></tr>
<tr><td>Reset Instance</td><td>This is a hard reset the VM does not do a graceful shutdown. Performs a reset on the instance that you have specified using the resource ID.</td><td>reset_instance <br/>Miscellaneous</td></tr>
<tr><td>Aggregated List Instances</td><td>Retrieves an aggregated list of all of the instances in your project across all regions and zones.</td><td>get_aggregated_list_instances <br/>Investigation</td></tr>
<tr><td>Set Instance Label</td><td>Set user defined labels on a Specified instance</td><td>set_device_label <br/>Investigation</td></tr>
<tr><td>Disk Snapshot</td><td>takes a snapshot of persistent disk</td><td>take_disk_snapshot <br/>Investigation</td></tr>
</tbody></table>
### operation: List Instances within Zone
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Filter</td><td>A filter expression that filters resources listed in the response.
</td></tr><tr><td>OrderBy</td><td>Sorts list results by a certain order. By default, results are returned in alphanumerical order based on the resource name.
</td></tr><tr><td>Page Token</td><td>Specifies a page token to use.
</td></tr><tr><td>Max Results</td><td>The maximum number of results per page that should be returned. Acceptable values are 0 to 500, inclusive. (Default: 500)
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "items": [],
    "nextPageToken": "",
    "selfLink": "",
    "warning": {}
}</pre>
### operation: Get Instance Details
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Resource ID</td><td>Name of the instance resource to return.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "creationTimestamp": "",
    "name": "",
    "description": "",
    "tags": {},
    "machineType": "",
    "status": "",
    "statusMessage": "",
    "zone": "",
    "canIpForward": "",
    "networkInterfaces": [],
    "disks": [],
    "metadata": {},
    "serviceAccounts": [],
    "selfLink": "",
    "scheduling": {},
    "cpuPlatform": "",
    "labels": {},
    "params": {},
    "labelFingerprint": "",
    "minCpuPlatform": "",
    "guestAccelerators": [],
    "startRestricted": "",
    "deletionProtection": "",
    "resourcePolicies": [],
    "sourceMachineImage": "",
    "reservationAffinity": {},
    "hostname": "",
    "displayDevice": {},
    "shieldedInstanceConfig": {},
    "shieldedInstanceIntegrityPolicy": {},
    "sourceMachineImageEncryptionKey": {},
    "confidentialInstanceConfig": {},
    "fingerprint": "",
    "privateIpv6GoogleAccess": "",
    "advancedMachineFeatures": {},
    "lastStartTimestamp": "",
    "lastStopTimestamp": "",
    "lastSuspendedTimestamp": "",
    "satisfiesPzs": "",
    "networkPerformanceConfig": {},
    "keyRevocationActionType": ""
}</pre>
### operation: Start Instance
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Resource ID</td><td>Name of the instance resource to return.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "creationTimestamp": "",
    "name": "",
    "zone": "",
    "clientOperationId": "",
    "operationType": "",
    "targetLink": "",
    "targetId": "",
    "status": "",
    "statusMessage": "",
    "user": "",
    "progress": "",
    "insertTime": "",
    "startTime": "",
    "endTime": "",
    "error": {},
    "warnings": [],
    "httpErrorStatusCode": "",
    "httpErrorMessage": "",
    "selfLink": "",
    "region": "",
    "description": "",
    "operationGroupId": ""
}</pre>
### operation: Stop Instance
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Resource ID</td><td>Name of the instance resource to return.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "creationTimestamp": "",
    "name": "",
    "zone": "",
    "clientOperationId": "",
    "operationType": "",
    "targetLink": "",
    "targetId": "",
    "status": "",
    "statusMessage": "",
    "user": "",
    "progress": "",
    "insertTime": "",
    "startTime": "",
    "endTime": "",
    "error": {},
    "warnings": [],
    "httpErrorStatusCode": "",
    "httpErrorMessage": "",
    "selfLink": "",
    "region": "",
    "description": "",
    "operationGroupId": ""
}</pre>
### operation: Delete Instance
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Resource ID</td><td>Name of the instance resource to return.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "creationTimestamp": "",
    "name": "",
    "zone": "",
    "clientOperationId": "",
    "operationType": "",
    "targetLink": "",
    "targetId": "",
    "status": "",
    "statusMessage": "",
    "user": "",
    "progress": "",
    "insertTime": "",
    "startTime": "",
    "endTime": "",
    "error": {},
    "warnings": [],
    "httpErrorStatusCode": "",
    "httpErrorMessage": "",
    "selfLink": "",
    "region": "",
    "description": "",
    "operationGroupId": ""
}</pre>
### operation: Reset Instance
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>Resource ID</td><td>Name of the instance resource to return.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "creationTimestamp": "",
    "name": "",
    "zone": "",
    "clientOperationId": "",
    "operationType": "",
    "targetLink": "",
    "targetId": "",
    "status": "",
    "statusMessage": "",
    "user": "",
    "progress": "",
    "insertTime": "",
    "startTime": "",
    "endTime": "",
    "error": {},
    "warnings": [],
    "httpErrorStatusCode": "",
    "httpErrorMessage": "",
    "selfLink": "",
    "region": "",
    "description": "",
    "operationGroupId": ""
}</pre>
### operation: Aggregated List Instances
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Include all scopes</td><td>Indicates whether every visible scope for each scope type (zone, region, global) should be included in the response. For resource types which predate this field, if this flag is omitted or false, only scopes of the scope types where the resource type is expected to be found will be included.
</td></tr><tr><td>Filter</td><td>A filter expression that filters resources listed in the response.
</td></tr><tr><td>OrderBy</td><td>Sorts list results by a certain order. By default, results are returned in alphanumerical order based on the resource name.
</td></tr><tr><td>Page Token</td><td>Specifies a page token to get that specified page of results.
</td></tr><tr><td>Max Results</td><td>The maximum number of results per page that should be returned.
</td></tr><tr><td>Return partial success</td><td>Opt-in for partial success behavior which provides partial results in  case of failure. The default value is false.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "items": {},
    "nextPageToken": "",
    "selfLink": "",
    "warning": {},
    "unreachables": []
}</pre>
### operation: Set Instance Label
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Instance Name</td><td>Specify the name of the instance for this request
</td></tr><tr><td>Zone</td><td>Specify the name of the zone for this request
</td></tr><tr><td>Key Name</td><td>Specify the key of the Label
</td></tr><tr><td>Key Value</td><td>Specify the value of the Label
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "items": [],
    "nextPageToken": "",
    "selfLink": "",
    "warning": {}
}</pre>
### operation: Disk Snapshot
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Zone</td><td>The name of the zone for this request.
</td></tr><tr><td>instance_name</td><td>The name of the instance for this request.
</td></tr></tbody></table>
#### Output
The output contains the following populated JSON schema:

<pre>{
    "kind": "",
    "id": "",
    "items": [],
    "nextPageToken": "",
    "selfLink": "",
    "warning": {}
}</pre>
## Included playbooks
The `Sample - google-cloud-compute - 1.2.0` playbook collection comes bundled with the Google Cloud Compute connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR&trade; after importing the Google Cloud Compute connector.

- Aggregated List Instances
- Delete Instance
- Disk Snapshot
- Get Instance Details
- List Instances within Zone
- Reset Instance
- Set Instance Label
- Start Instance
- Stop Instance

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection since the sample playbook collection gets deleted during connector upgrade and delete.
