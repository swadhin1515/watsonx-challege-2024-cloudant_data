IBM Cloud
Cloudant 
Product guide
Edition notices
This PDF was created on 2024-07-16 as a supplement to  
Cloudant
 in the IBM Cloud docs. It might not be a complete set of information or the latest version. For the
latest information, see the IBM Cloud documentation at 
https://cloud.ibm.com/docs/Cloudant?topic=Cloudant-getting-started-with-cloudant
.Getting started with IBM Cloudant
The IBM® Cloudant® for IBM Cloud® 
Getting started
 tutorial demonstrates how to use the IBM Cloud® dashboard to create an IBM Cloudant service
instance and obtain service credentials to connect to it. Finally, it guides you through the 
creation of a simple, locally hosted web application that uses your
IBM Cloudant database.
Objectives
Create a service instance.
Create an IBM Cloudant service credential.
Step 1: Creating a service instance
1
. 
Log in to your IBM Cloud account, and click 
Create resource
.
Figure 1. IBM Cloud Dashboard
2
. 
Type 
Cloudant
 in the Search bar and click to open it.
3
. 
Select an offering and an environment.
4
. 
Type an instance name.
Figure 2. IBM Cloudant service name and credentials
 Note: 
The IBM Cloud Dashboard can be found at: 
https://cloud.ibm.com/
. After you authenticate with your username and password, you're
presented with the IBM Cloud Dashboard.
Cloudant
   
3(In this example, the instance name is 
Cloudant-o7
.) Verify that the resource group and authentication methods are correct. Add a tag if you like.
The authentication methods that are available include 
IAM
 or 
IAM and legacy credentials
. 
For more information, see 
authentication methods
.
5
. 
Select your plan.
6
. 
To create the service, click 
Create
:
After you click 
Create
, the system displays a message to say that the instance is being provisioned, which returns you to the Resource list. From the
Resource list, you see that the status for your instance is, 
Provision in progress
.
7
. 
After you create an instance, the status changes to 
Active
.
8
. 
Click the instance, and proceed to the next section, 
Creating service credentials
.
Step 2: Creating service credentials
1
. 
For more information about where to find your credentials, see 
Locating your credentials
.
2
. 
See more information on 
Understanding your service credentials
.
3
. 
Now, you're ready to use your IBM Cloudant database and get familiar with the basic features of IBM Cloud by following this tutorial: 
Creating a web-
based To-Do list
.
 Important: 
The IBM Cloudant team encourages you to use IAM access controls over IBM Cloudant legacy authentication whenever possible.
Cloudant
   
4Plans and provisioning
IBM® Cloudant® for IBM Cloud® Standard is IBM Cloudant's most feature-rich offering, receiving updates and new features first. Pricing is based on
provisioned throughput capacity that is allocated and data storage that is used, making it suitable 
for any required load.
The free 
Lite plan
 includes a fixed amount of throughput capacity and data for development and evaluation purposes. The paid 
Standard plan
 offers
configurable provisioned throughput capacity 
and data storage pricing that scales as your application requirements change. An optional 
Dedicated
Hardware plan
 is also available for an extra monthly fee to run one or more of your Standard plan instances 
on a dedicated hardware environment. The
dedicated hardware environment is for your sole use. If a Dedicated Hardware plan instance is provisioned within a US location, you can optionally select a
HIPAA
 -compliant configuration.
Plans
You can select which plan to use when you 
provision your IBM Cloudant service instance
. The available plans include Lite and Standard. When you select a
plan, Capacity displays, and the Cost estimator shows the 
monthly charge for the selected plan. By default, the 
Lite plan
 is selected.
Lite plan
The Lite plan is free, and is designed for development and evaluation purposes. All of IBM Cloudant's functions are included, but Lite plan instances have a
fixed amount of provisioned throughput capacity and data storage. The provisioned 
throughput capacity is fixed at 20 reads per second, 10 writes per
second, and 5 global queries per second, and data storage is capped at 1 GB.
Storage usage is checked daily. If you exceed your 1-GB storage limit, requests to the IBM Cloudant instance receive a 402 status code with the following
error message, 
Account exceeded its data usage quota. An upgrade to a paid plan is required.
 
A banner also appears on the IBM Cloudant Dashboard. You
can still read and delete data. However, to write new data, you have two options. First, you can upgrade to a paid 
Standard plan
, which removes the write
limitation immediately. Alternatively, you can delete data so that your total storage falls under the 1-GB limit and wait until the next daily storage check
runs for your instance to allow writes again.
If you want to store more than one GB of data, or be able to scale provisioned throughput capacity, move to the 
Standard plan
.
You're limited to one IBM Cloudant Lite plan instance per IBM Cloud account. If you already have one Lite plan instance, you can't create a second Lite plan
instance, or change a Standard plan instance to a Lite plan. If you try, you see the 
following message. 
You can have only one instance of a Lite plan per
service. To create a new instance, either delete your existing Lite plan instance or select a paid plan.
Standard plan
The IBM Cloudant Standard plan is available to all paid IBM Cloud® accounts, either as pay-as-you-go or subscription, and scales to meet the needs of your
application. The Standard plan is priced based on two factors: the provisioned throughput 
capacity that is allocated, and the amount of data that is stored in
the instance.
Pricing is pro-rated hourly with a starting provisioned throughput capacity of 100 reads per second, 50 writes per second, and 5 global queries per second.
This rate is equal to a starting cost of USD $0.105 per hour. You can toggle the provisioned 
throughput capacity up or down by using the user interface or
API. Toggle in increments of 100 reads per second, 50 writes per second, and 5 global queries per second. Costs are calculated for the provisioned
throughput capacity that is 
allocated and not on the metered volume of requests. The Standard plan includes 20 GB of data storage. If you store more than
20 GB, you're charged a defined cost per GB per hour.
Refer to the IBM Cloud Pricing Calculator in the dashboard for pricing at different capacities and currencies, and the 
pricing
 information for examples 
to
estimate costs.
Dedicated Hardware plan
An IBM Cloudant Dedicated Hardware plan instance is a bare metal IBM Cloudant environment that is provisioned for the sole use of your IBM Cloudant
Standard plan instances. The IBM Cloudant Dedicated Hardware plan offers the following options:
An IBM Cloudant Dedicated Hardware plan environment that can be provisioned in any 
IBM® global data center
.
This plan is necessary for HIPAA compliance and must be selected at provisioning time.
Users can choose to bring-your-own-key (BYOK) with customer-managed encryption keys with IBM Key Protect for all environments provisioned 1
January 2020 or later. IBM Cloudant runs on encrypted disks, but to BYOK, the Dedicated Hardware 
plan is required. BYOK encryption details must
be chosen at provisioning time, and the feature isn't available for already-provisioned Dedicated Hardware plan environments.
All Standard plan instances that are deployed on Dedicated Hardware plan environments include both private (internal) endpoints and public
endpoints in locations that support Cloud Service Endpoints (CSE). Using private endpoints allows 
customers to connect to an IBM Cloudant instance
through the internal IBM Cloud® network to avoid upstream application traffic from going over the public network and incurring bandwidth charges.
For more information, see 
Cloud Service Endpoint documentation
 for details about enabling Cloud Service Endpoints for your IBM Cloud® account.
Users of an IBM Cloudant Dedicated Hardware plan environment can employ IP allowlisting by contacting support. IP allowlisting configuration
Cloudant
   
5applies to all instances that are running on the environment. The public and private network allowlists 
can be managed independently, and the
public allowlist can be set to block all traffic so that all traffic goes over the private endpoints.
You can provision one or more Standard plan instances on a single Dedicated Hardware environment. The Dedicated Hardware environment expands or
contracts as needed based on the throughput capacity and data that is used by the Standard plan 
instances. An IBM Cloudant Dedicated Hardware plan
instance has a fixed price that is an addition to the consumption pricing of any Standard plan instances deployed on it. Billing is prorated daily, with a 1-
month minimum duration charged 
for the environment. Provisioning of an IBM Cloudant Dedicated Hardware plan is asynchronous and can take 5-7
business days. To create an IBM Cloudant Dedicated Hardware plan instance and provision a Standard plan instance on it, follow 
the 
Creating and
leveraging an IBM Cloudant Dedicated Hardware plan instance on IBM Cloud
 
tutorial.
Request classes
Throughput provision is identified and measured as one of the following types of request classes:
1
. 
Reads
 (formerly called lookups) which are described in this list.
a
. 
A read of a specific document, based on the 
_id
 of the document.
b
. 
A 
partitioned
 query, which is a request that is made to an IBM Cloudant query endpoint within the 
_partition
 namespace in the request
path, including the following types:
Primary Index (
_all_docs
)
MapReduce View (
_view
)
Search Index (
_search
)
IBM Cloudant Query (
_find
)
2
. 
Writes
, which are creation, modification, or deletion of individual documents.
3
. 
Global Queries
 to global indexes (formerly called queries), which are requests that are made to an IBM Cloudant query endpoint 
not
 within the
_partition
 namespace, including the following types:
Primary Index (
_all_docs
)
MapReduce View (
_view
)
Search Index (
_search
)
IBM Cloudant Query (
_find
)
Provisioned throughput capacity
Throughput provision is identified and measured as a request class of the following operation types: 
Read
, 
Write
, and 
Global Query
.
The measurement of throughput is a simple count of the number of units of each request class, per second, where the second is a 
sliding
 window.
If your account exceeds the number of throughput units that are allotted for a request class, IBM Cloudant rejects requests. The requests are rejected until
the number of units of the request class within the sliding window no longer exceeds 
the number that is provisioned. It might help to think of the sliding 1-
second window as being any consecutive period of 1,000 milliseconds.
For example, the Standard plan is provisioned for 200 reads per second. Your account might use a maximum of 200 reads during a consecutive period of
1,000 milliseconds (1 second). Subsequent reads that are made during the sliding 1,000-millisecond 
period are rejected until the number of reads in that
period drops to less than 200 again.
When a request is rejected because the number of a request class is exceeded, applications receive a 
429
 Too Many Requests
 response.
Recent versions of the 
supported client libraries
 help you handle a 
429
 response. For example, the Java™ library generates a
TooManyRequestsException
 response.
By default, the supported client libraries don't automatically retry a request when a 
429
 response is received.
It's better to ensure that your application handles 
429
 responses correctly. The reason is that the number of retries is limited; regularly transgressing the
number of requests is a strong indicator for moving to a different plan 
configuration.
 Important: 
The Dedicated Hardware plan isn't available to IBM Cloud Dedicated customers. The Dedicated Hardware plan is only available to IBM
Cloud customers.
 Tip: 
The number of read operations that are used by a partitioned query request varies depending on the results returned.
Cloudant
   
6In summary, you must ensure that your application can handle a 
429
 response correctly.
Consumption of read operations by partitioned queries
Partitioned query requests use a variable number of read operations that depend on the results returned. Consumption is based on two axes:
1
. 
The number of rows that are read from the index that is involved in the query.
2
. 
The number of documents read from the database, if any, during the execution of the query.
View queries, search queries, and 
_all_docs
Each block of 100 rows that are read from the index uses one read operation. In addition, each document that is read from the database during execution
of a query uses one read unit.
The number of rows that are read from the index is the same as the number of results returned. Documents are only read from the database when
include_docs=true
 is passed as a query string parameter during the query request.
You can see example costs in the following table:
Table 1. Example costs
Number of results
Include documents
Total Read consumption
Consumption for rows read
Consumption for documents read
199
No
2
2
0
199
Yes
201
2
199
301
No
4
4
0
301
Yes
305
4
301
Reducing use of 
include_docs=true
 is key for reducing read consumption for partitioned 
_all_docs
, view, and search queries.
IBM Cloudant Query
For IBM Cloudant Query requests, the number of read operations used for index rows read relates to the rows read from the underlying index. The rows
are read before filtering occurs based on parts of the selector that can't be satisfied 
by the index. Therefore, these results mean that the rows read value,
and consumed read units, can be higher than the number of eventual results you receive.
In addition, IBM Cloudant Query must read the document for every row that is returned by the underlying index. This way, it can run further filtering that is
required by the selector and passed to the query.
Table 2. Read consumption
Number of
results
Number of rows returned by
index
Total Read
consumption
Consumption for rows
read
Consumption for documents
read
5
199
201
2
199
199
199
201
2
199
5
301
305
4
301
301
301
305
4
301
Using appropriate indexes is key for reducing read consumption for partitioned IBM Cloudant Query queries.
 Note: 
If you're porting an existing application, it might not be able to handle a 
429
 response. As part of your migration verification, check that
your application handles 
429
 responses correctly.
 Note: 
There is a minimum cost of 1 read for all partition queries.
Cloudant
   
7Consumption of read and write operations by replication
Replication
 between two databases uses read capacity on the source database and write capacity on the target database. The replicator is aware of the
rate limits in IBM Cloudant 
and employs staggered retry logic when encountering 
429
 responses associated with reaching the provisioned throughput
capacity limits set for the instance.
You can use the default parameters and replicate a database with a large backlog of documents. In that case, a single replication job uses close to 2500 -
3000 reads per second on the source database and a few writes per second on the target 
database. Users can reduce the approximate read throughput
that is used by a replication job by adjusting the 
performance-related options
 that are 
associated with 
tuning replication speed
. The following table
provides recommended options for users who want to reduce the read capacity used on the 
source database:
Table 3. Reduce read capacity
http_connections
worker_processes
Approximate reads per second on source database
2
1
200
6
2
1000
12
3
2000
20
4
3000 (This value is the default.)
Viewing and changing capacity
Managing the provisioned throughput capacity allocated to an instance can be done by using either the UI or API. Changes to the provisioned throughput
capacity are only allowed by using the paid IBM Cloudant Standard plan. Users of the free 
Lite plan have a fixed amount of provisioned throughput capacity
but can use the Capacity UI to estimate costs for a capacity setting on the Standard plan.
UI - Resource Group
If the IBM Cloudant instance is deployed in a 
Resource Group
, you can change the capacity by following these instructions.
1
. 
Log in to the IBM Cloud Dashboard.
2
. 
Go to the Service Details page for the instance.
3
. 
Click 
Manage
 > 
Capacity
 to view the current and target capacity.
Figure 1. Capacity
4
. 
To change the target capacity, slide the capacity slider to the setting you want.
5
. 
Click 
Update to Standard Plan
.
6
. 
Select the pricing plan that you want, and click 
Save
.
7
. 
Select the type of account that you're looking for by clicking 
Go
.
The checkmark turns yellow and says 
Updating Capacity
 until the target capacity is reached. Capacity changes are asynchronous. The time that is
Cloudant
   
8required to synchronize those changes depends on the size of the changes in 
capacity that were requested and the data that is stored in the instance.
When the target capacity is reached, the following message appears, 
Success. Your capacity will be updated shortly.
API
To use the API to view the current provisioned throughput capacity that is allocated or change the target-provisioned throughput capacity for an IBM
Cloudant instance, see the 
Capacity API
 
documentation.
The API syntax for changing the capacity is also shown in the 
Increase capacity through API
 tab on the Capacity page for instances that are deployed in a
Resource Group.
Monitoring usage
Information about your usage of provisioned throughput capacity is available in the IBM Cloudant Dashboard Monitoring tab. The 
Current Operations
 tab
shows recent consumption of 
provisioned throughput capacity
 
by showing the number of requests that are broken down by reads, writes, and global
queries. The dotted line represents the peak capacity that is allowed according to the provisioned throughput capacity set for the instance.
Current Operations
 tab
Shows recent consumption of 
provisioned throughput capacity
.
Shows the number of requests that are broken down by reads, writes, and global queries.
The peak capacity that is allowed according to the provisioned throughput capacity set for the instance is shown by a dotted line in the following
screen capture.
Figure 4. Monitoring - Current Operations
Denied Requests
 tab
Shows the number of requests that were denied in a given second.
Shows the response, 
429: too many requests.
 Note: 
Capacity increases made by using the IBM Cloud Dashboard can be made up to 100 blocks of capacity. One hundred blocks of capacity
equal 10,000 reads per second, 5,000 writes per second, and 500 global queries per second. If you require more 
capacity, see the 
Need
additional capacity?
 tab on the Capacity page.
Cloudant
   
9Requests are denied because they exceed the provisioned throughput capacity that is allocated to the instance. The graphs are broken down by
reads, writes, and global queries.
Figure 5. Monitoring - Denied Requests
Monitoring helps you recognize that a change to the provisioning in your plan might be advisable. For example, if you frequently approach the maximum
number of database reads, then you can modify the capacity for the instance through the 
Capacity
 UI.
Data usage
The data storage that is measured for billable purposes for an IBM Cloudant instance is inclusive of both JSON data, indexes, and attachments.
Data storage included
This value is the storage capacity that is included in the plan. The Lite plan has a hard limit of 1 GB allowed. The paid Standard plan includes 20 GB for free
and any additional data that is stored is metered for billing.
Data overage
All Lite and Standard plans are monitored for disk space used. When you use more data than the plan allocates, you can expect the conditions that are
described in the following sections to apply:
Lite plan
Disk usage is capped on the Lite plan at 1 GB.
After you reach the cap, you receive a warning on the IBM Cloudant Dashboard and can't write new data. If you try to write new data, a 
402:
payment required
 response occurs.
To write new data, you must either upgrade to the Standard plan or delete data, and wait until the next check runs for your account to be reactivated.
Standard plan
Cloudant
   
10If the account uses more than the 20 GB of storage that is included in the Standard plan, the excess is considered "disk overage". Overage causes the
account to be billed at the indicated price for each extra GB used beyond the 
plan allocation.
The cost for the amount of disk overage is calculated on an hourly basis.
For example, assume your Standard plan increases disk usage to 107 GB for half a day (12 hours). This change means that your instance caused overflow
of 87 GB more than the 20 GB plan allocation, for 12 hours. As the result, you're billed 
an overage charge based on 87 GB x 12 hours = 1044 GB hours for
that extra space.
Overage is calculated by using the maximum number of GB more than the plan allocation during a particular hour within the billing cycle.
Disk overage example
Assume that you start a month of 30 days with a Standard plan service instance that uses 9 GB of storage. Next, your storage increases to 21.5 GB for 15
minutes during the hour beginning at 02:00 of day 3. The instance drops back to 9.5 GB 
for the next 10 minutes of hour 02:00, then increases to 108 GB
for the next 25 minutes of hour 02:00. Finally, your instance finishes the hour and indeed the rest of the month by dropping down to 28 GB.
This pattern means the maximum number of GB more than the plan allocation was 88 GB during hour 2 of day 3. From hour 03:00 of day 3, and for the rest
of the month, your instance was 8 GB more than the plan allocation.
Therefore, from hour 02:00 of day 3, your bill includes an overage based on 88 GB x 1 hour = 88 GB hours.
From hour 03:00 of day 3 to the end of day 3, your bill includes an overage based on 8 GB x 21 hours = 168 GB hours.
From hour 00:00 of day 4 until the end of the month (of 30 days), your bill includes an overage. The overage is based on 8 GB x 24 hours x 27 days = 5184
GB hours.
The total overage bill for the month is based on a total of 88 + 168 + 5184 = 5440 GB hours.
Request and document size limits
IBM Cloudant JSON documents and requests have the following maximum size limits:
Table 4. Maximum size limits for JSON documents and requests
Limit
Maximum Size
Individual Document Size
1 MB
Single Attachment Size
10 MB
Request Body Size
11 MB
If you exceed these limits, a 
413 response
 alerts you.
The IBM Cloudant team recommends that you store binary attachments, or large JSON blobs, in object storage and save a link to the location in an IBM
Cloudant JSON document.
When you replicate, documents or attachments that exceed these limits don't replicate to the target database. For more information about how to detect
replication errors, see 
Replication errors
.
Locations and tenancy
By default, all Lite and Standard plans are deployed on multi-tenant environments. As part of your plan selection, you can choose from the following IBM
Cloud locations.
Chennai (SZR)
Dallas
Frankfurt‡
London
Osaka
Sydney
Seoul (SZR)
Tokyo
Washington DC
Cloudant
   
11Single-Zone Region (SZR) means that only one availability zone is available in that location. All other locations are Multi-Zone Regions (MZR) and leverage
three separate availability zones for instances that are deployed in those locations. 
For more information, see the 
High availability (HA), disaster recovery
(DR), and backup
 documentation.
Dedicated Hardware plan instances can be deployed in most 
IBM data center locations
. See the drop-down menu in the IBM Cloud catalog for an up-to-
date list of available locations.
‡All IBM Cloudant instances that are deployed from the IBM Cloud Frankfurt region are deployed into EU-managed environments. Any IBM Cloudant
account or API key that is generated outside an EU-managed environment can't be granted access to an 
EU-managed IBM Cloudant instance. For more
information, see 
Enabling the EU Supported setting
 for your IBM Cloud account.
Authentication methods
IBM Cloudant is accessed by using an HTTPS API. Where the API endpoint requires it, the user is authenticated for every HTTPS request IBM Cloudant
receives. During provisioning, the available authentication methods include 
Use both legacy credentials and IAM
 
or 
Use only IAM
. For more
information, see the 
IAM guide
 or the legacy 
Authentication API document
.
After you provision an IBM Cloudant instance, the connection URL and IAM authorization details can be found when you generate new credentials in the
Service Credentials tab of the IBM Cloud Dashboard. For more information, see 
Locating your service credentials
. 
If you chose this option during
provisioning, the IBM Cloudant legacy username and password is also included.
High availability, disaster recovery, and backup in a data center
To provide high availability (HA) and disaster recovery (DR) within a data center, all data is stored in triplicate across three separate physical servers in a
cluster. You can provision accounts in multiple data centers, then use continuous 
data replication to provide HA/DR across data centers. IBM Cloudant data
isn't automatically backed up, but supported tools are provided to handle backups. Review the 
Disaster recovery and backup guide
 to explore all HA, DR,
and backup considerations to meet your application requirements.
IBM Cloud Support
Support for Standard and Dedicated plan service instances is optional. Support is provided when you purchase 
IBM Cloud Standard Support
. Support isn't
available for the Lite plan.
For more information, see the 
IBM Cloud Standard Support plans
 and the 
IBM support guide
.
Provisioning an IBM Cloudant instance on IBM Cloud
You can provision an IBM Cloudant Lite or Standard plan instance on IBM Cloud in two ways by:
Using the dashboard. For more information, see the 
Creating an IBM Cloudant instance on IBM Cloud
 tutorial that describes the process.
Creating an IBM Cloudant Dedicated Hardware plan instance. For more information, see the 
Creating and leveraging an IBM Cloudant Dedicated
Hardware plan instance on IBM Cloud
 tutorial that describes the process.
 Important: 
The IBM Cloudant team recommends you use IAM access controls for authentication whenever possible. If you're using IBM Cloudant
legacy authentication, the IBM Cloudant team recommends that you use 
API keys
 rather than account-level credentials for programmatic access
and replication jobs.
 Note: 
The support systems that are used for IBM Cloudant don't offer features for the protection of personal data or sensitive personal data. This
content includes Healthcare Information, health data, Protected Health Information, or data that is 
subject to more regulatory requirements. As
such, the Client must not enter or provide such data.
Cloudant
   
12Pricing
IBM® Cloudant® for IBM Cloud® is priced based on the provisioned throughput capacity that you allocate for your instance, and the amount of data storage
consumed. With IBM Cloudant, you can scale your provisioned throughput capacity up and down, 
and pay a pro-rated hourly rate. The provisioned
throughput capacity is a reserved number of reads per second, writes per second, and global queries per second allocated to an instance. The throughput
capacity setting is the maximum usage level 
for a given second. You can't exceed the reserved capacity for either reads, writes, or global queries. If you do,
an HTTP 429 status code occurs that indicates the application is trying to exceed its provisioned throughput capacity allowance. 
IBM Cloudant usage is
billed hourly.
The estimated monthly cost for a particular level of provisioned throughput and storage capacity can be determined by using the Cost Estimator on the 
IBM
Cloud® Catalog page
 for IBM 
Cloudant.
You can use the IBM Cloud pricing calculator to see estimated costs in other currencies by clicking 
Add to estimate
 from the IBM Cloudant catalog tile.
Specify storage, capacity, and select the country whose currency you want 
to see.
Click 
Calculate cost
 and 
Save
. Now, click 
Review estimate
. Expand the estimate to see more details. If you save multiple estimates, you can then click
Review estimate
 and compare 
them.
You can launch the IBM Cloud Dashboard. Click 
Resource list
 > 
Services
 > 
your instance
 > 
Manage
 > 
Capacity
 to view and change the provisioned
throughput 
capacity, and see the hourly and approximate monthly costs.
Changing Provisioned Throughput Capacity
Let's assume you're building a mobile app with IBM Cloudant and don't yet know the capacity that you might need. In this case, the IBM Cloudant team
recommends that you start with the lowest provisioned throughput capacity and increase it as 
needed by your application's usage over time. IBM Cloudant
bills pro-rated hourly and changing the provisioned throughput capacity doesn't incur downtime.
The minimum provisioned throughput capacity for the Standard plan is 100 reads per second, 50 writes per second, and 5 global queries per second.
When you need to scale up (or down), you can scale in increments of these blocks of capacity. Assuming 
the instance has less than the 20 GB of storage
that is included in the Standard plan, no storage costs are incurred. Go to the provisioned throughput capacity setting from the IBM Cloudant Dashboard >
Account
 > 
Capacity
 
tab, which is shown in the following screen capture:
Figure 1. IBM Cloudant Dashboard Capacity tab
The capacity slider shows the hourly cost of the provisioned throughput capacity. The monthly amount is an estimate based on an average of 730 hours
per month. The cost in any month can be slightly different depending on the number of hours 
in the month.
Reads, writes, and global queries can't be scaled independently. Use the slider to select the number of blocks of provisioned throughput capacity based on
the maximum limit of either reads per second, writes per second, or global queries per 
second as required for your application. For example, if your
application requires 1,000 reads per second, use the slider to select the capacity that offers 1,000 reads per second, 500 writes per second, and 50 global
queries per second. Select 
this capacity even if you don't need the corresponding number of writes or global queries.
Data usage pricing
What about pricing for data overage? How does that work?
Cloudant
   
13Table 1. Pricing for data overage
Plan
Storage
included
Overage limit
Lite
1 GB
Your account is blocked from writing new data until you delete enough data to be under the 1-GB limit, or upgrade to
a higher plan.
Standard
20 GB
Extra storage costs charged per GB per hour, for each GB over the included 20 GB.
IBM Cloud Usage Dashboard
How does data populate the IBM Cloud Usage Dashboard?
Current and historical usage bills can be seen in the IBM Cloud Dashboard, under 
Manage
 > 
Billing and usage
 > 
Usage
. This view shows the totals for
usage that are accrued during a particular 
month at the service, plan, or instance level. The Estimated Total reflects the bill so far for the month or for past
complete months. It shows only the hourly costs that are accrued up to that point for the current month.
Cloudant
   
14Limits
Limits that pertain to the usage of IBM® Cloudant® for IBM Cloud® databases are shown in the following tables.
Databases
Table 1. Limits for databases
Description
Limit
Database size
Consult the IBM Cloudant team if your database is likely to exceed 5 TB in size.
Partition size
10 GB
Indexes
Table 2. Limits for indexes
Description
Limit
Number of global indexes
Unlimited
Number of partition indexes
10
Request payload
Table 3. Limits for request payload
Description
Limit
Total request size
10 MB
Document size
1 MB
Attachment size
10 MB
Request timeouts
Table 4. Limits for request timeouts
Description
Limit
Default
60 seconds
_partition/*
5 seconds
Query
Table 5. Limits for query results
Description
Limit
Default
Unlimited
_partition/*
 default
2000
_search
200
_find
 by using 
text
 index
200
Cloudant
   
15Connecting
IBM® Cloudant® for IBM Cloud® is accessed through an HTTP API. You can see the different parts that you use to connect to IBM Cloudant in the following
list:
Endpoints
Service credentials
Authentication
Accessing the IBM Cloudant Dashboard
Programmatically accessing IBM Cloudant by using 
curl
 or client libraries
Endpoints
IBM Cloudant is accessed through HTTP API endpoints. The endpoints for an instance are shown in both the URL field of the Service Credentials that are
generated for the instance, and in 
Account
 > 
Settings
 
of the IBM Cloudant Dashboard.
All IBM Cloudant HTTP endpoints must be accessed over TLS and prefaced by 
https://
.
The publicly facing external endpoint is shown in the following example:
https://$ACCOUNT.cloudant.com
All instances created after 1 January 2019 include an 
appdomain.cloud
 domain endpoint. The publicly facing external endpoint is shown in the following
example:
https://$ACCOUNT.cloudantnosqldb.appdomain.cloud
Private (internal) endpoints are added to all instances deployed on Dedicated Hardware plan environments. The IBM Cloud Private (internal) network
endpoint is shown in the following example:
https://$ACCOUNT.private.cloudantnosqldb.appdomain.cloud
In the previous example, ACCOUNT is the service name of the service instance user in the URL. An example ACCOUNT is de810d0e-763f-46a6-ae88-
50823dc85581-bluemix, and resulting example external endpoint would be de810d0e-763f-46a6-ae88-50823dc85581-
bluemix.cloudantnosqldb.appdomain.cloud.
Service credentials
To generate service credentials for IBM Cloudant by using the IBM Cloud Dashboard, see the 
Creating an IBM Cloudant instance on IBM Cloud
 tutorial. To
generate service 
credentials from the IBM Cloud CLI, see 
Creating an instance with CLI
.
The following example shows service credentials for an IBM Cloudant instance:
{
  
"apikey"
:
 
"MxVp86XHkU82Wc97tdvDF8qM8B0Xdit2RqR1mGfVXPWz"
,
  
"host"
:
 
"76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"iam_apikey_description"
:
 
"Auto generated apikey during resource-key [...]"
,
  
"iam_apikey_name"
:
 
"auto-generated-apikey-050d21b5-5f[...]"
,
  
"iam_role_crn"
:
 
"crn:v1:bluemix:public:iam::::serviceRole:Manager"
,
  
"iam_serviceid_crn"
:
 
"crn:v1:staging:public:iam-identity::[...]"
,
  
"password"
:
 
"8fb6a16b48903e87b769e7f4968521e85c2394ed8f0e69b2769e56dcb27d2e76"
,
  
"port"
:
 
443
,
  
"url"
:
 
"https://<username>:<password>@76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"username"
:
 
"apikey-v2-58B528DF5397465BB6673E1B79482A8C"
}
The service credentials include the following fields:
username
The username that is required for applications to access the service instance.
password
 Note: 
For more information about how to block public network connectivity by using IP allowlisting, see 
Secure access control
.
Cloudant
   
16The legacy credentials password that is required for applications to access the service instance. This field displays only if the 
Use both legacy
credentials and IAM
 option is chosen.
host
The hostname that is used by applications to locate the service instance. This field displays only if the 
Use both legacy credentials and IAM
option is chosen.
port
The HTTPS port number for accessing the service instance on the host. It's 443 as only HTTPS access is allowed by IBM Cloudant. This field displays
only if the 
Use both legacy credentials and IAM
 option is chosen.
url
The HTTPS URL to access the IBM Cloudant instance. If the 
Use both legacy credentials and IAM
 option is chosen, it also includes the
embedded legacy username and password.
apikey
The IAM API key.
iam_apikey_description
Description of the IAM API key.
iam_apikey_name
ID of the IAM API key.
iam_role_crn
The IAM role that the IAM API key has.
iam_serviceid_crn
The CRN of the service ID.
Authentication
IBM Cloudant has two authentication methods available at provisioning time, either 
Use only IAM
 or 
Use both legacy credentials and IAM
. You can
see the details about your legacy credentials in the service credentials only if the 
Use both legacy credentials and IAM
 authentication method 
is
chosen. The credentials display on the Service credentials tab for your instance. For more information, see the 
IAM guide
 and 
legacy authentication
document for details about using either style of 
authentication.
IBM Cloudant Dashboard
You can open the IBM Cloudant Dashboard for your instance by going to the Manage tab of the IBM Cloud Dashboard instance details page. You can use
either 
Launch
 or 
Launch Cloudant Dashboard
 to open the dashboard in 
a new browser tab. You can do the following tasks by using the IBM Cloudant
Dashboard:
Monitor your current consumption of the instance.
Perform create, retrieve, update, delete on IBM Cloudant databases, documents, and indexes.
Set up and view replication jobs.
View active tasks.
View and update account information like provisioned throughput capacity, announcements, CORS, and settings.
Programmatic access
Command line (curl)
You can leverage the curl command-line utility to access the IBM Cloudant HTTPS API.
For more information, see 
Working with curl
. 
Working with curl
 provides details on supplying a username and password to access the IBM Cloudant API
with curl.
 Important: 
The IBM Cloudant team recommends you use IAM access controls for authentication whenever possible. If you're using IBM Cloudant
legacy authentication, you must use 
API keys
 
rather than account-level credentials for programmatic access and replication jobs.
Cloudant
   
17If you use IBM Cloud IAM authentication, you must first get an IBM Cloud IAM token by using an API key. You pass the IAM token to the IBM Cloudant
instance to authenticate. For more information, see 
Passing an IBM Cloud IAM token to authenticate with a service's API
 tutorial.
Client libraries
IBM Cloudant has official, supported client libraries for Java™, Node.js, Python, Swift, Go, and Mobile. For more information, see the 
client libraries
documentation
 
to access the libraries, and see examples for connecting to an IBM Cloudant instance from each.
 Note: 
You can't use an IAM API key directly to authenticate against IBM Cloudant.
Cloudant
   
18Learning Center
The IBM® Cloudant® for IBM Cloud® Learning Center offers a video series to help you learn to use IBM Cloudant. The videos start with the basics of using
IBM Cloudant. Then the videos walk you through document structure, the API, indexing and querying, 
and include an 
Under the Hood
 topic that highlights
the architecture that powers the service.
You can use the 
playlist
 to go through the courses, or navigate directly to the topic of your choosing.
Introduction to IBM Cloudant video
Learn about the IBM Cloudant 17-part video series that provides an overview of the IBM Cloudant database-as-a-service.
View video: 
Introduction to IBM Cloudant
Under the hood video script
Welcome to the Introduction to IBM Cloudant course, an 17-part video series that gives you an overview of the IBM Cloudant database-as-a-service.
This video is part 17 - 
Under the hood
.
Let's look at how an IBM Cloudant service is organized: This overview applies to the IBM Cloudant services that map to CouchDB 2 and 3. CouchDB 4 is
built on different technology.
IBM Cloudant is a distributed database with data that is stored around a cluster of storage nodes. Picture the IBM Cloudant service as ring of nodes, in this
case twelve. Every node can deal with incoming API calls and every node has responsibility 
for storing some of the data: shards and associated secondary
indexes of databases that exist in the cluster.
When data is written to IBM Cloudant, one of the nodes in the ring handles the request: Its job is to instruct three copies of the data to be stored in three
storage nodes. Data is stored in triplicate in IBM Cloudant, so each shard of a database 
is stored multiple times, often across a region's availability zones.
When you make an API call to write data and get a response back, we write the data to at least two of the three storage nodes. Data is flushed to disk - it
isn't cached in memory to be flushed data. We consider that technique too risky and 
prone to data loss.
When you create a database, a number of database shards are created (16 by default) which are spread around the cluster. Three copies of each shard
exist, which equals 48 shard copies.
You don't see any of this activity. The activity is handled for you transparently when you create a database.
What happens if a node goes down or needs to be rebooted for maintenance? The rest of the cluster continues as normal. Most shards still have three
copies of data but some have only two. API calls continue to work as normal, only two copies 
of the data are written.
Even if two nodes go down, most shards still have three copies, some have two, and some have one. Writes continue to work, although the HTTP response
code reflects that the quorum of two node confirmations wasn't reached.
It's the same story for reads. Service continues with a failed node. We can survive one failed node...
Or more failed nodes. If a copy of each node exists, the API continues to function.
When a node returns, it catches up any missed data from its peers and then returns into service, handling API calls and answering queries for data.
The nature of this configuration is that IBM Cloudant exhibits eventual consistency. Any node can handle a request. Data is distributed around nodes
without the sort of locking that you might see in a relational database.
IBM Cloudant favors availability over consistency: It would rather be up and answering API calls than be down because it can't provide consistency
guarantees. (A relational database is often configured in the opposite way: It operates in a 
consistent manner or not at all.) The upshot of eventual
consistency for a developer is that your app must not 
read its writes
 in a short time. A small-time window might exist in which it is possible to see an
older version 
of a document than the one you updated. Eventually, the data flows around the cluster, and in most cases, the quorum mechanism provides
the illusion of consistency, but it is best not to rely on it.
 Note: 
In CouchDB 4, and in IBM Cloudant services based on that code version, a different consistency model is employed.
Cloudant
   
19If your data model requires you to update a document over and over in a short time window, it's possible that multiple writes for the same revision number
are accepted. These writes lead to a branch in the revision tree - known as a conflict. 
In this example revision 
2
 was modified in two different ways,
causing two revision 3s. It's possible to tidy up conflicts programmatically, but they must be avoided as they can cause performance issues in extreme
circumstances.
Conflicts can also happen when you use replication and a document is modified in different ways, and then the conflicting revisions are merged in by using
replication. IBM Cloudant does not throw away data in this scenario. A 
winning
 
revision is chosen, but the nonwinning revisions can be accessed and your
application can resolve the conflict by electing a new winner, deleting unwanted revisions, or any action you need. A conflict is not an error condition. It's a
side 
effect of having disconnected copies of data that can be modified without locking. IBM Cloudant chooses to handle conflicts by not discarding clashing
changes, but storing them as a conflict.
To check a document for conflicts, simply add 
?conflicts=true
 to a fetch of a single document. Any conflicting revisions are listed in the 
_conflicts
array.
Unwanted revisions can be removed by using the normal 
DELETE
 operation, specifying the rev token of the revision you want to delete. The bulk API is also
good for removing conflicting revisions, even for removing multiple conflicts 
from the same document.
To summarize, IBM Cloudant is a distributed service that stores databases, which are broken into multiple shards, with three copies of each shard spread
around a ring of storage nodes. IBM Cloudant is eventually consistent, favoring high availability 
over strong consistency.
Avoid writing to the same document over and over so as not to create conflicts. Although conflicts are sometimes inevitable in replication situations.
Embrace eventual consistency - don't try to make IBM Cloudant consistent.
That's the end of this course. For more information, see the 
IBM Cloudant documentation
 and 
blog
.
 Note: 
IBM Cloudant products based on CouchDB 4 might have a different consistency model.
Cloudant
   
20Security & compliance
Security
Protecting application data for large-scale web and mobile apps can be complex, especially with distributed and NoSQL databases.
Just as it reduces the effort of maintaining your databases to keep them running and growing nonstop, IBM® Cloudant® for IBM Cloud® also ensures your
data stays secure and protected.
Tier one physical platforms
The IBM Cloudant DBaaS is physically hosted on Tier-1 cloud infrastructure providers such as IBM Cloud® and Amazon. Therefore, your data is protected by
the network and physical security measures that are employed by those providers, including 
(but not limited to):
Certifications - Compliance with SSAE16, SOC2 Type 1, ISAE 3402, ISO 27001, CSA, and other standards.
Access and identity management.
General physical security of data centers and network operations center monitoring.
Server hardening.
IBM Cloudant gives you the flexibility to choose or switch among the different providers as your SLA and cost requirements change.
Secure access control
IBM Cloudant has a multitude of built-in security features for you to control access to data:
Feature
Description
Authentication
IBM Cloudant is accessed by using an HTTPS API. Where the API endpoint requires it, the user is authenticated for every HTTPS
request IBM Cloudant receives. IBM Cloudant supports both legacy and IAM access controls. For more information, 
see the 
IAM
guide
 or the legacy 
Authentication API document
.
Authorization
IBM Cloudant supports both legacy and IAM access controls. The IBM Cloudant team recommends that you use IAM access
controls for authentication whenever possible. If you're using IBM Cloudant legacy authentication, IBM Cloudant team
recommends 
that you use 
API keys
 rather than account-level credentials for programmatic access and replication jobs. For more
information, see the 
IAM guide
 
or the legacy 
Authentication document
 and the legacy 
Authorization document
.
At-rest
encryption
All data that is stored in an IBM Cloudant instance is encrypted at rest by using LUKS1 with 256-bit Advanced Encryption Standard
(AES-256). By default, IBM Cloudant manages the encryption keys for all environments. If you require bring-your-own-key 
(BYOK)
encryption for encryption-at-rest, BYOK is enabled by using your encryption key that is stored in an IBM Cloud Key Protect
instance. IBM Cloudant supports the BYOK feature for new IBM Cloudant Dedicated Hardware plan instances 
that are deployed in
all regions. For more information, see the 
Creating an IBM Cloudant Dedicated Hardware plan instance
 
tutorial for details on how
to choose BYOK at provisioning time.
In-flight
encryption
All access to IBM Cloudant is encrypted by using HTTPS.
Client-side
encryption
Customers can use client-side encryption to ensure that the data protection is controlled by the data owner and the data is never
visible to the service provider.
TLS
IBM Cloudant requires the use of TLS 1.2+. IBM Cloudant strongly recommends that you do not pin certificates in your application.
Certificates renew regularly, at least annually, and intermediate and root certificates could change when 
they do. IBM Cloudant
does not send out notifications before certificate renewals. We recommend that you keep your certificate truststore up to date with
the latest root certificates. IBM Cloudant acquires its certificates from DigiCert. 
You can find their root certificates on the 
DigiCert
Trusted Root Authority Certificates
 page. IBM Cloudant sends a notification 
if we move to a different certificate authority.
Public
Endpoints
All IBM Cloudant instances are provided with external endpoints that are publicly accessible.
 Tip: 
More details about the certifications are available in the 
Compliance information
.
Cloudant
   
21Table 1. IBM Cloudant security features
Private
Endpoints
All instances that you deploy on Dedicated Hardware plan environments also have private (internal) endpoints. Using private
endpoints allows customers to connect to an IBM Cloudant instance through the internal IBM Cloud® network to avoid 
upstream
application traffic from going over the public network and incurring bandwidth charges. For more information, see 
Service Endpoint
documentation
, 
and also, see documentation about 
enabling Service Endpoints
 for your IBM Cloud® account. If you want to allow
only a subset of IP addresses to be able to access your application, 
refer to IP allowlisting in the next row.
IP allowlisting
IBM Cloudant customers, who have an IBM Cloudant Dedicated Hardware plan environment, can allowlist IP addresses to restrict
access to only specified servers and users. IP allowlisting isn't available for any IBM Cloud Public Lite or Standard 
plans that are
deployed on multi-tenant environments. Open a support ticket to request an IP allowlist for a specific set of IP addresses or IP
ranges. The public and private network allowlists can be managed independently, and the public 
allowlist can be set to block all
traffic so that all traffic is over the private endpoints. IP allowlists apply to both the IBM Cloudant API and Dashboard, so be mindful
to include any administrator IP addresses that need to access 
the IBM Cloudant Dashboard directly.
CORS
Enable CORS support for specific domains by using the IBM Cloudant Dashboard or API. For more information, see the 
CORS API
documentation
.
Protection against data loss or corruption
IBM Cloudant has a number of features to help you maintain data quality and availability:
Table 2. IBM Cloudant data quality and availability features
Feature
Description
Redundant and
durable data
storage
By default, IBM Cloudant saves to disk three copies of every document to three different nodes in a cluster. Saving the copies
ensures that a working failover copy of your data is always available, regardless of failures.
Data
Replication and
export
You can replicate your databases continuously between clusters in different data centers or Apache CouchDB. Another option is to
export data from IBM Cloudant (in JSON format) to other locations or sources (such as your own data center) 
for added data
redundancy.
Compliance
IBM® Cloudant® for IBM Cloud® provides a trustworthy and secure cloud database system. The service is built on best-in-industry standards, including ISO
27001:2013.
Tier-1 physical systems
IBM Cloudant DBaaS is physically hosted on Tier-1 cloud infrastructure providers such as IBM Cloud®. Therefore, your data is protected by the network and
physical security measures that are employed by these providers.
General Data Protection Regulation (GDPR)
The GDPR seeks to create a harmonized data protection law framework across the EU. It also aims to give citizens back the control of their personal data,
while it imposes strict rules on those entities who host and "process" this data, 
anywhere in the world. The Regulation also introduces rules that relate to
the free movement of personal data within and outside the EU. For more information, see the 
IBM privacy statement
.
HIPAA
IBM Cloudant meets the required IBM controls that are commensurate with the Health Insurance Portability and Accountability Act of 1996 (HIPAA)
Security and Privacy Rule requirements. These requirements include the appropriate administrative, 
physical, and technical safeguards required of
Business Associates in 45 CFR Part 160 and Subparts A and C of Part 164. HIPAA must be requested at the time of provisioning and applies to the IBM
Cloudant Enterprise plan, IBM Cloudant on IBM 
Cloud Dedicated plan, and IBM Cloudant Dedicated Hardware plan on IBM Cloud. Contact your sales
representative to sign a Business Associate Addendum (BAA) agreement with IBM.
International Organization for Standardization (ISO)
IBM Cloudant and IBM Cloudant Dedicated Cluster are audited by a third-party security firm and meet ISO 27001, ISO 27017, and ISO 27018
requirements. For more information, see the 
IBM Cloudant Compliance page
 for links to the certificates. The following descriptions on the IBM Cloudant
Compliance page cover the IBM Cloudant service and respective certifications:
Cloudant
   
22IBM Cloud Services (PaaS and SaaS) certified cloud product listing
IBM Cloud Services (PaaS and SaaS) certificate - ISO 27001
IBM Cloud Services (PaaS and SaaS) certificate - ISO 27017
IBM Cloud Services (PaaS and SaaS) certificate - ISO 27018
PCI
The following IBM Cloudant plans are compliant with the Payment Card Industry Data Security Standard (PCI DSS):
Multi-tenant Lite.
Standard.
Standard plan instances that are deployed on Dedicated Hardware plan environments.
IBM Cloud completes annual PCI DSS assessments by using an approved Qualified Security Assessor (QSA), and the resulting Attestations of Compliance
(AOCs) and Service Responsibility Matrix guides are available upon customer request. Auditors 
reviewed IBM Cloudant for compliance under PCI DSS
version 3.2.1 at Service Provider Level 1.
Customers are responsible for the storing, processing, and transmission of their cardholder data, and can create cardholder data environments (CDEs) that
can store, transmit, or process cardholder data by using IBM Cloudant. Customers can use 
the IBM Cloud AOCs and SRM guides when they seek their own
PCI DSS certifications. It is the responsibility of the customer to document and operate CDEs and applications that are built by using IBM Cloud Platform
services in a PCI DSS-compliant 
manner.
IBM Cloudant documentation on 
service security
 and 
deletion of data
 
covers methods to manage cardholder data within the environment in accordance
with PCI requirements. It is the customer’s responsibility to familiarize themselves with these processes and to manage data retention and removal from
the service 
according to the customer’s policies. To facilitate this process, no cardholder data can be used in an IBM Cloudant document ID. If PAN data is
to be stored in IBM Cloudant, they must be rendered unreadable (in accordance with PCI requirement 
3.5) before transmission to the IBM Cloudant
service.
A full list of PCI DSS-ready IBM Cloud Platform services and options to request that a PCI DSS AOC and SRM guide can be found at the 
IBM Cloud
compliance page
.
SOC 1 Type 2, SOC 2 Type 2, and SOC 3 Certification
IBM provides a Service Organization Controls (SOC) report for IBM Cloudant. The reports evaluate IBM's operational controls according to the criteria set by
the American Institute of Certified Public Accountants (AICPA) Trust Services Principles. 
The Trust Services Principles define adequate control systems and
establish industry standards for service providers such as IBM Cloud to safeguard their customers' data and information.
You can request an SOC report from the Customer portal or contact your sales representative. Alternatively, you can open a support ticket with 
IBM Cloud
Support
.
Data privacy and governance
As a pioneer in the provision of a fully managed and globally distributable Database-as-a-Service, IBM® Cloudant® for IBM Cloud® allows customers to
locate data in any global IBM Cloud® or AWS region. By providing customers with such high levels 
of data mobility to serve the local needs of customers,
IBM®, and IBM Cloudant take data privacy and governance seriously.
IBM Cloud data privacy processing processes and procedures are documented within the IBM Cloud DPA. This Data Processing Addendum (DPA) and its
applicable DPA Exhibits apply to the Processing of Personal Data by IBM Cloud on behalf of Client (Client 
Personal Data). The processing of Personal Data
is subject to the General Data Protection Regulation 2016/679 (GDPR). It is also subject to any other data protection laws that are identified at 
Data
Protection Laws
 in order to provide services (Services) according to the Agreement between Client and IBM Cloud. The IBM Cloud DPA can be found at
Data Processing Addendum
.
In addition to the DPA, the cloud services contain DPA exhibits that detail the types of data that is processed by this service. Cloud services also contain
the relevant processing locations (including hosting locations) where client PI is processed. 
The relevant DPA exhibit for IBM Cloudant can be found on the
IBM Cloud Terms site
.
IBM Cloud relies on Standard Contractual Clauses (as our primary data transfer mechanism) in our customer contracts. IBM Cloud also relies on numerous
supplementary measures to help clients ensure an adequate level of protection when they transfer 
personal data outside of the EU/EEA. For more
information, see EU Standard Contractual Clauses that are signed by all 
IBM Cloud Data Importers
, 
if applicable.
 Tip: 
If you intend to store sensitive information in an IBM Cloudant database, you must use client-side encryption to render data unreadable to
IBM Cloudant operators. For example, for PCI DSS compliance, you must encrypt the Primary Account Number 
(PAN) before sending a document
that contains it to the database.
Cloudant
   
23IBM Cloudant does not move your data without notification. IBM Cloudant relies on centralized components for aspects of the service. Of particular interest
for data residency are logs that contain URLs. These logs are sent out of region-specific 
infrastructure, to centralized logging components. For any data
where residency is a concern, avoid its inclusion within URLs such as in the path or query string. IBM Cloudant documentation describes how this task can
be achieved for various 
areas of our API. For more information, see 
Multi-query a MapReduce view
 for an example of how to use POST for view queries
rather than GET.
For the position of IBM Cloud on trust and transparency, in relation to customer data, see 
Trust principles
.
If more questions that are associated with the privacy principles of IBM Cloud arise, email 
DPA.Help.project@uk.ibm.com
. For more information, see
Compliance
 
about the overall standards for compliance of IBM Cloudant.
Audit logging
Audit logs are available for IBM® Cloudant® for IBM Cloud®. You can find more details on how to obtain audit logs depending on whether you use IBM
Cloudant or outside IBM Cloud®.
IBM Cloudant for IBM Cloud
Users of IBM Cloudant can use IBM Cloud® Activity Tracker to access audit logs for the service. IBM Cloud Activity Tracker records user-initiated activities
that change the state of a service in IBM Cloud. You can use this service to investigate 
abnormal activity and critical actions and to comply with regulatory
audit requirements. You can also be alerted about actions as they happen. The events that are collected comply with the IBM Cloud Auditing Data
Federation (CADF) standard. 
For more information, see 
IBM Cloud Activity Tracker events
.
IBM Cloudant not in IBM Cloud
Users of IBM Cloudant outside of IBM Cloud, such as users of IBM Cloudant Enterprise dedicated clusters, can contact support to request audit logs for
exceptional purposes. The process is described in the following section. Any user who requires 
frequent access to audit logs for purposes such as
compliance audits must migrate to IBM Cloudant in IBM Cloud.
How to access audit logs for your account
Audit logging records the IBM Cloudant principals who accessed data that is stored in IBM Cloudant. For all HTTP API access to IBM Cloudant, the audit log
function records the following information about each HTTP request:
Table 1. Recorded audit information
Information
Description
Principal
Account credentials, API keys, or IBM Cloud IAM credentials, as identified by an HTTP request header.
Action
The action carried out, for example, document read.
Resource
Details about the account, database, and document accessed or query made.
Timestamp
A record of the time and data of the event.
IBM Cloudant audit logs can be used to understand:
What and when databases and documents were accessed within an account, and by whom.
What and when queries were run, and by whom.
What a specific principal or user that is accessed, updated, or deleted, and when.
What and when replication documents were created or deleted.
To request access to the audit logs for your account, contact IBM Cloudant support. Support provides a copy of the audit logs that are of interest to you.
When you contact support, be sure to include the following information:
The IBM Cloudant account that the request relates to.
The time frame for audit logs (must not be more than one month per support request).
Any specific databases, documents, or principals of interest.
General Data Protection Regulation (GDPR)
The GDPR seeks to create a harmonized data protection law framework across the EU. It aims to give citizens back the control of their personal data, while
Cloudant
   
24it imposes strict rules on the ones who host and "process" this data, anywhere 
in the world. The Regulation also introduces rules that relate to the free
movement of personal data within and outside the EU.
With the 
General Data Protection Regulation
, IBM® Cloudant® for IBM Cloud® customers can rely on the IBM Cloudant team's understanding and
compliance with emerging data privacy standards 
and legislation. Customers can also rely on IBM's wider ability to provide a comprehensive suite of
solutions to assist businesses of all sizes with their own internal data governance requirements.
How do I audit access to IBM Cloudant?
You can find information about auditing in 
Audit logging
.
Supported classifications of Personal Data
The following categories of 
Personal Data
 are supported by IBM Cloudant for GDPR:
Identity and civil status
Personal life
Professional life
Location data
Connectivity and device data
Sensitive Personal Data
 is restricted to the following category:
Health data, extra conditions apply to be covered in the 
IBM Cloudant Dedicated Cluster Service Description
 
and 
IBM Cloud® Additional Service
Description
.
If you store healthcare data, you 
must
 notify IBM Cloudant before you write any data.
For more information about supported classifications of Personal Data, see the 
Data Sheet Addendum (DSA) under 2. Personal Data
.
Data about me
IBM Cloudant records some data about its users, and is a Data Controller for said Personal Information (PI) data. The data that IBM Cloudant records
depends on the type of account you have.
If you have an IBM Cloudant Dedicated Cluster or IBM Cloudant Enterprise Cluster, IBM Cloudant records data about you and are considered a Data
Controller for your data within the context of GDPR. If you have an IBM Cloudant Dedicated Cluster 
or IBM Cloudant Enterprise Cluster, IBM Cloudant
stores the following information about you:
Name
Email
The data that IBM Cloudant holds can be viewed and updated through the IBM Cloudant Dashboard.
If you have an account that is provisioned by IBM Cloud (including a dedicated instance), IBM Cloudant 
does not
 collect the personal data that was
discussed earlier. This data is held by IBM Cloud.
IBM Cloudant processes limited customer PI in the course of running the service and optimizing the user experience of it. IBM Cloudant uses email for
contacting customers. Monitoring customer interactions with the IBM Cloudant Dashboard is the 
other way IBM Cloudant processes PI.
Restriction of processing
IBM Cloudant sends dashboard interaction data to Segment. It's possible to ask IBM Cloudant to restrict processing of customer PI in this way with an IBM
Cloudant support request through the 
IBM Cloud Support portal
. 
Upon receipt of such a request, IBM Cloudant deletes information that is associated with
the customer as sent to Segment, and prevents further data from being sent. IBM Cloudant needs to retain the ability to contact dedicated customers 
by
email. IBM Cloudant provides an interface for customers to keep this information up to date either directly, or by using customer configuration of their
contact details with their IBM Cloud account details.
Is the IBM Cloudant database encrypted?
All clusters have an encrypted file system (encryption at rest) that uses Linux™ Unified Key Setup (LUKS). Data in the database is visible to the operations
and support teams (see the following paragraph).
 Important: 
Do not use sensitive data for IBM Cloudant instance names when you provision by using IBM Cloud, such as: Personal Information (PI),
Personal Identifying Information (PII), and Customer-specific Data.
Cloudant
   
25For sensitive data, that you determine must remain invisible to IBM Cloudant, you must encrypt or otherwise protect (pseudonymize) your data before you
send it to us. Do not use PI as a document 
_id
 in your URLs, for example, 
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID
, 
since PI is
always visible and written to the access logs.
Data locations
Locations where IBM Cloudant processes personal data are made available, and kept up to date, through the DSA.
For more information about data locations, see the 
DSA under 7. IBM Hosting and Processing Locations
.
Service security
Using IBM Cloudant securely
As a user of IBM Cloudant, you must follow these guidelines:
Use the default CORS configuration to prevent unexpected access.
Use API keys liberally, since components can have 
least privileged access
, which is coupled with the audit log. This practice helps you
understand who accessed which data.
Encrypt or otherwise protect (pseudonymize) sensitive data that you determine must remain invisible to IBM Cloudant.
Physical and environmental security measures
Physical security of our data centers is handled by the infrastructure providers: IBM Cloud®, AWS, and 21Vianet. All hold externally audited certifications
for their physical security. IBM Cloudant doesn't provide further details of the physical 
security controls in place at our data centers.
Physical security of the office locations that are used by our personnel is handled by IBM Corporate. Certification details and attestation reports (that is,
ISO and SOC2) can be provided to the customer upon request.
Technical and Organizational Measures
Technical and Organizational Measures (TOMs) are employed by IBM Cloudant to ensure the security of Personal Data. IBM Cloudant holds externally
audited certifications for the controls IBM Cloudant employs. Certification details and attestation 
reports (that is, ISO and SOC2) can be provided to the
customer upon request.
Service access to data
IBM Cloudant operations and support staff have access to customer data and can access it during routine operations. This access is only done as required
in order to operate and support the service. Access is also limited to a 
need to know
 
basis and is logged, monitored, and audited.
Deletion of data
Deleting a document
When a document is deleted, the database creates a "tombstone." What the tombstone includes depends on how you delete it:
If you make a 
DELETE
 call, the tombstone includes the 
_id
, 
_rev
, and 
_deleted
 fields.
If you delete by updating the document with a 
_deleted: true
 field and add a 
PUT
 or 
POST
 request to it, the tombstone includes what you set in
the document body. This practice can be useful in some 
circumstances, for example, when recording why a document was deleted in its tombstone.
For more information, see 
Simple removal of "tombstone" documents
.
When is a deleted document removed?
Compaction runs automatically and periodically removes old revisions (deleted or otherwise) from the database, by writing out only "leaf" revisions to a
new file. IBM Cloudant keeps a history of 
_id
 and 
_rev
 to enable replication, but not old document bodies.
IBM Cloudant doesn't guarantee that a database is compacted in a specific time. Compaction is done as a background process across the storage tier.
Databases are always being compacted. It isn't guaranteed that the data compacted is the data 
that you deleted or changed.
IBM Cloudant is accepting the 
right to be forgotten
 requests through the 
IBM Data Privacy Office (DPO)
. When a 
right to be forgotten
 request is 
made from
the IBM DPO, IBM Cloudant verifies the request, explicitly triggers database compaction, and verifies that compaction occurred. At the end of this process,
the only version of the document is its tombstone ( 
_id
, 
_rev
, 
_deleted
, and any fields your application includes there).
 Tip: 
IBM Cloudant doesn't expose the CouchDB compaction API.
Cloudant
   
26Removal of tombstones
IBM Cloudant can completely remove all references and data for a document when required. This task is an operator-managed process called purging.
Before you request that documents be purged, it's important to understand that purged documents 
cannot be recovered
 by IBM Cloudant once the process
is complete.
In the context of GDPR, purging is only required if PI is used in a document ID. It's a bad idea for an 
_id
 to store PI for lots of reasons, but a handful of
semi-valid use cases exist (for example, a unique email). If possible, 
encrypt or pseudonymize data so it's opaque to IBM Cloudant.
If a document needs removal through a 
right to be forgotten
 request, follow these steps:
1
. 
File a request with the 
IBM DPO
 to request purging of specific document 
_id
 values along with the reason.
2
. 
On receipt of a formal request by the IBM DPO, IBM Cloudant operations verifies the request to confirm the 
id
 contains PI. IBM Cloudant doesn't
purge data that doesn't have PI in the 
_id
.
3
. 
IBM Cloudant triggers the purging action to permanently remove the requested data.
This process is only to be used for emergency deletion requests (for example, 
right to be forgotten
) and must not be relied upon long term. If your
application is intentionally using PI in document IDs, then it must be changed to 
either pseudonymize that PI, or not use PI in document IDs. You cannot
rely on regular purging by the IBM Cloudant operations team to avoid this situation. Therefore, IBM Cloudant rejects the following purge requests:
1
. 
The request is for regular purging, for example, 
every 30 days
.
2
. 
The request is for over 100 documents.
Even with purge, PI in the 
_id
 field leaks into places you don't want it, such as IBM Cloudant logs, so it must be avoided. IBM Cloudant has a business
reason to keep those logs and doesn't remove log lines that include document 
_id
 values.
What about deleting a database?
Deleting a database adds it to the trash for up to 48 hours. After which time, the database is removed from the file system. The IBM Cloudant team 
does
not
 make back ups of your databases; this task is the 
responsibility of the customer
. You must ensure that all copies of your database are removed from
your system. For more information, see 
IBM Cloudant backup and recovery
.
If you need more help, go to the 
IBM Cloud Support portal
.
 Tip: 
The CouchDB purge API is not supported by IBM Cloudant.
Cloudant
   
27Transaction Engine notice
What is Transaction Engine?
IBM Cloudant has an architecture option, which is underpinned by a Transaction Engine. This architecture aims to provide the best of both non-relational
and relational data stores combining scale, fault tolerance, consistency, security, and 
speed at optimal cost. The Transaction Engine architecture is
compared to the "Classic" architecture for clarity in the documentation. Instances that are provisioned with the 
Standard on Transaction Engine
 plan
are deployed 
by using this architecture, while instances on the 
Lite
 and 
Standard
 plan are deployed on the "Classic" architecture.
 Deprecated: 
The IBM® Cloudant® for IBM Cloud® on Transaction Engine service ends on 1 February 2023. You can no longer create new instances
of IBM Cloudant on Transaction Engine. On 1 February 2023, all instances of IBM Cloudant on Transaction Engine will 
be permanently disabled
and deprovisioned. Users of existing instances need to migrate from the service before the end of service date. You can find guidance on migrating
from IBM Cloudant on Transaction Engine to IBM Cloudant Standard here: 
Migrating from TXE
.
Cloudant
   
28Service Changes and Deprecations for IBM Cloudant
You can see the deprecations for IBM® Cloudant® for IBM Cloud® here.
IBM Cloudant Deprecation of 
_show
, 
_list
, 
_update
, 
_rewrite
 functions
Details
Notice that the following Cloudant features are deprecated:
show functions - used to modify the format of the response when requesting a single document from the database.
list functions - similar to show functions, but applied to the output of MapReduce views.
rewrite functions - used to embody routing logic in CouchApps.
update functions - used to carry out business logic within the database e.g. adding a timestamp to all document writes.
These four features are already deprecated in Apache CouchDB and scheduled to be removed from the code in Apache CouchDB 4.0. None of these
features are modelled in our Cloudant SDKs.
We may completely remove the features in the future, but will leave them operable for the time being to give customers time to modify their applications.
As deprecated features, they will not appear in our documentation, their use is not recommended 
and they will not be supported by our Support team.
Alternatives to these functions can be found on the Cloudant blog 
here
.
IBM Cloudant Remove replicator endpoint proxy support
Details
Replicator endpoint proxy support is removed. Replication jobs with 
proxy
, 
source_proxy
 or 
target_proxy
 fields set will fail with an error.
IBM Cloudant Deprecation of Cloudant instances that are created as Cloud Foundry
service instances
Details
Due to the end of the Cloud Foundry service, IBM Cloudant instances that are created as Cloud Foundry service instances are being deprecated and must
be migrated to an IBM Cloud 
resource group
.
Migration to a resource group provides the added capability to use 
IBM Cloud IAM
 to control access. When migrating the Cloudant instance, you can
choose which 
of your IBM Cloud resource groups to migrate it to. For example, you might have one resource group for production and a different one for
Dev/Test.
Should IBM be required to migrate a Cloudant instance to a resource group, it will be migrated to the default resource group for the IBM Cloud account.
The assignment of the Cloudant instance to the default resource group cannot be changed 
later.
Deadline for Lite plan instances has been extended from 1 August 2023 to 18 September 2023: Lite plan instances that are not migrated before 18
September 2023 will be disabled for 30 days and deleted on 18 October 2023.
How do I know if my instances use Cloud Foundry?
Display the list of Cloudant instances in the IBM Cloud GUI
The presence of the migrate icon after the instance name identifies instances that need to be migrated
How do I migrate the instance to an IBM Cloud resource group?
To complete the migration, follow these 
IBM Cloudant instructions
.
1
. 
Open the 
More actions
 menu.
 Important: 
Although these features are deprecated, they will not be removed from the service yet.
 Important: 
Standard Plan instances that are not migrated before 1 September 2023 will be migrated by IBM.
Cloudant
   
292
. 
Select 
Migrate to a resource group
 to get started.
3
. 
Select a resource group.
4
. 
Click 
Migrate
 and the instance is migrated for you.
5
. 
Since you can migrate only one instance at a time, you can continue migrating eligible instances after you migrate the first one.
The data in the Cloudant instance is not involved in this migration.
 
There is no Cloudant service downtime as a result of this migration.
IBM Cloudant Geospatial notice
What is IBM Cloudant Geospatial?
Data is stored as GeoJSON in the IBM Cloudant database to describe point, line, polygon, multi-point, multi-line, and multi-polygon objects. Each object,
as well as the geographic information, can have optional properties: Metadata about the 
object, which is returned in the search results.
Again, an index is defined as a JavaScript function, and then, queries can be used to ask questions of your collection of geographic features. For example,
find me the nearest object to this point; find objects within this polygon; find objects 
along this path; or find objects that intersect with this object.
To summarize, IBM Cloudant Geo is something unique to the IBM Cloudant service and is used to perform advanced geospatial queries against your
databases of GeoJSON objects. It cannot be combined with other index types. It is only of use to 
Geographic Information Systems or use-cases that have a
purely geographic purpose.
What is changing?
As of 1 February 2023, the following conditions apply:
Users cannot query 
/$DATABASE/_design/$DDOCS/_geo
 endpoints. Requests to those endpoints return a 
404 Not Found
 response.
Users can define indexes by using the 
st_indexes
 keyword in design documents, but those indexes are ignored by the service. This practice
ensures that existing design documents can be updated, and replications that contain geospatial 
indexes do not fail. Existing Geo indexes are
deleted, and customers are no longer billed for the space they consume.
IBM Cloud® support no longer answers questions or assists with issues that are related to the Geospatial feature of the IBM Cloudant service.
Alternatives to geospatial
Many simple geospatial queries can be done without using the Geospatial capability that was removed from the IBM Cloudant service. These alternatives
are described in this 
IBM Cloudant blog post
.
IBM Cloudant dbcopy feature removal
As of 1 October 2023, IBM Cloudant's dbcopy feature (also known as "Chained MapReduce" or "view chaining") will cease to function. The dbcopy feature
was 
removed from our documentation in 2016
 
and 
since November 2022, new users cannot configure dbcopy
. 
Starting 1 October 2023, the dbcopy
feature will be removed from the IBM Cloudant service entirely.
What is dbcopy?
IBM Cloudant allows materialized MapReduce views to be created on a database - a secondary index structure that contains user-defined keys and values.
MapReduce views exist and are queried in the same path as the primary database.
With the "dbcopy" feature configured, the MapReduce data is instead written to a second database. The second database then contains the key/value pairs
that would usually be found in the materialized view of a normal MapReduce view. 
The dbcopy feature was used to allow view data to be "chained" (for
example, the creation of views of views) or to provide a primitive 
join
 functionality between documents.
What happens after the feature is removed?
The primary database continues to function as normal, but any MapReduce indexes with dbcopy configured no longer write data to the secondary
database. The secondary database still exists, but it cannot be updated when the primary data changes.
How do I know whether my MapReduce views use dbcopy?
MapReduce index definitions are stored in a database's 
design documents
. These MapReduce index definitions contain JavaScript that programmatically
 Deprecated: 
Support for the IBM Cloudant Geospatial capability ends on 31 January 2023. In many cases, existing applications fail if changes are
not made to address the removal of this functionality before the end of support.
Cloudant
   
30decides what 
data from the document makes it into the view, as shown in the following example:
{
  
"_id"
: 
"_design/myview"
,
  
"views"
: {
    
"view"
: {
      
"map"
: 
"function(doc) { emit(doc.date, doc.price) }"
,
      
"dbcopy"
: 
"another_database"
    }
  }
}
If a view definition contains an attribute that is called 
dbcopy
, as is the case with the previous example design document, then the dbcopy feature 
is in
use and is affected by the feature's removal
.
Alternatives to dbcopy
No alternative to the dbcopy feature exists. Simply removing the "dbcopy" attribute from a design document instructs IBM Cloudant to build a normal
MapReduce view. This view contains the same data that was being copied to the secondary 
database, for example:
{
  
"_id"
: 
"_design/myview"
,
  
"views"
: {
    
"view"
: {
      
"map"
: 
"function(doc) { emit(doc.date, doc.price) }"
    }
  }
}
If you are concerned about the removal of the dbcopy feature, you can open a support ticket and ask to consult with our Client Architecture team.
IBM Cloudant Replications no longer support HTTP
As of 1 October 2023, the replicator for IBM Cloudant no longer supports the HTTP protocol – it supports only the HTTPS protocol to ensure that customer
data is always encrypted in flight.
What is replication?
IBM Cloudant replications allow you to copy one database's changes to another IBM Cloudant database. This database is in the same IBM Cloudant
instance or in another IBM Cloudant instance on the other side of the world. IBM Cloudant also replicates 
to and from Apache CouchDB and PouchDB
databases on the public internet.
What happens after HTTP support is removed?
Following this change, a replication that is configured with the 
http://
 protocol fails permanently. The replication job is not retried. Any replications
using the 
https://
 protocol are unaffected.
How do I know whether my replications use HTTP?
Replication job definitions are stored in documents in an IBM Cloudant account's 
_replicator
 database, for example:
{
  
"_id"
: 
"myreplicationjob"
,
  
"source"
: 
"https://mycloudantservice.cloudant.com/products"
,
  
"target"
: 
"http://myselfhostedcouchdb.mydomain.com/products"
}
If either the 
source
 or 
target
 URLs contain an 
http://
 prefix, then 
the replication job is affected
 and action must be taken to ensure the replication
 Note: 
The dbcopy key was removed, so this view becomes a normal MapReduce view that you can 
query by using the IBM Cloudant API
.
 Important: 
These changes only affect replications leaving IBM Cloudant. Customers who only replicate between Cloudant instances have no
action to take.
Cloudant
   
31runs.
How do I avoid being affected?
If a self-hosted CouchDB service supports HTTPS, then change the replication definition to contain an 
https://
 prefix, as shown in the following
example:
{
  
"_id"
: 
"myreplicationjob"
,
  
"source"
: 
"https://mycloudantservice.cloudant.com/products"
,
  
"target"
: 
"https://myselfhostedcouchdb.mydomain.com/products"
}
IBM Cloudant restarts the replication from where the old replication job stopped.
If a self-hosted CouchDB service does _not* support HTTPS, CouchDB can mediate replication jobs instead of IBM Cloudant. For example, stop the
replication job that runs on the IBM Cloudant side and set up a replication job on a self-hosted 
Apache CouchDB service to "pull" the data from IBM
Cloudant.
IBM Cloudant supports only 
https://
 traffic, so if IBM Cloudant is to be the 
source
 or 
target
 in a self-hosted replication definition, it must be
configured with an 
https://
 prefix.
Cloudant
   
32Release notes for IBM Cloudant Classic
Use these release notes to learn about the most recent updates to IBM® Cloudant® for IBM Cloud® that are grouped by date and build number.
July 2024
Upcoming changes
The following changes are planned for the next release:
Welcome message
The CouchDB version in the welcome message will be updated from 
major.minor.patch
 to 
major.minor.patch+cloudant
, eg:
3.3.3+cloudant
. Cloudant applies its own customizations, extensions, and security 
fixes atop upstream CouchDB, therefore the CouchDB version
number could be considered only a reference for compatibility. To make this distinction clear, the 
+cloudant
 suffix was introduced.
June 2024
10 June 2024
The following changes were made in build 8513:
IAM auth
JSON web tokens (JWT) added the 
exp
 claim to ensure that user tokens are considered invalid once they expire.
Replicator
Fix replicator session plugin to consider only 
Set-Cookie
 headers with 
AuthSession
 set and ignore others.
5 June 2024
The following changes were made in build 8511:
IAM auth
Refresh access tokens when credentials change. Previously, an access token was allowed to expire before obtaining a new one with the new
credentials.
Runtime environment
Upgrade to the latest Erlang/OTP 25 release.
Add QuickJS as a Javascript engine option.
April 2024
26 April 2024
The following changes were made in build 8510:
IAM auth
Align with the latest Cloud Resource Name (CRN) authentication requirements. Prior to this change, database names shorter than 4 characters or
containing some non-alpha-numeric characters were incorrectly prohibited from working with IAM 
auth.
Mango
Cloudant
   
33Fix a race condition that resulted in some query response execution stats incorrectly reporting zero for 
total_keys_examined
. See
https://github.com/apache/couchdb/issues/4560
 
for more details.
Replicator
Fix case clause error in replicator response. For more information, see 
Advanced replication
.
Runtime environment
Upgrade to the latest 
Erlang/OTP 25.3.2.11
 release.
March 2024
25 March 2024
The following changes were made in build 8495:
Optimization
Added compatibility for OTP 25 and improved performance.
20 March 2024
Several updates were made to 
Service Changes & Deprecations
 - removing TXE notification; adding previously announced deprecation of 
_show
, 
_list
,
_update
, 
_rewrite
 functions; removing 
_find
 API accounting notice.
8 March 2024
List of IBM Cloudant instances hosted on a dedicated environment
The IBM Cloud Console GUI for IBM Cloudant instances on dedicated hardware plan now shows the list of instances hosted on the dedicated
environment.
6 March 2024
The following changes were made in build 8490:
Runtime environment
Upgrade runtime environment back to Erlang/OTP 25 after addressing the related production issues.
February 2024
12 February 2024
The following changes were made in build 8472:
Indexes
In rare cases, background index updates for specific indexes would fail until a database node was restarted. After a node restart, the node would
immediately start updating these indexes. If this generated a lot of indexing activity, customer 
requests involving this node would see degraded
performance during that activity. This release fixes the issue with background indexing failures. For more information, see 
Cloudant Query
.
Replication
Improve performance when updating replication documents.
Cloudant
   
34Fix replication delays caused by conflicting jobs during internal data optimization. For more information, see 
Replication
.
Runtime environment
Downgrade runtime environment to Erlang/OTP 24.
January 2024
10 January 2024
The following changes were made in build 8469:
Runtime environment
Upgrade to Erlang/OTP-25.3.2.8.
December 2023
04 December 2023
The following changes were made in build 8462:
_active_tasks
Optimize 
_active_tasks
 to better handle heavy workloads.
Indexing
Improve robustness of index compaction.
Mango
Introduce 
$beginsWith
 operator.
Runtime environment
Downgrade runtime environment to Erlang/OTP 24.
Security
Allow stronger on-disk password hashes without impacting database request performance.
November 2023
17 November 2023
IBM Cloudant Dashboard
Update the Cloudant Query explain page with a user-friendly view of the JSON output. The parsed view better explains how indexes are chosen to
help the user create more efficient queries.
October 2023
24 October 2023
The following changes were made in build 8452:
Cloudant
   
35Runtime environment
Upgrade to the latest Erlang/OTP 25 release.
18 October 2023
The following changes were made in build 8451:
Security
Scrub sensitive headers from JSON requests.
13 October 2023
The following changes were made in build 8448:
_db_updates
 endpoint
Remove 
_db_updates
 endpoint support.
Mango query
Correct 
_explain
 API to always return an array for 
fields
. Return 
[]
 instead of 
"all_fields"
 if the 
fields
 parameter was unset.
Prevent occasional duplication of paginated 
text
 results.
Legacy auth
Send compatible AuthSession cookie when possible.
Replicator
Fix 
badrecord
 error when cancelling transient replication job.
Replace 
kaboom
 with 
open_doc_revs_failed
 error.
Use HTTP rules for hostname verification.
September 2023
14 September 2023
The following changes were made in build 8442:
_changes
 feed
Improve emitted changes feed sequence after a split.
Return the correct number of pending changes when 
descending=true
.
Design documents
_design_docs/queries
 / 
_local_docs/queries
 with parameter 
keys
 will return only design / local documents respectively.
Legacy auth
Send a session cookie after successful basic authentication to migrate users to a strong password hashing scheme without impacting performance
for each request.
Mango query
Cloudant
   
36Remove duplicate elements from 
indexable_fields
 results.
Correct the 
_explain
 endpoint 
r
 response field content from a byte array to an integer to match the declared API type.
Rename the 
_explain
 endpoint response 
covered
 field name to 
covering
 to match correctly the Apache CouchDB name.
Replicator
Fix undefined range in 
mem3_rep
 purge replication logic.
Crash replication jobs on unexpected 4XX errors.
Add 
CouchDB-Replicator/...
 user agent to replicator 
/_session
 requests.
Search
Correct the representation of empty faceted results from 
0
 to 
{}
 to match the declared API type.
See 
PR
.
Shard splitting
Allow resumption of failed jobs, and make 
timeout
 configurable.
Optimization
Stop the client process and clean up if the client disconnects.
August 2023
30 August 2023
The following changes were made in build 8435:
_all_dbs
 endpoint
Restrict 
_all_dbs
 to accept only binary 
start_key
/
end_key
 parameters.
_replicate
 endpoint
Authentication is required to access the 
_replicate
 endpoint.
Mango query
Improve error messages in case of invalid field errors.
Replicator
Remove replicator endpoint proxy support.
July 2023
21 July 2023
The following changes were made in build 8430:
Attachments
Fix multipart parser "attachment longer than expected" error.
Remove Content-MD5 header support.
Replace MD5 with xxHash in ETag generation.
Mango query
Return correct 
keys_examined
 value in 
execution_stats
 field.
Cloudant
   
37Return correct 
keys_examined
 value in 
execution_stats
 field.
Improve error messages of the 
_index
 endpoint.
Optimization
Speed up internal replicator.
Optimize low-level file name calculations.
Use a faster sets implementation available since OTP 24.
Replicator
Handle replicator instance start time during upgrades better.
Resharding
Fix purge infos replicating to the wrong shards during shard splitting.
June 2023
05 June 2023
The following changes were made in build 8413:
_all_docs
 endpoint
Do not return documents for non-string 
key
 parameter.
Filter view functions
Optimize by not unnecessarily re-compiling filter view functions.
Geospatial
Remove geospatial functionality.
Javascript
Treat javascript internal errors (such as Out of Memory) as fatal.
_local_docs
 endpoint
Hide internal checkpoint documents by default in the 
_local_docs
 response.
Mango query
Return correct documents for queries with 
$regex
 and text indexes.
Optimize queries using keys-only covering indexes.
Add new covered Boolean field to 
_explain
 endpoint to indicate whether query is covered by an index.
Return 405 instead of 500 for invalid path under 
_index
 endpoint.
Partitioned database queries
Fix permissions required for partitioned 
_find
 and 
_explain
 endpoints.
Runtime environment
Upgrade to the latest Erlang/OTP 24 release.
View query
Treat single element 
keys
 parameter same as 
key
.
Cloudant
   
38April 2023
03 April 2023
IBM Cloudant Dashboard
Update Dashboard to use Carbon 11's color theme.
The following changes were made in build 8382:
Indexing
Prevent 
couch_index_server
 from crashing under load.
Runtime environment
Upgrade the runtime environment to latest Erlang/OTP 24 point release.
March 2023
14 March 2023
The following changes were made in build 8373:
_changes
 endpoint
Enforce document ids 
_changes
 filter optimization limit.
Compaction
Active database size now decreases when users delete documents.
Indexing
Enforce partition index count limits for (noninternally) replicated documents.
Optimize process pool management (fixes CVE-2023-26268).
Query
Optimize by pushing down field selectors to shards.
Replication
Replace auto-inserted VDU with BDU.
Constrain protocol types and socket options.
Upload design docs individually when you replicate with 
bulk_get
.
Runtime environment
Upgrade the runtime environment to Erlang/OTP 24 point release patched with 
alias-cleanup-fix
.
Views
Disable 
stable
 and 
stale
 parameters in POST requests to partitioned views.
January 2023
11 January 2023
Cloudant
   
39The following changes were made in build 8349:
IAM trusted profiles
Fix bug in IAM trusted profiles.
Runtime environment
Upgrade runtime environment to Erlang/OTP 24.
November 2022
17 November 2022
The following changes were made in build 8341:
_bulk_get
 endpoint
Optimize 
_bulk_get
 endpoint.
_changes
 endpoint
Fix 
eventsource
 formatted feed.
Remove support for the long-deprecated change sequence format.
dbcopy
Prevent further use of 
dbcopy
 feature for all but current users.
Compaction
Fix smoosh 
get_priority/2
 case clause.
Replication
Use the 
_bulk_get
 endpoint for replication if available.
Return a string for the default start sequence from 
_scheduler/{jobs,docs}
 endpoints.
_session
 endpoint
Return error when POSTing to 
/_session
 with content type other than 
application/x-www-form-urlencoded
 or 
application/json
.
Runtime environment
Upgrade runtime environment to Erlang/OTP 23 patch release.
September 2022
21 September 2022
The following changes were made in build 8336:
Runtime environment
Upgrade runtime environment to Erlang/OTP 23 patch release.
View collation
Upgrade view collator to libicu 67.1.
Cloudant
   
40August 2022
5 August 2022
The following changes were made in build 8335:
Bulk docs
Improve performance for 
_bulk_docs
 endpoint.
Compaction
Fix bugs in automatic compaction.
Fix race between database deletion and compaction.
Document updates
Improve reliability of document updates during heavy load.
Return a 400 response for 
new_edits=false
 document update without revisions.
Replicator
Introduce numerous performance improvements.
June 2022
10 June 2022
The following changes were made in build 8310:
All databases
Fix 
skip
 and 
limit
 parameters for 
_all_dbs
 and 
_dbs_info
 endpoints.
Attachments
Wait until attachments are uploaded before response to client.
Bulk docs
Return 500 errors if timeouts occur when documents are bulk loaded.
Compaction
Retain compactor state across node reboots.
IAM auth
Retry 
authz
 endpoint on failure.
Indexes
Prevent creation of indexes with empty 
name
 or 
ddoc
 fields.
Improve index building during shard splitting.
Replicator
Improve replicator stability during timeouts.
May 2022
Cloudant
   
4125 May 2022
Virtual Private Endpoints (VPE)
VPE can now be created for IBM Cloudant instances on dedicated hardware.
13 May 2022
The following changes were made in build 8299:
Runtime environment
Upgrade runtime environment to Erlang/OTP 23 with fix for memory leak.
Replicator
Fix 
function_clause
 error for replicated changes with a target VDU.
April 2022
14 April 2022
The following changes were made in build 8287:
Runtime environment
Downgrade runtime environment to Erlang/OTP 20.
March 2022
24 March 2022
The following changes were made in build 8278:
IAM auth
Improve compatibility during upgrades.
Document updates and compaction
Improve efficiency of updating and compacting conflicted documents.
11 March 2022
The following changes were made in build 8269:
Runtime environment
Upgrade runtime environment to Erlang/OTP 23.
04 March 2022
The following changes were made in build 8266:
Cloudant
   
42Bulk docs
Return 400 Bad Request error for 
_bulk_docs
 with 
new_edits:false
 and without 
_rev
. Previously returned 500 error.
Fix bug where Validate Document Update function interacts with 
new_edits:false
 setting.
Indexing
Improve scalability by sharding the index server.
Replicator
Set 
instance_start_time
 to the creation time of the database to restore the ability for the replicator to detect a database recreation event during a
replication.
Search
Expose index signature in the 
_search_info
 endpoint response.
Security
Always send all the cookie attributes whenever we send a cookie. Only the value of AuthSession varies.
Views
Track ICU collator version that is used to build the view and expose this information in existing endpoints.
Exposes list of collator versions in 
_design/*/_info
 endpoint response.
The opaque collator version in 
_node/*/_versions
 endpoint response.
January 2022
28 January 2022
Switch 
Legacy Credentials and IAM
 to 
IAM only
It is now possible to switch authentication methods from 
Legacy Credentials and IAM
 to 
IAM only
 by using the IBM Cloud console.
December 2021
03 December 2021
IBM Cloud Monitoring integration
Metrics are now available in the Frankfurt region.
November 2021
01 November 2021
The following changes were made in build 8243:
Audit messages
Order customer supplied fields last in audit messages.
Changes feed
Reduce changes feed rewinds when nodes are down or shards are moved.
Cloudant
   
43View collation
Fix reduce view collation results for Unicode equivalent keys.
October 2021
01 October 2021
The following changes were made in build 8238:
Changes feed
Use shards moved from other nodes to help prevent changes feed rewind.
Error message
Reduce frequency of 
No DB shards could be opened
 error message.
Shards with purge sequences
Fix splitting shards with large purge sequences.
View results
Fix view results with 
limit=0
 and 
sorted=false
.
Sort view results
Properly sort view results with 
descending=true
 when a key list is provided.
Row aggregation
Stabilize view merge row aggregation.
September 2021
1 September 2021
The following changes were made in build 8220.
Changes feed rewinds
Avoid changes feed rewinds after shard moves.
Response code
Fix response code for attachment deletion with wrong revision.
Indexes
Ensure that indexes are correctly closed.
August 2021
1 August 2021
The following changes were made in build 8202:
IAM trusted profiles
Support IAM trusted profiles.
Cloudant
   
4415 August 2021
The following changes were made in build 8201:
Improvements
Internal bug fixes.
June 2021
1 June 2021
The following changes were made in build 8194:
API task filtering
Bug fixes, including account API key task filtering.
Replication support
Support replication 
basic auth credentials in auth object
.
Basic auth credentials
No longer display basic auth credentials (for example, 
username:*****
) in the output of these endpoints:
_scheduler/jobs
_scheduler/docs
_active_tasks
April 2021
1 April 2021
The following changes were made in build 8192:
New! Fair share replicator
Added Fair share replicator. For more information, see 
Fair Share Replication Scheduler Implementation
.
Improvements
Internal bug fixes.
March 2021
15 March 2021
The following changes were made in build 8182:
Improvements
Internal bug fixes.
Caching
Apply caching to account-local 
_users
 databases.
Error condition
Cloudant
   
45Treat 408 as a retryable error condition for replicator.
Compressed requests
Allow compressed (
gzipped
) requests to 
/_session
 endpoint.
/_active_tasks
 endpoint
Show process status in 
/_active_tasks
 endpoint.
/{DB}/_changes
 endpoint
Validate JSON payload on 
POST
 to 
/{DB}/_changes
 endpoint.
December 2020
1 December 2020
The following changes were made in build 8169:
New! Mango query operator
Introduce the Mango query operator, 
$keyMapMatch
 that offers the ability to make queries on the keys of a map.
Improvements
Internal bug fixes.
Database reporting
Report the database that was used for authentication for a 
GET /_session
 request, provided it is configured.
September 2020
1 September 2020
The following changes were made in build 8162:
Improvements
Internal bug fixes.
Drilldown
 parameters
Drilldown
 parameters for text index searches can now be specified as a list of lists, which gives you the ability to avoid having to define it
redundantly in a single query. Some languages don't have this facility.
couch_index
 server
The 
couch_index
 server doesn't crash and log errors in the following cases: If a design document is deleted while that index is building, or when a
design document is added immediately after database creation.
Invalid parameters
IBM Cloudant now checks for and reports invalid parameters on database creation.
July 2020
1 July 2020
The following changes were made in build 8158:
Improvements
Cloudant
   
46Internal bug fixes.
May 2020
15 May 2020
The following changes were made in build 8153:
Improvements
Internal bug fixes.
April 2020
1 April 2020
The following changes were made in build 8152:
Improvements
Internal bug fixes.
March 2020
15 March 2020
The following changes were made in build 8142:
New! Endpoints
New endpoints were added, so you can post multiple queries: 
POST /{db}/_all_docs/queries
 and 
POST /{db}/_design_docs/queries
.
Multiple queries
The ability to submit multiple queries against a view by using the 
POST
 to 
/{db}/_design/{ddoc}/_view/{view}
 with the 
?queries
 option was
replaced by the new 
queries
 endpoint. The same 
is true of the 
_all_docs
 and 
_design_docs
 endpoints. Specify a 
keys
 object when you 
POST
to these endpoints.
disk_size
 and 
data_size
 fields
The 
disk_size
 and 
data_size
 fields were retired from the database information object that is returned by 
GET /{db}
.
/{db}/_changes
 feed
The 
/{db}/_changes
 feed immediately returns headers now, even when no changes are available. This process prevents client's from becoming
blocked.
Negative and noninteger heartbeat values
Negative and noninteger heartbeat values now return a 
400 Bad Request
 response status code.
Separate proxies
Allow specifying separate proxies for both the source and target in a replication by using 
source_proxy
 and 
target_proxy
 keys.
POST
 view function
The 
POST
 view function now supports identical parameters and behavior as specified in the 
/{db}/_design/{ddoc}/_view/{view}
,
/{db}/_all_docs
, and 
/{db}/_design_docs
 endpoints. You can supply 
query string parameters as keys in a JSON object in the body of the 
POST
request.
Replication errors
Cloudant
   
47Replication 
"info"
 errors are now JSON objects. Previously, they were strings.
Replication support
A compatibility change was made to support replication with future databases that contain per-document access control fields.
Warning message
Add a warning to the 
_find
 endpoint if multiple document scans were required to generate a result.
_find
 endpoint error
Fix a bug in the 
_find
 endpoint whereby an error would be returned if a document matched by a text index was deleted while the query was being
processed.
January 2020
15 January 2020
The following changes were made in build 8126:
Improvements
Internal bug fixes.
Replication error reports
Improvements to replication error reporting - instead of a function_clause, human-readable markers are returned, for example, 
bulk_docs_failed
.
Stack traces are no longer included.
Replication job statistics
Replication job statistics, such as 
docs_read
, 
docs_written
, and 
doc_write_failures
 are preserved when replication jobs restart.
Replication jobs
Replication jobs to a target endpoint by using IAM Writer permissions no longer crash and continuously restart when they write design documents.
Instead, the 
doc_write_failures
 statistic is incremented for each failed design 
document write. This behavior is consistent with replicating by
using the legacy API-key-based authentication.
November 2019
1 November 2019
The following changes were made in build 8111:
Improvements
Internal bug fixes.
Replication statistics
The 
_scheduler/docs
 endpoint now includes more detailed replication statistics to match 
_active_tasks
 output. It also includes details on
replications that started with 
_replicate
.
Replication error
Fix an instance where the replicator failed a replication but the error was recoverable.
Empty payload
Fix a bug introduced in recent builds where sending an empty payload to 
_bulk_docs
 would result in a 400 response status code rather than
accepting the no-op operation.
October 2019
Cloudant
   
4821 October 2019
Multiple restrictions employed for performance gains
IBM released exciting new capabilities for IBM Cloudant that are available now. IBM Cloudant documented the deprecation of some functionality,
and also, new restrictions for other processes. A communication was released that details the 
exact timeline when these restrictions go into effect. If
you use any of the following functions or are concerned about how to make the necessary application changes, reach out to support by email. The
following functions are affected 
by this deprecation:
Remove the 
offset
 field from the response body of an 
all_docs
 request. The IBM Cloudant team recommends that you use paging with
start_key
 / 
end_key
 and 
limit
.
The 
_sorted
 field has no functional effect because all responses are sorted automatically.
Duration of operations has a 5-second limit. Transactions lasting more than 5 seconds fail.
Limitations on keys (10 KB) and values (100 KB) that are emitted from a map function are shown in the following list:
The sum of all keys that are emitted for a document cannot exceed 100 KB.
Emitted keys cannot exceed 10 KB.
Values cannot exceed 100 KB.
In rare cases, the number of key-value pairs that are emitted for a map function can affect database performance or violate IBM
Cloudant rules. For example, the number of key-value pairs might lead to a transaction either exceeding 
10 MB, which isn’t allowed, or
exceeding 5 MB, which impacts the performance of the database. In this situation, IBM Cloudant returns an error.
The 
stable = true
 option is no longer supported, and the 
stale = "ok"
 option is converted to 
update = false
.
15 October 2019
The following changes were made in build 8106:
Improvements
Internal bug fixes.
1 October 2019
The following changes were made in build 8103:
X-Cloudant-Action
 HTTP response header
New 
X-Cloudant-Action
 HTTP response header that returns the IBM Cloud® IAM actions that are associated with a request.
Search requests
Previously, search requests would return a 
400
 status code both on a bad request and on internal server errors. Now, internal server errors correctly
return a 
500
 response status code.
September 2019
18 September 2019
Replaced deprecated database information fields
Calls to 
GET /{db}
 were replaced by the following fields:
Old Field
New Field
Cloudant
   
49Table 1. Database information fields
data_size
sizes.active
disk_size
sizes.file
other.data_size
sizes.external
Calls to 
GET /{db}/_design/{ddoc}/_info
 were replaced by the following fields:
Table 2. Design doc information fields
Old Field
New Field
data_size
sizes.external
disk_size
sizes.file
June 2019
1 June 2019
The following changes were made in build 8076:
Improvements
Internal bug fixes.
Stability
Stability improvements.
May 2019
15 May 2019
The following changes were made in build 8070:
Improvements
Internal bug fixes.
1 May 2019
The following changes were made in build 8062:
Improvements
Internal bug fixes.
April 2019
15 April 2019
Cloudant
   
50The following changes were made in build 8058:
ibrowse
 HTTP client
Fixed bug in 
ibrowse
 HTTP client that leaves dead process IDs in the connection pool, and in some cases, caused persistent IAM-based replication
failures.
1 April 2019
The following changes were made in build 8052:
partitioned_indexes
 field
Accessing the database information endpoint (
/db/
) for a partitioned database now includes information about the contained partitioned indexes.
The new field, 
partitioned_indexes
, contains the following information:
The current number of partitioned indexes in the database (
count
).
A breakdown of those indexes by type (
indexes
).
The maximum partitioned indexes allowed for this database (
limit
).
March 2019
15 March 2019
The following changes were made in build 8048:
Improvements
Internal bug fixes.
1 March 2019
The following changes were made in build 8038:
Partition queries
Allow 
POST
 when you search 
partition queries
.
February 2019
15 February 2019
The 
stale
 option
The 
stale
 option is deprecated and is replaced by 
stable
 and 
update
, which allow controlling the two orthogonal behaviors that are caused by
stale
 separately.
stable
 value
Equivalent by using 
stable
 and 
update
false
stable=false
, 
update=true
Cloudant
   
51Table 3. Stale option replacement
ok
stable=true
, 
update=false
update_after
stable=true
, 
update=lazy
1 February 2019
The following changes were made in build 7681:
Partition query
Partition query bug fixes.
January 2019
15 January 2019
The following changes were made in build 7668:
New! Partition query
This build introduces a new feature, 
partition query
.
limit
Allow 
limit
 when you use 
POST
 for search.
View requests
Previously, view requests that use a 
limit
 parameter greater than 268435456 would have the limit that is silently reduced to 268435456. Now,
requests with the 
limit
 parameter greater than 268435456 are rejected 
with a 
400 Bad Request
 error.
1 January 2019
The following changes were made in build 7631:
Improvements
Internal changes and bug fixes.
December 2018
1 December 2018
The following changes were made in build 7544:
Replicator statistics
Fixed a problem where the replicator would sometimes reset statistics during replications. The reset would affect values in the 
replication status
information
. See 
PR
.
IBM Cloudant Query and 
_find
 request
Fixed an issue with IBM Cloudant Query. After you delete a document, if you issue a 
_find
 request to a text index with 
update=false
, it might
return a 
500
 response. See 
PR
.
Cloudant
   
52_bulk_get
You can now use 
multipart/mixed
 and 
multipart/related
 when you use 
_bulk_get
. See 
PR
.
_design_docs
 handler
Fix a bug with total row count in the 
_design_docs
 handler. See 
PR
.
Replication filters
Optimizations to the 
_doc_id
 and 
_design_docs
 replication filters. See 
issue
.
Index jobs
Fix a regression where long-running index jobs can fail.
November 2018
4 November 18
The following changes were made in build 7410:
Improvements
Internal changes and bug fixes.
1 November 2018
The following changes were made in build 7426:
Improvements
Internal bug fixes to data compression, search, and core database components.
Audit logs
Include 
CRN
 in audit logs.
Replicator
Replicator stability improvements.
q
 parameter
Improve validation of 
q
 parameter on database creation. See 
COUCHDB-1582
.
_bulk_get
 endpoint
Fix error in 
_bulk_get
 endpoint for the 
_users
 database. See 
COUCHDB-1650
.
JavaScript URL rewrites
Fix JavaScript URL rewrites hanging on 
POST
 or 
PUT
 requests. See 
COUCHDB-1612
.
IBM Cloudant Query and invalid 
reduce
 functions
Fix invalid 
reduce
 functions in IBM Cloudant Query indexes that prevent indexing. See 
COUCHDB-1666
.
October 2018
11 October 2018
The following changes were made in build 7304:
Improvements
This build is identical to build 7302 except that the build is on Erlang 17.5 instead of Erlang 20.
Cloudant
   
53September 2018
25 September 2018
The following changes were made in build 7302:
Mango Query
Improve Mango Query so that mixed clusters return correct results during upgrades.
Downgrade function
Add a downgrade function to support future cluster purge releases.
Search blocklist
Improve search blocklist.
18 September 2018
The following changes were made in build 7276:
Improvements
Add a filter for databases that are being opened asynchronously to prevent exceptions when 
couch_server
 terminates.
Concurrency error
Fix 
couch_server
 concurrency error.
Configuration option
Add a configuration option to disable off-heap messages.
13 September 2018
TLS 1.3 connection support
From today, IBM Cloudant supports TLS 1.3 connections to IBM Cloudant.
IBM Cloudant recommends that you use TLS 1.2 or 1.3 for all access to IBM Cloudant. 
(In June 2019, IBM Cloudant retired the use of older versions
(TLS 1.0 and 1.1) at which point only TLS 1.2+ is supported.)
 Find more information on the 
Security page
.
7 September 2018
The following changes were made in build 7205:
Refactor Mango Query selectors
Refactor Mango Query selectors to reduce the amount of traffic sent between nodes in the cluster.
Document update errors
Expose document update errors on concurrent document updates to client.
render_error
 errors
Fix 
render_error
 errors where the 
req
 object that is passed to the JavaScript list function is set to 
noproc
 Atom.
Cloudant
   
54August 2018
1 August 2018
The following changes were made in build 7138:
Erlang
Upgrade to Erlang OTP 20.
15 August 2018
The following changes were made in build 7137:
Validation of configuration parameters
Improve validation of configuration parameters supplied by administrator.
Compaction
While compaction is running, delete compaction files when database is deleted.
Sandboxing feature
Improve sandboxing features.
Authentication check
Optimize authentication check.
Semantics
Change semantics of status codes for delete database.
conflicts: true
 support
Support 
conflicts: true
 for queries to the 
/{db}/_find
 endpoint.
update_seq
 field
Preserve 
update_seq
 field across view compaction.
July 2018
12 July 2018
The following changes were made in build 7084:
stats
 reducer
Refactor code for 
_stats
 reducer.
Views
Fix active size calculations for views.
couch_key_tree
 algorithm
Rewrite the 
couch_key_tree
 algorithm to reduce its computational complexity and avoid calling stemming when unnecessary.
Allocation strategy
Change the allocation strategy for the message queue for each important process, so it's not stored on the heap of that process.
Internal audit facility
Improvements to internal audit facility.
Constant fields
Cloudant
   
55Any constant fields that are in the selector, and are part of the index. For example, 
{A: {$eq: 10}}
 is inserted into the sort list if they aren't already
included. This method increases the chance that the best index is selected 
for the query, for example, index = 
[A, B]
, sort = 
[B]
, and selector =
{A: 1}
. The sort then becomes 
[A, B]
.
June 2018
29 June 2018
The following changes were made in build 7051:
Forward compatibility clause
Add forward compatibility clause for 
_stats
 disk format change.
Compatibility clause
Add compatibility clause for attachment receiver to facilitate Erlang upgrade.
Audit facility
Improvements to internal audit facility.
12 June 2018
The following changes were made in build 7014:
Query selector
Remove the requirement to cover 
_id
 or 
_rev
 in the query selector in order to use a JSON index that explicitly contains them.
May 2018
29 May 2018
The following changes were made in build 6979:
Audit facility
Improve internal audit facility.
14 May 2018
The following changes were made in build 6919:
New! Action, 
DELETE
Introduce new action, 
DELETE
, on the 
/_iam_session
 endpoint, which invalidates the IAM session cookie.
Improvements
Remove outdated dependencies.
 Tip: 
Only the fields that are in front of the current sort fields in the list are added.
Cloudant
   
56April 2018
26 April 2018
The following changes were made in build 6909:
Improvements
Improve compatibility with IAM.
http
 multipart requests
Fix 
badarg
 error in the module that parses 
http
 multipart requests.
25 April 2018
The following changes were made in build 6900:
New! Support replication
Support replication with IAM.
Validation
Improve validation of password schemes.
State field
In 
_scheduler/docs
, set the value of the state field to 
crashing
 when the last event in the history was a crash.
_design/$DDOC/_rewrite
 and 
_design/$DDOC/_update
Disallow 
_design/$DDOC/_rewrite
 and 
_design/$DDOC/_update
 endpoints with IAM.
17 April 2018
The following changes were made in build 6895:
Pluggable storage engine
Fix a regression that is introduced with pluggable storage engine.
6 April 2018
Replaced 
queries
 parameter
The 
queries
 parameter for performing multiple view queries in a single request is no longer accepted as a URL parameter for 
GET
/{db}/_design/{ddoc}/_view/{view}
 or a request body parameter for 
POST /{db}/_design/{ddoc}/_view/{view}
. 
The parameter was
replaced with the endpoint 
POST /{db}/_design/{ddoc}/_view/{view}/queries
 and is supplied as a 
queries
 request body parameter. You can
also make multiple queries with the following new endpoints:
POST /{db}/_all_docs/queries
POST /{db}/_design_docs/queries
Sending several queries to a view
Sending multiple queries to a view that uses a 
POST
 request to 
/$DATABASE/_design/$DDOC/_view/$VIEWNAME
 is deprecated with 
multi-querying
a MapReduce view
. 
For more information, see the previous deprecation note about replacing the 
queries
 parameter.
Cloudant
   
574 April 2018
The following changes were made in build 6875:
New! Audit facility
Internal audit facility is added to the platform.
IBM Cloudant Query error messages
Improve error messages for IBM Cloudant Query.
March 2018
30 March 2018
The following changes were made in build 6870:
kill
 command
Fix how the 
kill
 command works when you terminate an operating system process.
_changes
 endpoint
Fix 
_changes
 endpoint shard substitution.
Compaction resumption
Fix compaction resumption for terminated compactions.
13 March 2018
The following changes were made in build 6761:
New! 
_dbs_info
 endpoint
Introduce new 
_dbs_info
 endpoint to get information from a list of databases. See 
Get a list of all databases in the instance
.
New! Pluggable storage engine
Add a pluggable storage engine.
Improvement
Update MochiWeb to version 2.17.
Attachments
Ensure deterministic revisions for attachments. See 
COUCHDB-3255
.
chttpd
 multipart
Prevent 
chttpd
 multipart zombie processes.
Unconditional retries
Avoid unconditional retries in replicator's HTTP client.
Session support
Prepare for session support in replicator.
February 2018
15 February 2018
Cloudant
   
58The following changes were made in build 6656:
Query parameters
Update 
_design_docs
 to respect the query parameters that are used by 
_all_docs
. See 
Get design documents
.
COPY
 request
When you send a 
COPY
 request to 
/$DATABASE/docid
 endpoint, IBM Cloudant now decodes the Destination header and creates a new ID without
escaped values.
Replication document
Remove headers from replication document on read.
update_seq
 and 
offset
 parameters
If the 
keys
 parameter is specified and the 
update_seq
 parameter is set to true, the 
update_seq
 and 
offset
 parameters return 
null
 in the
response.
Semantics
Change semantics of status codes for create database.
7 February 2018
Db2 Warehouse on Cloud feature is deprecated
To find alternatives to IBM Cloudant's IBM® Db2® Warehouse on Cloud feature, see the 
data-flow-examples repository
 for tutorials on extracting IBM
Cloudant documents and writing the data to a Db2 Warehouse on Cloud table.
January 2018
10 January 2018
The following changes were made in build 6620:
IBM Cloudant Query and empty 
partial_filter_selector
 field
IBM Cloudant Query falls back to 
selector
 on an empty 
partial_filter_selector
 field.
December 2017
28 December 2017
The following changes were made in build 6600:
IBM Cloudant Query and 
$or
 operations
IBM Cloudant Query fields that are referenced within 
$or
 operations are considered when IBM Cloudant Query determines the usable indexes for a
particular selector.
7 December 2017
The following changes were made in build 6588:
New!
create_target_params
 parameter
Cloudant
   
59A new parameter, 
create_target_params
, was added for you to customize the target database that is created on a new replication. You can now
customize the cluster's default values for the number of shards and replicas to create.
/_scheduler
A request to 
/_scheduler
 without specifying subsections 
docs
 or 
jobs
 now returns a 
Not found
 error.
new_edits
 value
A new error is returned when a 
new_edits
 value is invalid in the 
/db/_bulk_docs
 URL. The error is 
400: Bad request
.
eval()
 and 
Function()
 constructors
For security reasons, by default, the use of 
eval()
 and 
Function()
 constructors is disabled in JavaScript.
Prefer: return=minimal
 header
Added the header 
Prefer: return=minimal
 to return only essential headers. This header reduces the size of the request, which gives a
performance improvement to nonbrowser clients.
Disabled JavaScript constructors
If a user calls the disabled JavaScript constructors, 
eval()
 or 
Function()
, an error message similar to this one is returned, 
Call to 
eval()
 was
blocked by CSP.
 You can fix the problem by replacing 
eval()
 calls with the calls from the 
expr-eval library
.
4 December 2017
Removed support for virtual hosts
IBM Cloudant disabled the virtual host functionality on 4 December 2017. Support for insecure HTTP connections was replaced by HTTPS only. After
you turn off HTTP support, the virtual hosts feature is no longer available since use of virtual 
hosts precludes secure HTTPS connections. Previous
users of the virtual host feature need to make alternative arrangements to present a chosen hostname to your clients from your application and use
HTTPS connections only.
November 2017
7 November 2017
Incompatibility between CouchDB version 1.6 and IBM Cloudant version 2.0.0
An incompatibility exists between the most recent version of IBM Cloudant and CouchDB 1.6-based codebase. In the older version of IBM Cloudant,
if you add a query parameter ("reduce=false") to the request body, the parameter in 
the request body is ignored. However, the parameter in the
request URL is respected. In recent versions of IBM Cloudant, the query parameter ("reduce=false") in the request body isn't ignored.
October 2017
17 October 2017
Query (
_find
 endpoint) improved
IBM Cloudant Query now uses a new method to select an index. Learn more about 
IBM Cloudant Query index selection
.
Index validation
The logic for determining whether a specific index is valid for a query that changed, addressing a bug that might lead to incorrect results.
Text indexes
Queries that use text indexes no longer fail when 
$exists
: 
false
 is used.
Partial indexes
Partial indexes are now supported for both JSON and text indexes. For more information, see 
Creating a partial index
 to learn about the
partial_filter_selector
 
parameter.
Cloudant
   
60Execution statistics
Execution statistics about a query can now be generated. These statistics are enabled by using the 
execution_stats=true
 parameter. For more
information, see 
querying an index by using selector syntax
 
to learn more about 
execution_stats=true
 parameter.
Pagination
Pagination
 is supported by using the bookmark field. Bookmarks are enabled for all index types.
use_index
 field invalid
_find
 now falls back to any valid index if the value specified in the 
use_index
 field is invalid for the current query. When 
find
 falls back, the
warning
 field is populated in the query 
response.
9 October 2017
Error handling
If you rely on 500 replies for your application, you might have issues. To fix the problem, update your application to rely on 400 responses.
If you don't take care of reduce overflow errors as part of a row in the response body, issues occur. To fix this problem, change the application to
handle the errors from view requests.
August 2017
17 August 2017
The following changes were made in build 6365:
New! X-Frame-Options
Add the 
X-Frame-Options
 header settings. The 
X-Frame-Options
 setting is a response header that controls whether an HTTP response can be
embedded in a 
<frame>
, 
<iframe>
, or 
<object>
. This security feature helps prevent click jacking.
You can configure this option based on your CORS settings. If CORS is enabled, 
X-Frame-Options
 are automatically enabled and send the response
header, 
X-Frame-Options: DENY
, by default. If a request HOST header 
matches the URL listed in the origins section of CORS, an 
X-Frame-
Options: ALLOW-FROM URL
 response header is returned.
This change might impact customers who are accessing the database directly from the browser. If you see the error message, "X-Frame-Options:
DENY", and it's breaking your service, you must enable CORS by 
modifying the CORS configuration
. After you enable CORS, add the value of the
HOST header that you send in the request to the list of allowed 
origins
.
New! Replication scheduler
Add the replication scheduler. Learn more about 
replication scheduler
.
_revs-diff
 endpoint
POST
 requests to the 
_revs_diff
 endpoint require either the 
_reader
 or 
_replicator
 role.
July 2017
24 July 2017
Retire Shared plan
IBM Cloudant Shared Plan accounts can no longer be created from the 
IBM Cloudant product page
.
Cloudant
   
614 July 2017
The following changes were made in build 6276:
Error message
An error message changed that occurs when you try to put a document attachment with a nonexistent revision. Now, the error is a 409 error with the
following information:
{
"error"
:
"not_found"
,
"reason"
:
"missing_rev"
}
June 2017
26 June 2017
The following changes were made in build 6233:
IBM Cloudant Query and indexes
Fixes an IBM Cloudant Query issue where indexes that excluded potentially matching documents were selected by the query planner.
14 June 2017
Revised error message
The error message that occurs when you try to put a document attachment with a nonexistent revision. This error is changed to a 409 error with the
following information:
{
"error"
:
"not_found"
,
"reason"
:
"missing_rev"
}
May 2017
11 May 2017
The following changes were made in build 6069:
New! 
$allmatch
 operator support
Added support for the 
$allmatch
 operator.
Replication
Previously, a replication job that failed for some reason, which resulted in an update to the replication document, was followed by a fresh attempt to
start a new replication. Under some circumstances, this behavior might continue indefinitely: 
many duplicates of the same error message. A fix was
introduced so that the replication document is not updated unless the reason for the error changes.
February 2017
13 February 2017
The following changes were made in build 5834:
Cloudant
   
62Document 
id
 length
The maximum length of a document 
id
 is now 7168 characters (7k).
November 2016
25 November 2016
The following changes were made in build 5728:
Malformed user documents
IBM Cloudant is more tolerant of malformed user documents that are stored within the 
_users
 database.
Structure for user documents
User documents must be structured and populated to comply with 
Apache CouchDB requirements
.
October 2016
11 October 2016
The following changes were made in build 5638:
New! Parameters
Introduces new 
stable
 and 
update
 query parameters for views.
Replicator retries
Replicator no longer retries forever if it cannot write checkpoints to the source database.
June 2016
14 June 2016
The following changes were made in build 5421:
View-based filters
Changes feeds support view-based filters.
_docs_ids
 filter
Changes feeds support the 
_doc_ids
 filter.
POST
 requests
POST
 requests are supported for 
_changes
.
attachments=true
 parameter support
Both 
_all_docs
 and 
_changes
 support the 
attachments=true
 parameter.
CouchDB 1.6 
_users
 database support
Support for the CouchDB 1.6 
_users
 database features, including server-side hashing of passwords when documents are created in the 
_users
database.
/_bulk_get
 endpoint
/_bulk_get
 endpoint to reduce the number of requests that are used in replication to mobile clients.
Design document metadata
Cloudant
   
63Design document metadata contains an 
update pending
 field.
Eliminate error
IBM Cloudant Query no longer returns an error if no valid index exists.
February 2016
4 February 2016
dbcopy
The 
dbcopy
 feature can cause problems under some circumstances. Information about the feature was removed from the documentation. Use of
dbcopy
 is discouraged.
November 2014
6 November 2014
generate_api_key
 endpoint is deprecated
An earlier method of generating API keys by issuing the 
POST
 command to the 
https://cloudant.com/api/generate_api_key
 endpoint is
deprecated.
July 2014
1 July 2014
New! Introducing IBM Cloudant Classic
IBM® Cloudant® for IBM Cloud® is a document-oriented database as a service (DBaaS). It stores data as documents in JSON format. It is built with
scalability, high availability, and durability in mind.
Cloudant
   
64Locating your service credentials
You can find the credentials for any service that is associated with your account.
Objectives
1
. 
Locate your service credentials in IBM Cloud.
2
. 
Understand your service credentials.
Before you begin
Create a service instance in the IBM Cloud Dashboard by following the 
Getting started with IBM Cloudant
 tutorial.
Step 1: How to find your service credentials
1
. 
Go to 
IBM Cloud
 and log in.
2
. 
Find the service instance called 
Cloudant-o7
 and open it.
This instance is the one you created as in the 
Before you begin
 section.
Figure 1. Selecting the IBM Cloudant service
3
. 
Click 
Service credentials
.
4
. 
Click the chevron next to the service credentials to see the credentials that are required to access the service.
Cloudant
   
65Figure 2. Viewing the IBM Cloudant service credentials
Now, you can see the service credentials:
Figure 3. The IBM Cloudant service credentials
Step 2: Understanding your service credentials
Service credentials are valuable. If anyone or any application has access to the credentials, they can effectively do whatever they want with the service
instance. For example, they might create spurious data, or delete valuable information. 
Protect these credentials carefully.
IBM Cloudant has two authentication methods available at provisioning time, either 
Use only IAM
 or 
Use both legacy credentials and IAM
. You can
see the details about your legacy credentials only if the 
Use both legacy credentials and IAM
 
authentication method is chosen. The credentials
display on the Service credentials tab for your instance. For more information, see the 
IAM guide
 and 
legacy authentication
 
document for details about
using either style of authentication.
The service credentials include the following fields, as well as designating the fields that are only shown if you select the 
Use both legacy credentials
and IAM
 option:
Field
Purpose
Legacy-auth enabled
username
The username that is required for applications to access
the service instance.
password
The legacy credentials password that is required for
applications to access the service instance.
X
host
The hostname that is used by applications to locate the
service instance.
X
 Note: 
The service credentials in these examples were defined when a demonstration IBM Cloudant service was created on IBM Cloudant.
The credentials are reproduced here to show how they would appear in the dashboard. However, the demonstration 
IBM Cloudant service
was removed, so these credentials are no longer valid. You 
must
 supply and use your own service credentials.
Cloudant
   
66Table 1. Service credential fields
port
The HTTPS port number for accessing the service
instance on the host. It's 443 as only HTTPS access is
allowed by IBM Cloudant.
X
url
The HTTPS URL to access the IBM Cloudant instance.
X (If the 
Use both legacy credentials and IAM
 option
is chosen, it also includes the embedded legacy
username and password.)
apikey
The IAM API key.
iam_apikey_description
Description of the IAM API key.
iam_apikey_name
ID of the IAM API key.
iam_role_crn
The IAM role that the IAM API key has.
iam_serviceid_crn
The CRN of the service ID.
X
To create an application that can access your service instance, you need these credentials.
Cloudant
   
67Migrating an instance with legacy credentials and IAM Authentication to IAM Only
Authentication
When you create a new service credential by using the IBM Cloud Dashboard or the IBM Cloud CLI, it always produces a new username and password
combination. This method applies to legacy credentials as well as a new IAM API key. This tutorial guides 
you through migrating your instance from
generating new legacy credentials and IAM API keys to generating new IAM API keys only.
See the effects of this tutorial on existing legacy credentials:
New format legacy credentials (usernames that start with 
apikey-v2-
) continue to function until the service credential is deleted.
URL style legacy credentials if still active are revoked. If you would like to revoke them separately, follow the 
Revoking credential that is tied to your
instance URL
 
steps before you complete this tutorial.
Objectives
1
. 
Update your applications to use IAM credentials instead of legacy credentials.
2
. 
Disable creation of new legacy credentials.
Step 1: Generating new IBM Cloudant IAM Credentials
1
. 
Use the IBM Cloud Dashboard or the IBM Cloud CLI to 
generate new service credentials
 for your IBM Cloudant instance. For more information, 
see
Creating service credentials
 for further instructions.
Step 2: Updating applications
1
. 
Update all applications to use IAM access tokens when you authenticate with the IBM Cloudant instance.
Step 3: Migrating to IAM only
1
. 
Go to 
IBM Cloud
.
2
. 
Find your IBM Cloudant instance on the list of resources and open it.
 Important: 
This tutorial is only applicable to IBM Cloudant instances within resource groups with legacy credentials that are enabled.
 Important: 
This operation cannot be undone. Make sure all applications that access the instance are using IAM to authenticate before you start
this step.
Cloudant
   
68Figure 1. Resource list
3
. 
Click the 
Migrate to IAM Only
 button under the 
Authentication methods
 section. If you do not see the button, your instance is already IAM Only.
Figure 2. Authentication methods
4
. 
Click OK to confirm your action on the dialog window to proceed. If the instance URL-style credential is still enabled, the confirmation box differs. You
still click OK to confirm your action on the dialog window to proceed.
5
. 
When the operation completes successfully, the Authentication methods row shows only 
IBM Cloud IAM
.
Figure 3. Successful operation
Cloudant
   
69Revoking a credential that is tied to your instance URL
In IBM Cloud®, you create a new service credential by using the IBM Cloud Dashboard or the IBM Cloud CLI. This step always produces a new username
and password combination as your IBM® Cloudant® for IBM Cloud® legacy credentials. As expected, 
deleting the service credential effectively revokes
access for any applications that use those credentials.
Revoking a credential that is tied to your instance only works if the instance is in a resource group. This tutorial is not for instances in Cloud Foundry. If you
want to revoke a credential that is tied to your instance, you must first migrate 
the instance to a resource group. For more information, see 
Migrating Cloud
Foundry service instances and apps to a resource group
 or 
Resource Groups FAQ
.
Service credentials were not always handled like this though. Before 15 January 2021, creating a new service credential would always produce the same
IBM Cloudant legacy credential username and password combination. Deleting the service credential 
did not revoke its access either. This practice was
required to prevent breaking legacy applications that expected this behavior.
You can inspect the username of your IBM Cloudant legacy credentials to verify which type you are currently using. The old style credential uses the format
<RANDOM_ID>-bluemix
 for username, which matches your IBM Cloudant instance 
URL. The new style credentials use 
apikey-v2-<RANDOM_ID>
.
Objectives
1
. 
Update your applications to use the new style credentials in place of the instance URL style credentials.
2
. 
Revoke access to the old style IBM Cloudant legacy credential.
Step 1: Generating new IBM Cloudant legacy credentials
1
. 
Use the IBM Cloud Dashboard or the IBM Cloud CLI to 
generate new service credentials
 for your IBM Cloudant instance. See 
Creating service
credentials
 
for further instructions.
Step 2: Updating applications
1
. 
Update all applications that have access to the IBM Cloudant instance to use the new username and password combination.
Step 3: Revoking access to the instance URL style credential
1
. 
Go to 
IBM Cloud
.
2
. 
Find your IBM Cloudant instance on the list of resources and open it.
 Important: 
This tutorial is only applicable to IBM Cloudant instances provisioned before 15 January 2021 with IBM Cloudant legacy credentials
enabled. Instances provisioned after this date already use the new format of legacy credentials.
 Important: 
This operation cannot be undone. Make sure all your applications are no longer using the old style credential before you start this
procedure.
Cloudant
   
70Figure 1. IBM Cloudant instances in resource list
3
. 
Click the 
Revoke
 button under the 
Cloudant credentials status
 section. If you do not see the information that is shown in the next screen capture, the
credential was already revoked, or it never existed.
Figure 2. Instance URL style credential
4
. 
Click OK to confirm your action on the dialog window to proceed.
5
. 
When the operation completes successfully, the status changes to 
Revoked
.
 Note: 
After the credential is revoked by using this process, the 
Cloudant credentials status
 section no longer appears on the page.
Cloudant
   
71Using the IBM Cloudant Dashboard
By using the IBM® Cloudant® for IBM Cloud® Dashboard, you create an IBM Cloudant database, populate the database with data, and retrieve data by using
queries or API endpoints. For more information about API endpoints, see the 
API and SDK reference
.
Objectives
1
. 
Open the IBM Cloudant Dashboard.
2
. 
Create a database.
3
. 
Add JSON documents to the database and run a query.
4
. 
Replicate a database.
5
. 
Monitor active tasks.
6
. 
Monitor with IBM Cloudant.
Before you begin
Create a service instance in IBM Cloud before you start this tutorial. You can follow the instructions in the 
Getting started
 tutorial to create one.
Step 1: Opening your service instance on IBM Cloudant Dashboard
Open your IBM Cloudant service instance by following these steps:
1
. 
Go to the IBM Cloud Dashboard.
2
. 
Click 
Services
 in the Resource list.
3
. 
From the Services section, click the 
Cloudant-o7
 instance that you created in the 
Getting started
 tutorial, and click 
Launch Dashboard
. The IBM
Cloudant Dashboard opens.
Now, you can create a database and run queries against it.
Step 2: Creating a database
In this exercise, you create the 
dashboard-demo
 
database
, which is the database that you use in this tutorial.
1
. 
From the IBM Cloudant Dashboard, click 
Create database
.
The Create database window opens.
2
. 
Enter the database name 
dashboard-demo
.
3
. 
Select 
Non-partitioned
, and click 
Create
.
The 
dashboard-demo
 database opens automatically.
Now, you can create some documents.
Step 3: Adding documents to the database
The 
documents
 that you create in this exercise include the data that you use to query the 
dashboard-demo
 database in later exercises.
1
. 
Click 
Create document
.
The New Document window opens.
2
. 
Copy the following sample text and replace the existing text in the new document. Use the following sample text for document 1:
{
  
"firstname"
:
 
"Sally"
,
  
"lastname"
:
 
"Brown"
,
  
"age"
:
 
16
,
  
"location"
:
 
"New York City, NY"
,
  
"_id"
:
 
"doc1"
}
3
. 
Repeat steps 1 and 2 to add the remaining four documents to the database. Use the following sample text for document 2:
Cloudant
   
72{
  
"firstname"
:
 
"John"
,
  
"lastname"
:
 
"Brown"
,
  
"age"
:
 
21
,
  
"location"
:
 
"New York City, NY"
,
  
"_id"
:
 
"doc2"
}
Use the following sample text for document 3:
{
  
"firstname"
:
 
"Greg"
,
  
"lastname"
:
 
"Greene"
,
  
"age"
:
 
35
,
  
"location"
:
 
"San Diego, CA"
,
  
"_id"
:
 
"doc3"
}
Use the following sample text for document 4:
{
  
"firstname"
:
 
"Anna"
,
  
"lastname"
:
 
"Greene"
,
  
"age"
:
 
44
,
  
"location"
:
 
"Baton Rouge, LA"
,
  
"_id"
:
 
"doc4"
}
Use the following sample text for document 5:
{
  
"firstname"
:
 
"Lois"
,
  
"lastname"
:
 
"Brown"
,
  
"age"
:
 
33
,
  
"location"
:
 
"New York City, NY"
,
  
"_id"
:
 
"doc5"
}
You populated the 
dashboard-demo
 with five documents. You can see the documents from the Table view in the following screen capture:
Figure 1. Sample documents
Running a simple query
This example demonstrates how IBM Cloudant Query finds documents based on the 
lastname
 and the 
firstname
.
1
. 
Click 
Query
.
2
. 
Copy the following sample JSON and replace the existing text in the new query window:
 
{
    
"selector"
:
 
{
          
"lastname"
 
:
 
"Greene"
,
          
"firstname"
 
:
 
"Anna"
            
       
}
        
 
}
Cloudant
   
733
. 
Click 
Run Query
.
The query displays the results. You can see them from the Table view in the following screen capture:
Figure 2. Query results
For more information, see the 
IBM Cloudant Query
 tutorial or the API reference on 
IBM Cloudant Query
.
Step 4: Replicating a database
When you replicate a database, it synchronizes the state of two databases: source and target. A replication copies all the changes that happened in the
source database to the target database. When a document is deleted from the source database, 
the document is also deleted from the target database.
For more information, see 
Replication
.
1
. 
Click 
Replication
.
2
. 
Click 
New Replication
.
The Job configuration page opens.
3
. 
Enter the following information for your replication job. Use the following information in the Source section:
Type - Select 
Remote database
.
Name - Enter the database URL: 
$SERVICE_URL/query-movies
.
Authentication - Leave as 
None
.
Use the following information in the Target section:
Type - Select 
New local database
.
New database - Enter the name for the new database, 
query-movies
.
New database options - Do not select the Partitioned option.
Authentication - Select 
IAM Authentication
.
IAM API Key - Enter the 
apikey
 from the Service credentials for your instance.
For more information, see the section on 
Locating your service credentials
.
Use the following information in the Options section:
Replication type - Leave as 
One time
.
Replication document - Leave as 
Custom ID (optional
.
 Note: 
Additionally, you can create a replication from the databases page by clicking 
Replicate
 in the Actions column.
Cloudant
   
74Figure 3. Replication configuration page
4
. 
Click 
Start Replication
.
The Replication page opens where you can see that your replication job is running.
Figure 4. Status of your replication job
5
. 
See the status when your job finishes change to Completed.
6
. 
Check that the database was created on the databases page.
Cloudant
   
75Figure 5. Databases page
Step 5: Monitoring active tasks
The Active tasks page displays a list of all running tasks. When you monitor your system's performance, this list can help you find potential issues. You can
see a list of active tasks, which includes compaction, replication, and indexing. For 
more information, see the 
Managing tasks
 guide.
1
. 
Click 
Active Tasks
.
The Active Tasks page opens.
Figure 6. Active tasks
2
. 
Click the associated tab to see task-specific information.
Step 6: Monitoring with IBM Cloudant
Monitor your usage with a graph that shows your throughput by reads, writes, and global queries. You can see your current operations, denied requests,
and storage usage.
Your service instance contains no data because it is for demonstration purposes only. However, you can see what monitoring information is available to you
by following these steps:
1
. 
Click 
Monitoring
.
The Monitoring page opens to the Current Operations tab. Review recent consumption of provisioned throughput capacity by looking at requests
broken down by reads, writes, and global queries. The dotted line is the peak capacity that is allowed 
for your instance. Peak capacity is based on
what is set for your provisioned throughput capacity.
 Tip: 
If your instance does not have any active tasks, you can return to the previous step, delete the 
query-movies
 database, and then replicate it
again. If you open the Active Tasks page immediately, you can see your replication.
Cloudant
   
76Figure 7. Current Operations
2
. 
Click 
Denied Requests
.
Review the number of denied requests from a given second that are shown by the number of 
429: too many requests
 responses. Requests are
denied when they exceed the provisioned throughput capacity set for the instance. The graph 
shows the denied requests that are broken down by
reads, writes, and global queries.
Figure 8. Denied Requests
3
. 
Click 
Storage
.
Periodically review your storage, so you are prepared if your plan's provisioning needs to be changed.
Cloudant
   
77Figure 9. Storage
For more information, see 
Plans and provisioning
.
Cloudant
   
78Digging deeper into IBM Cloudant Dashboard
The IBM® Cloudant® for IBM Cloud® Dashboard gives new and experienced IBM Cloudant users the opportunity to add, edit, and delete documents. The
IBM Cloudant users can refine the indexing and querying options that best suit their application's 
use-cases.
Objectives
Set up some basic indexes using the Dashboard to see how each of IBM Cloudant's querying mechanisms works.
Before you begin
You need to create a service instance in IBM Cloudant before you start this tutorial. You can follow the instructions in the 
Getting started
 tutorial to create
one.
Step 1. The data set
1
. 
Create a database called 
books
.
2
. 
Create some sample data that represents a book in a library as shown in the following example:
{
  
"_id"
: 
"BXP9G5ZQY9Q4EA13"
,
  
"author"
: 
"Dickens"
,
  
"title"
: 
"David Copperfield"
,
  
"year"
: 
1840
,
  
"pages"
: 
723
,
  
"publisher"
: 
"Penguin"
,
  
"url"
: 
"https://www.somurl.com/dc"
}
3
. 
Continue to add some documents that match the pattern in the previous step by using the IBM Cloudant Dashboard.
The documents store simple 
key/value
 pairs that hold metadata about each book: its author and its publisher. In this example, we address the
following three use-cases:
a
. 
A query facility that allows a user to find a book by a known publisher and year.
b
. 
A general-purpose search engine that allows a user to find books by a combination of one or more of the following descriptors: author, title,
year, and publisher.
c
. 
A report that details the number of books that are published by year.
Step 2. Querying books by publisher and year - IBM Cloudant Query
IBM Cloudant Query is a query language that allows small slices of a total database to be located. The following query finds 10 books that are published by
Penguin
 in the year 2000:
{
  
"selector"
:
 
{
    
"$and"
:
 
[
      
{
 
"publisher"
:
 
"Penguin"
 
}
,
      
{
 
"year"
:
 
{
 
"$gt"
:
 
2000
 
}
 
}
    
]
  
}
,
  
"limit"
:
 
10
}
The query contains a 
selector
 object, which uses operators and text fields to define the slice of data you need:
$and
 means 
both
 of the query clauses must be satisfied for a document to make it to the result set.
{ "publisher": "Penguin" }
- the publisher must be "Penguin".
{ "year": { "$gt": 2000 } }
 - the year must be greater than 2000. 
$gt
 means "greater than".
We can try the query by choosing "Query" when you view our 
books
 database in the IBM Cloudant Dashboard. You can paste in the query JSON and click
Run Query
.
Cloudant
   
79Running a query
To try the query, do the following steps:
1
. 
Go to IBM Cloudant Dashboard.
2
. 
Open the service instance that you created in the prerequisite section.
3
. 
Open the database that you created.
4
. 
Go to the Query tab.
5
. 
Paste the query JSON from the previous section into the Cloudant Query window.
6
. 
Click 
Run Query
. See the results in the following screen capture:
Figure 1. Window for running queries
Creating an index
To create an index, we can tell IBM Cloudant to create an index on the 
publisher
 and 
year
 fields that we are using in our query.
1
. 
From the IBM Cloudant Dashboard, select the 
books
 database.
2
. 
Select the Design Documents tab.
3
. 
Select New Indexes from the Design Documents menu.
4
. 
Copy and paste the following index definition:
{
   
"index"
: {
      
"fields"
: [
         
"publisher"
, 
"year"
      ]
   },
   
"name"
: 
"publisher-year-index"
,indexingdashboard5
   
"type"
: 
"json"
}
 Note: 
IBM Cloudant matches the documents that meet your criteria and it 
seems
 to do it quickly, but there's a catch. IBM Cloudant isn't using an
index to service this query, meaning that the database has to scan every document in the database 
to get your answer. This scan is fine for small
data sets. But if you're running a production application where the data set is expanding all the time, you definitely 
don't
 want to rely on unindexed
queries.
Cloudant
   
80See an example in the following screen capture:
Figure 2. Window for creating indexes
The 
fields
 array contains a list of fields that we want IBM Cloudant to index.
If we repeat our query, it is faster and remains quick even as the database size reaches millions of documents.
For more information, see the following details in IBM Cloudant documentation:
Optimizing IBM Cloudant Queries
IBM Cloudant Query documentation
This index is useful for queries that involve both the 
publisher
 and the 
year
, but if we introduce another field or make the query more complex (for
example, by using the 
$or
 operator), then the index 
doesn't get used. We are back to a full database scan.
For a general-purpose search facility, we need IBM Cloudant Search, which is described in the next section.
Step 3. Creating a search engine - IBM Cloudant Search
IBM Cloudant Search is based on Apache Lucene and has its own query language that allows rich queries to be constructed. See the following example of a
search:
publisher:Penguin AND (year:1972 OR year:1973) AND title:Crash
Unlike IBM Cloudant Query, you 
must
 specify the fields to index 
before
 you perform a query. IBM Cloudant Search indexes are defined by supplying IBM
Cloudant with a JavaScript function that is called once for every document 
in the database - if the function calls 
index
 then data is added to the index.
1
. 
From the IBM Cloudant Dashboard, select the 
books
 database.
2
. 
Select the Design Documents tab.
3
. 
Select New Search Index from the menu.
4
. 
Enter a design document name.
5
. 
Enter an index name.
6
. 
Paste the following code into the search index function:
function
 (
doc
) {
  
index
(
"author"
, doc.
author
);
  
index
(
"publisher"
, doc.
publisher
);
  
index
(
"title"
, doc.
title
);
  
index
(
"year"
, doc.
year
);
}
 Note: 
Indexing instructs IBM Cloudant to create a secondary data structure that allows it to find the slice of data you need much faster than
looking over every document in turn. IBM Cloudant Query is best for fixed queries based on the same fields 
in the same order.
Cloudant
   
817
. 
Choose the "Standard Analyzer".
Figure 3. New Search Index window
You can then build complex queries that involve one, some, or all of the indexed fields combined with AND and OR operators.
For more information, see the following resources:
IBM Cloudant Search uses "analyzers" to pre-process text before indexing. Learn about 
Search Analyzers
 to ensure you get the results that you
expect.
IBM Cloudant Search documentation
Step 4. Aggregating data - MapReduce
IBM Cloudant Query and IBM Cloudant Search cannot 
aggregate
 search results. In other words, you can't ask, 
How many books were published in 1973?
IBM Cloudant's MapReduce feature allows secondary indexes to be created that 
can be used for selection or aggregation. MapReduce indexes are, like
IBM Cloudant Search, which is created by supplying a JavaScript function - any call to an 
emit
 function adds a row to the index.
1
. 
From the IBM Cloudant Dashboard, select the 
books
 database.
2
. 
Select the Design Documents tab.
3
. 
Select New View from the menu.
4
. 
Keep New document in the drop-down field.
5
. 
Enter a name in the Index name field. This name is the new view name.
6
. 
Select 
_count
 from the Reduce (optional) drop-down menu. This way our results are 
counted
.
7
. 
Paste the following code into the Map function field:
 Tip: 
IBM Cloudant Search is best if you have many search use-cases involving different combinations of fields.
Cloudant
   
82function
 (
doc
) {
  
emit
(doc.
year
, 
null
);
}
See an example of the window in the following screen capture:
Figure 4. New View window
The subsequent MapReduce view allows documents to be found by year (as that is the key of the index). But if we select the checkbox for the
Reduce function from the 
Options
 pull-down menu, the index aggregates the results, 
grouping by key (year):
Figure 5. Windows for running queries
See an example result from after the index aggregated the results.
Cloudant
   
83Figure 6. Result set
MapReduce views are perfect for generating ordered views of your data, containing 
key/value
 pairs that you define. They can be used for selecting
individual keys, range queries, or aggregation grouping by the key.
For more information, see the following resources from IBM Cloudant documentation:
MapReduce blog
MapReduce documentation
Cloudant
   
84Creating a web-based To-Do list
Create a simple web-based to-do list to get familiar with the basic IBM Cloud features.
Objectives
1
. 
From this tutorial, you learn how to create a basic website that interfaces with your IBM Cloud database to read and write data.
2
. 
To create this to-do list, your application needs to be able to read and write to the database. To read to-dos in "newest first" order and to filter by tag,
your database needs to have some secondary indexes. Now, we can create 
all of that.
You can complete the tutorial in less than an hour. It doesn't cost you anything over your current IBM Cloudant bill (so it's free if you are on the IBM
Cloudant Lite plan).
The website that you create is served from your local machine, so no other services are required apart from IBM Cloud.
After you complete it, you have a basic understanding of how applications can interface with IBM Cloudant through an IBM Cloudant SDK (in this case,
NodeJS).
Before you begin
You need the following implements to complete this tutorial:
1
. 
An IBM Cloudant service instance and some service credentials. You can create the instance and credentials in the IBM Cloudant Dashboard by
following the 
Getting started with IBM Cloudant
 
tutorial. Be sure to make a note of the APIKey and URL when you create your service credentials.
2
. 
Ensure you have access to a Mac or Linux™ terminal.
3
. 
Download 
Git
.
4
. 
Download 
Node.js and npm
.
Step 1: Get the code
1
. 
Open your terminal.
2
. 
Type the following command:
git 
clone
 https://github.com/IBM-Cloud/todo-list.git
cd
 todo-list
Step 2: Prepare the environment and run the website
In this step, you install all the code dependencies and environment variables you need to run your website.
1
. 
Ensure you are in the 
todo-list
 directory.
2
. 
From your terminal, run the following command:
npm install
export
 CLOUDANT_APIKEY=
"<the_apikey_from_prerequisites>"
export
 CLOUDANT_URL=
"https://<the_url_from_prerequisites>"
npm run start
Step 3: Check out your website!
Now, you can check out your website.
1
. 
From your browser, go to 
https://localhost:8080
.
 Tip: 
The project is a simple to-do list, where you can see a list of notes. You can add and delete notes. Each of your notes has a tag, and you
can filter your notes by tag.
 Note: 
When you run this command for the first time, your code detects that no database exists. The code creates a database for you with some
indexes (by date and by tag) and some sample data.
Cloudant
   
85You can see your to-do list with a couple of items on it:
Figure 1. Your web-based To-Do list
2
. 
Add or delete notes, or you can filter by tag by clicking one of the tags.
Understanding the code
Database and Index creation
The backend script (
server.js
), on start-up, tries to connect to the 
todo
 database by using the 
getDatabaseInformation
 method. If it doesn't find it,
it attempts to create it by using the 
putDatabase
 
method.
After you create the 
todo
 database, it creates two indexes by using the 
postIndex
 method. The first creates an index on the timestamp field (the
creation date of your note), so it can retrieve all notes in reverse 
chronological order. The second index is on the tag and timestamp so that it can filter by
tag and return a date-ordered list for a known tag.
Using the database
The front end is using the popular 
express
 framework to display a webpage and call service endpoints in your backend when you click different actions,
like create, delete, and filter.
For example, when your webpage is first loaded, it calls the 
GET /todolist
 endpoint. The 
GET /todolist
 endpoint uses the 
postFind
 method to
query the database for all documents (by using the index created 
after the 
todo
 database), and then orders the notes by timestamp, and returns them to
the front end for display.
Filtering by tag uses the same 
postFind
 method, but by using the second index, you create and delete notes by using the 
postDocument
 and
deleteDocument
 methods.
Summary
IBM Cloudant allows rapid development of web applications, as its HTTP API is modeled by the 
Node.js SDK
 and is easy to integrate with your own code.
You create an IBM Cloudant 
database and add JSON documents that model your own data. Remember to create secondary indexes to help service your
query access patterns so that query performance remains quick as your data volume grows.
Cloudant
   
86If you don't fancy writing JavaScript, we have SDKs for 
Java™, Python, and Go
, plus our 
HTTP API
. Don't forget. The 
IBM Cloudant Dashboard
 
is a great
way to explore your databases, create and modify documents, and refine your index and querying skills.
You can find more best practice guidance in our 
blog
 and 
learning center
.
Cloudant
   
87Creating an instance with CLI
This tutorial shows you how to create an IBM® Cloudant® for IBM Cloud® service instance on IBM Cloud® by using the IBM Cloud CLI.
Objectives
1
. 
Use your IBM Cloud account to create your IBM Cloudant service instance and credentials.
2
. 
Retrieve and use your IBM Cloudant service instance.
Before you begin
Install the IBM Cloud CLI developer tools by following the 
Getting started with the IBM Cloud CLI
 tutorial.
Step 1: Logging in to your IBM Cloud account
The following example describes how to log in. If you use a federated user ID, it's important that you switch to a one-time passcode (
ibmcloud login --
sso
), or use an API key (
ibmcloud --apikey key or @key_file
) to 
authenticate. For more information about how to log in by using the CLI, see
General CLI (ibmcloud) commands
 under 
ibmcloud login
.
1
. 
Start the login process for your IBM Cloud account by using the following command.
ibmcloud login
IBM Cloud responds by reminding you of the current API endpoint, and asks for the email address of your account.
$ 
API endpoint: https://cloud.ibm.com
Region: au-syd
Email>
Password>
2
. 
Enter the email address of your account, and then enter your password.
$ 
API endpoint: https://cloud.ibm.com
Email> J.Doe@email.com
Password>
IBM Cloud validates your details and summarizes the information about your login session.
$ 
API endpoint: https://cloud.ibm.com
Email> J.Doe@email.com
Password>
Authenticating...
OK
Targeted account J DOE
's Account (707...a32)
Targeted org J.Doe@email.com
Targeted space dev
API endpoint:   https://cloud.ibm.com (API version: 2.54.0)
Region:         au-syd
User:           j.doe@email.com
Account:        J DOE'
s Account (707...a32)
Org:            J.Doe@email.com
Space:          dev
3
. 
You're now logged in to your IBM Cloud account.
Cloudant
   
88Step 2: Creating the IBM Cloudant service
IBM Cloudant uses resource groups for provisioning new instances. For more information, see the 
Resource Groups FAQ
.
In this example, you create a service instance within IBM Cloud by running the following command.
$ 
ibmcloud resource service-instance-create NAME SERVICE_NAME SERVICE_PLAN_NAME LOCATION [-p, --parameters @JSON_FILE |
 
JSON_STRING ]
The fields in the command are described in the table that follows.
Table 1. Basic command format fields
Field
Description
NAME
Arbitrary name that you give to the instance.
SERVICE_NAME
cloudantnosqldb
SERVICE_PLAN_NAME
Lite plan (
lite
) or Standard plan (
standard
)
LOCATION
The location where you want to deploy includes the following cities: Sydney 
au-syd
, Chennai 
in-che
, Osaka 
jp-osa
, Tokyo
jp-tok
, Seoul 
kr-seo
, Frankfurt 
eu-de
, 
London 
eu-gb
, Dallas 
us-south
, Washington DC 
us-east
.
legacyCredentials
Defaults to 
true
. This field dictates whether the instance uses both legacy and IAM credentials or IAM credentials only.
Now, we create a service instance that is called, 
cs20170517a
.
1
. 
Set your target resource group and region by using the following format. To run this command, you need to know the region and resource groups,
which you find in the following steps.
For more information, see 
General CLI (ibmcloud) commands
 under 
ibmcloud target
.
ibmcloud target [-r REGION_NAME] [-g RESOURCE_GROUP]
2
. 
To see a list of regions, run the following command.
ibmcloud regions
3
. 
To see a list of resource groups, run the following command.
ibmcloud resource groups
4
. 
Create an instance of an IBM Cloudant service by using the 
Lite
 plan.
The instance name is 
cs20170517a
 in the US-South location and uses IAM credentials only.
ibmcloud resource service-instance-create cs20170517a cloudantnosqldb lite us-south -p 
'{"legacyCredentials": false}'
5
. 
After you create the service instance, see the following example message.
$ 
Creating service instance cs20170517a 
in
 resource group default of account John Does
's Account as j.doe@email.com...
OK
Service instance cs20170517a was created.
Name          Location   State        Tags
cs20170517a   au-syd   active   service_instance
 Tip: 
SERVICE_PLAN_NAME
 is the type of pricing plan you select when you create an instance. For more information, see 
Plans
 in the
documentation for details 
on using the IBM Cloudant Lite or Standard plan.
 Important: 
For more information about choosing an authentication method, see the 
IAM guide
. The IBM Cloudant team recommends that you use
IAM access controls over IBM Cloudant legacy 
authentication whenever possible.
Cloudant
   
89Next, you create service credentials for your IBM Cloudant service instance.
Step 3: Creating credentials for your IBM Cloudant service
Applications that require access to your IBM Cloudant service must have the necessary credentials.
For more information about the fields included in the service credentials, see the 
IAM guide
.
In the next example, you create credentials for a service instance within IBM Cloud by running the following command.
$ 
ibmcloud resource service-key-create NAME ROLE_NAME --instance-name SERVICE_INSTANCE_NAME
The fields in the command are described in the table that follows.
Table 2. Create credential fields
Field
Description
NAME
Arbitrary name that you give the service credentials.
ROLE_NAME
This field currently allows the Manager role only.
SERVICE_INSTANCE_NAME
The name that you give to your IBM Cloudant instance.
Now, you create credentials for the 
cs20170517a
 instance you created in the previous step.
1
. 
Create credentials for the 
cs20170517a
 instance of an IBM Cloudant service (where the name for the credentials is 
creds_for_cs20170517a
) by
running the following command.
ibmcloud resource service-key-create creds_for_cs20170517a Manager --instance-name cs20170517a
2
. 
After you receive the request to create credentials for the service instance, review the response from IBM Cloud that contains a message similar to
the one in the following example.
$ 
Creating service key 
in
 resource group default of account John Does
's Account as john.doe@email.com...
OK
Service key crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a was created.
Name:          creds_for_cs20170517a
ID:            crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a
Created At:    Tue Sep 18 19:58:38 UTC 2018
State:         active
Credentials:
               iam_apikey_name:          auto-generated-apikey-621ffde2-ea10-4318-b297-d6d849cec48a
               iam_role_crn:             crn:v1:bluemix:public:iam::::serviceRole:Manager
               url:                      https://apikey-v2-
58B528DF5397465BB6673E1B79482A8C:5811381f6daff7255b288695c3544be63f550e975bcde46799473e69c7d48d61@f6cf0c55-48ea-4908-b441-
a962b27d3bb6-bluemix.cloudant.com
               username:                 apikey-v2-58B528DF5397465BB6673E1B79482A8C
               port:                     443
               apikey:                   XXXXX-XXXXXX_XXXXXXXXXXXXX-XXXXXXXXXXX
               host:                     f6cf0c55-48ea-4908-b441-a962b27d3bb6-bluemix.cloudant.com
               iam_apikey_description:   Auto generated apikey during resource-k  ey operation for Instance -
 
crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42116849bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-825c937fafa3::
               iam_serviceid_crn:        crn:v1:bluemix:public:iam-
identity::a/b42116849bb7e2abb0841ca25d28ee4c::serviceid:ServiceId-53f9e2a2-cdfb-4f90-b072-bfffafb68b3e
               password:                 581138...7d48d61
Next, you learn how to retrieve your service credentials. You need your service credentials to log in to your IBM Cloudant instance.
 Important: 
Service credentials are valuable. If anyone or any application has access to the credentials, they can effectively do whatever they want
with the service instance. For example, they might create spurious data, or delete valuable information. 
Protect these credentials carefully.
Cloudant
   
90Step 4: Retrieving the service credentials for your IBM Cloudant service
1
. 
Retrieve credentials for the 
cs20170517a
 instance of an IBM Cloudant service. The name for the credentials is 
creds_for_cs20170517a
.
ibmcloud resource service-key creds_for_cs20170517b
2
. 
After you receive the request to retrieve the credentials for the service instance, review the response from IBM Cloud that contains a message similar
to the one in the following (abbreviated) example.
$ 
Retrieving service key 
in
 resource group default of account John Does
's Account as john.doe@email.com...
OK
Service key crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a was created.
Name:          creds_for_cs20170517a
ID:            crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a
Created At:    Tue Sep 18 19:58:38 UTC 2018
State:         active
Credentials:
             iam_apikey_name:          auto-generated-apikey-621ffde2-ea10-4318-b297-d6d849cec48a
             iam_role_crn:             crn:v1:bluemix:public:iam::::serviceRole:Manager
             url:                      https://apikey-v2-
58B528DF5397465BB6673E1B79482A8C:5811381f6daff7255b288695c3544be63f550e975bcde46799473e69c7d48d61@f6cf0c55-48ea-4908-b441-
a962b27d3bb6-bluemix.cloudant.com
             username:                 apikey-v2-58B528DF5397465BB6673E1B79482A8C
             port:                     443
             apikey:                   XXXXX-XXXXXX_XXXXXXXXXXXXX-XXXXXXXXXXX
             host:                     f6cf0c55-48ea-4908-b441-a962b27d3bb6-bluemix.cloudant.com
             iam_apikey_description:   Auto generated apikey during resource-key operation for Instance -
 
crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42116849bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-825c937fafa3::
             iam_serviceid_crn:        crn:v1:bluemix:public:iam-
identity::a/b42116849bb7e2abb0841ca25d28ee4c::serviceid:ServiceId-53f9e2a2-cdfb-4f90-b072-bfffafb68b3e
             password:                 581138...7d48d61
Now, the tutorial is complete. Optionally, you can delete the service credentials or service instance as shown in the steps in the next two sections.
For more information, see the 
Creating and populating a simple IBM Cloudant database on IBM Cloud
 tutorial. This tutorial shows you 
how to use an IBM
Cloudant service instance from a Python application by using legacy credentials. Remember to substitute the credentials you created.
Step 5: (Optional) Deleting service credentials
Delete the credentials called 
creds_for_cs20170517a
 by running a command like this one.
$ 
ibmcloud resource service-key-delete creds_for_cs20170517a
Step 6: (Optional) Deleting a service instance
Delete the 
cs20170517a
 instance of an IBM Cloudant service by running a command like this one.
$ 
ibmcloud resource service-instance-delete cs20170517a
Cloudant
   
91Using a Dedicated Hardware plan instance
This tutorial shows you how to create an IBM® Cloudant® for IBM Cloud® Dedicated Hardware plan instance that uses the IBM Cloud® Dashboard.
After that exercise, you learn how to provision one or more Standard plan instances to run on the IBM Cloudant Dedicated Hardware plan instance by using
either the IBM Cloud catalog or the IBM Cloud CLI.
When you create an IBM Cloudant Dedicated Hardware plan instance, an IBM Cloudant environment on dedicated hardware is created for your sole use. A
service instance for the Dedicated Hardware plan environment is also created in the IBM Cloud Dashboard. 
You can't access the Dedicated Hardware plan
instance directly, or have any Service Credentials for it. Instead, you use your IBM Cloudant Dedicated Hardware plan instance by creating one or more
Standard plan instances on it, and managing the 
Standard plan instances directly.
Objectives
1
. 
Create a Dedicated Hardware plan instance.
2
. 
Provision a Standard plan instance on a Dedicated Hardware environment.
3
. 
Provision a Dedicated Hardware plan instance with the IBM Cloud CLI.
4
. 
Provision a Standard plan instance on a Dedicated Hardware environment with the IBM Cloud CLI.
5
. 
Create the credentials for your IBM Cloudant service.
6
. 
List the service credentials for your IBM Cloudant service.
Step 1: Creating an IBM Cloudant Dedicated Hardware plan instance
1
. 
Log in to your IBM Cloud account.
The IBM Cloud Dashboard can be found by using the following website: 
https://cloud.ibm.com/
. After you authenticate with your username and
password, the IBM Cloud Dashboard opens.
2
. 
Click 
Create resource
.
3
. 
Type 
Cloudant
 in the Search bar and open it.
4
. 
Select the Cloudant offering.
5
. 
Select an environment.
a
. 
Click 
Dedicated
.
b
. 
Click 
Create Host
.
Figure 1. Host selection
c
. 
Select from the IBM Cloud regions.
6
. 
Configure the Host.
 Note: 
For Dedicated Hardware provisioned instances, you can select from the major IBM Cloud regions in the IBM Cloud Dashboard.
However, the actual physical location of the Dedicated Hardware instance is dictated by the location parameter in a 
later step.
Cloudant
   
92a
. 
Select a location for deployment.
This location is the physical location of the instance, which can be in any IBM Cloud location, including locations outside the major regions. For
more information, see 
IBM® global data centers
.
b
. 
Select 
Yes
 or 
No
 to answer whether HIPAA is required.
Step 3: Provisioning a Dedicated Hardware plan instance with the IBM Cloud CLI
a
. 
Log in to IBM Cloud to use IBM Cloud CLI.
For more information, see 
log in to your IBM Cloud account
 to learn about how to log in and set a target resource group.
b
. 
Use the following basic command format to create an IBM Cloudant Dedicated Hardware plan instance by using IBM Cloud CLI.
ibmcloud resource service-instance-create 
$NAME
 
$SERVICE_NAME
 
$PLAN_NAME
 
$REGION
 [-p, --parameters @JSON_FILE |
 
JSON_STRING ]
Table 1. Basic command format
Field
Description
NAME
An arbitrary name that you assign the instance.
SERVICE_NAME
cloudantnosqldb
PLAN_NAME
dedicated-hardware
REGION
The major region where you want to deploy, for example, us-south, us-east, or eu-gb.
IBM Cloudant Dedicated Hardware plan instances take four more parameters.
Table 2. Parameters
Parameter
Description
location
The actual physical location of the Dedicated Hardware plan instance, which might differ from the REGION. The location
can be in any IBM Cloud location, including major regions and locations outside the major regions. For more information,
see 
IBM® global data centers
.
hipaa
Either 
true
 or 
false
.
kms_instance_crn
An optional parameter that must be set to the CRN of the Key Protect instance housing the encryption key for BYOK. All
IBM Cloudant environments are encrypted. If you would like to BYOK with Key Protect, supply the CRN of the Key Protect
instance that holds the encryption key. Otherwise, don't supply this parameter in the CLI, which means the environment
is encrypted with an IBM Cloudant-managed key. In order to BYOK with Key Protect, ensure that IBM Cloudant is
authorized 
to access the selected key management service instance. You can manage service-to-service authorizations
at any time by visiting 
Manage
 > 
Security
 > 
Identity and Access
 and choosing 
Authorizations
.
kms_key_crn
This parameter is required if you use the 
kms_instance_crn
 parameter. Otherwise, it must not be supplied in the CLI
command. The 
kms_key_crn
 parameter is set to the CRN of the encryption key that is stored in 
the Key Protect instance
that is defined by the 
kms_instance_crn
 parameter.
The following example command includes the extra parameters.
ibmcloud resource service-instance-create cloudant-dedicated-with-byok cloudantnosqldb dedicated-hardware us-south -p
 
'{"location":"dallas", "hipaa":"false", "kms_instance_crn": "crn:v1:bluemix:public:kms:us-
south:a/abcdefg7df5907a4ae72ad28d9f493d6:888a5a41-543c-4ca7-af83-74da3bb8f711::", "kms_key_crn":
 
"crn:v1:bluemix:public:kms:us-south:a/abcdefg7df5907a4ae72ad28d9f493d6:888a5a41-543c-4ca7-af83-74da3bb8f711:key:0123c653-
f904-4fe7-9fdb-5097e1ed85db"}'
 Note: 
HIPAA is only valid for US locations. IBM® can provision a Dedicated Hardware plan environment to implement HIPAA controls.
An environment is only created upon confirmation of a Business Associate Agreement (BAA) that is established 
with IBM. For more
information, see 
how to locate your service credentials
.
Cloudant
   
93Step 4: Provisioning a Standard plan instance on a Dedicated Hardware environment
with the IBM Cloud CLI
a
. 
Log in to use the IBM Cloud CLI. For more information about how to log in and set a target resource group, see 
log in to your IBM Cloud
account
.
b
. 
Create an IBM Cloudant Standard plan instance on your IBM Cloudant Dedicated Hardware plan environment by using the following basic
command format.
ibmcloud resource service-instance-create 
$NAME
 
$SERVICE_NAME
 
$PLAN_NAME
 
$REGION
 [-p, --parameters @JSON_FILE |
 
JSON_STRING ]
Table 3. Basic command format
Field
Description
NAME
An arbitrary name that you assign the instance.
SERVICE_NAME
cloudantnosqldb
PLAN_NAME
standard
REGION
The region where you want to deploy, for example, us-south, us-east, or eu-gb.
IBM Cloudant instances that are deployed on Dedicated Hardware environments take two more parameters.
Table 4. Parameters
Parameter
Description
environment_crn
This parameter must be set to the CRN of the IBM Cloudant Dedicated Hardware plan instance. You can determine
what the CRN is by looking at the example CLI command in the Manage tab of the IBM Cloudant Dedicated Hardware
plan instance 
in the IBM Cloud Dashboard. Or you can determine what the CRN is by using the 
ibmcloud resource
service-instance SERVICE_INSTANCE_NAME
 command.
legacyCredentials
An optional parameter that defaults to true and dictates whether the instance uses both legacy and IAM credentials or
IAM credentials only. See the 
IAM guide
 for 
more details on choosing an authentication method.
The following example command includes the extra parameters.
ibmcloud resource service-instance-create cloudant_on_ded_hardware_cli cloudantnosqldb standard us-south -p
 
'{"environment_crn":"crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b43434444bb7e2abb0841ca25d28ee4c:301a3118-7678-4d99-
b1b7-4d45cf5f7b29::","legacyCredentials":false}'
Step 5: Creating the credentials for your IBM Cloudant service
Applications that require access to your IBM Cloudant service must have the necessary credentials.
The fields for the basic command format that is used in this exercise are described in the following table.
Field
Description
NAME
Arbitrary name that you give the service credentials.
ROLE_NAME
This field currently allows the Manager role only.
 Important: 
Service credentials are valuable. If anyone or any application gains access to the credentials, they can effectively do whatever
they want with the service instance. For example, they might create spurious data, or delete valuable information. 
Protect these credentials
carefully. For more information about the fields included in the service credentials, see the 
IAM guide
.
Cloudant
   
94Table 5. Basic command format
SERVICE_INSTANCE_NAME
The name that you give to your IBM Cloudant instance.
service-endpoints
An optional parameter to populate the URL field in the Service Credentials with an internal endpoint to connect to
the service over the IBM Cloud internal network. Omit this parameter to populate the URL with an external
endpoint that 
is publicly accessible. Applies only to Standard plan instances deployed on Dedicated Hardware
environments that support internal endpoints. If the environment doesn't support internal endpoints, the result is a
400 error.
The basic command format to retrieve the credentials for a service instance within IBM Cloud is shown in the following example.
$ 
ibmcloud resource service-key-create NAME ROLE_NAME --instance-name SERVICE_INSTANCE_NAME [-p 
'{"service-
endpoints":"internal"}]
a
. 
Create credentials for the 
cs20170517a
 instance of an IBM Cloudant service, and name the credentials 
creds_for_cs20170517a
.
ibmcloud resource service-key-create creds_for_cs20170517a Manager --instance-name cs20170517a
b
. 
After you receive the request to create credentials for the service instance, review the IBM Cloud response that includes a message similar to
the following (abbreviated) example with your credentials.
$ 
Creating service key 
in
 resource group default of account John Does
's Account as john.doe@email.com...
OK
Service key crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a was created.
Name:          creds_for_cs20170517a
ID:            crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-
bc22-825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a
Created At:    Tue Sep 18 19:58:38 UTC 2018
State:         active
Credentials:
               iam_apikey_name:          auto-generated-apikey-621ffde2-ea10-4318-b297-d6d849cec48a
               iam_role_crn:   crn:v1:bluemix:public:iam::::serviceRole:Manager
               url:                      https://apikey-v2-
58B528DF5397465BB6673E1B79482A8C:5811381f6daff7255b288695c3544be63f550e975bcde46799473e69c7d48d61@f6cf0c55-48ea-4908-
b441-a962b27d3bb6-bluemix.cloudant.com
               username:                 apikey-v2-58B528DF5397465BB6673E1B79482A8C
               port:                     443
               apikey:                   XXXXX-XXXXXX_XXXXXXXXXXXXX-XXXXXXXXXXX
               host:                     f6cf0c55-48ea-4908-b441-a962b27d3bb6-bluemix.cloudant.com
               iam_apikey_description:   Auto generated apikey during resource-key operation for Instance -
 
crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42116849bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3::
               iam_serviceid_crn:        crn:v1:bluemix:public:iam-
identity::a/b42116849bb7e2abb0841ca25d28ee4c::serviceid:ServiceId-53f9e2a2-cdfb-4f90-b072-bfffafb68b3e
               password:                 581138...7d48d61
c
. 
Populate the URL with the internal endpoint, and create the credentials by using a command similar to the following example.
ibmcloud resource service-key-create creds_for_cs20170517a Manager --instance-name cs20170517a -p 
'{"service-
endpoints":"internal"}'
d
. 
Review the request response in a message similar to the following example.
$ 
Creating service key 
in
 resource group default of account John Does
's Account as john.doe@email.com...
OK
Service key crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a was created.
Name:          creds_for_cs20170517a
ID:            crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-
bc22-825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a
 Note: 
The fields for the basic command format are described in the previous table.
Cloudant
   
95Created At:    Tue Jan 02 19:58:38 UTC 2019
State:         active
Credentials:
                iam_apikey_name:          auto-generated-apikey-621ffde2-ea10-4318-b297-d6d849cec48a
                iam_role_crn:             crn:v1:bluemix:public:iam::::serviceRole:Manager
                url:                      https://2624fed5-e53e-41de-a85b-3c7d7636886f-
bluemix.private.cloudantnosqldb.appdomain.cloud
                username:                 f6cf0c55-48ea-4908-b441-a962b27d3bb6-bluemix
                apikey:                   XXXXX-XXXXXX_XXXXXXXXXXXXX-XXXXXXXXXXX
                host:                     2624fed5-e53e-41de-a85b-3c7d7636886f-
bluemix.private.cloudantnosqldb.appdomain.cloud
                iam_apikey_description:   Auto generated apikey during resource-key operation for Instance -
 
crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42116849bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3::
                iam_serviceid_crn:        crn:v1:bluemix:public:iam-
identity::a/b42116849bb7e2abb0841ca25d28ee4c::serviceid:ServiceId-53f9e2a2-cdfb-4fo0                  90-b072-
bfffafb68b3e
Step 6: Listing the service credentials for your IBM Cloudant service
The basic command format to retrieve the credentials for a service instance within IBM Cloud is shown in the following example.
ibmcloud resource service-key KEY_NAME
a
. 
Retrieve your credentials 
cs20170517a
 (where the name for the credentials is 
creds_for_cs20170517a
) by using a command similar to the
following example.
ibmcloud resource service-key creds_for_cs20170517b
b
. 
Review the IBM Cloud response that includes your credentials and a message similar to the following (abbreviated) example.
$ 
Retrieving service key 
in
 resource group default of account John Does
's Account as john.doe@email.com...
OK
Service key crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a was created.
Name:          creds_for_cs20170517a
ID:            crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42223455bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-
bc22-825c937fafa3:resource-key:621ffde2-ea10-4318-b297-d6d849cec48a
Created At:    Tue Sep 18 19:58:38 UTC 2018
State:         active
Credentials:
               iam_apikey_name:          auto-generated-apikey-621ffde2-ea10-4318-b297-d6d849cec48a
               iam_role_crn:             crn:v1:bluemix:public:iam::::serviceRole:Manager
               url:                      https://apikey-v2-
58B528DF5397465BB6673E1B79482A8C:5811381f6daff7255b288695c3544be63f550e975bcde46799473e69c7d48d61@f6cf0c55-48ea-4908-
b441-a962b27d3bb6-bluemix.cloudant.com
               username:                 apikey-v2-58B528DF5397465BB6673E1B79482A8C
               port:                     443
               apikey:                   XXXXX-XXXXXX_XXXXXXXXXXXXX-XXXXXXXXXXX
               host:                     f6cf0c55-48ea-4908-b441-a962b27d3bb6-bluemix.cloudant.com
               iam_apikey_description:   Auto generated apikey during resource-key operation for Instance -
 
crn:v1:bluemix:public:cloudantnosqldb:us-south:a/b42116849bb7e2abb0841ca25d28ee4c:ee78351d-82bf-4e80-bc22-
825c937fafa3::
               iam_serviceid_crn:        crn:v1:bluemix:public:iam-
identity::a/b42116849bb7e2abb0841ca25d28ee4c::serviceid:ServiceId-53f9e2a2-cdfb-4f90-b072-bfffafb68b3e
               password:                 581138...7d48d61
Cloudant
   
96Creating and populating a database
This tutorial shows you how to use the 
Python programming language
 to create an IBM® Cloudant® for IBM Cloud® database in your IBM Cloud
service instance. You also learn how 
to populate the database with a simple collection of data.
Objectives
This tutorial builds on a series of Python language instructions, suitable for the following tasks:
a
. 
Connecting to an IBM Cloudant service instance on IBM Cloud®.
b
. 
Creating a database within the service instance.
c
. 
Storing a small collection of data as documents within the database.
d
. 
Retrieving data.
e
. 
Deleting the database.
f
. 
Closing the connection to the service instance.
Before you begin
This tutorial provides you with the following options:
Follow each step as outlined in this tutorial.
Or 
execute the Python script
, and come back to 
Step 5. Retrieving data
.
Installing Python
a
. 
Set up service credential requirements.
a. Create a service instance and credentials by following the 
Getting started
 tutorial.
b. 
Locate your service credentials
 by following this tutorial.
b
. 
Install the required version of Python.
You must have a current version of the 
Python programming language
 that is installed on your system. [: note]
a. Check that Python is installed by running the following command at a prompt:
$ 
python3 --version
b. Verify that you get a result similar to the following example:
Python 3.8.1
c
. 
Verify that your Python Client Library meets the requirement.
a. Check that the client library installed successfully by running the following command at a prompt:
$ 
pip freeze
You get a list of all the Python modules installed on your system.
b. Inspect the list, looking for an IBM Cloudant entry similar to the following example:
 Note: 
This tutorial doesn't use the most efficient Python code. The intent is to show simple and easy-to-understand working code that you
can learn from and apply to your own applications. You must apply normal best practices for checking and handling 
all warning or error
conditions that are encountered by your own applications.
 Tip: 
Normally, you don't run commands individually in Python. You usually create a script, which is a list of the commands you want to run,
stored in a Python file, with a 
py
 extension.
 Deprecated: 
The following examples use the deprecated 
python-cloudant
 client library.
Cloudant
   
97cloudant==2.14.0
Step 1: Connecting to a service instance
You must connect to your service instance before you create a database.
The following components are identified as normal 
import
 statements.
You can follow steps 1 - 5 to learn about the individual commands, or go to the end of the tutorial to 
execute the Python script
. When you finish,
return to 
Step 5. Retrieving data
.
a
. 
Run these 
import
 statements to connect to the service instance.
from
 cloudant.client 
import
 Cloudant
from
 cloudant.error 
import
 CloudantException
from
 cloudant.result 
import
 Result, ResultByKey
b
. 
Find 
username
, 
password
, and 
URL
 in your Classic service credentials and replace 
serviceUsername
, 
servicePassword
, and
serviceURL
 in the following example.
serviceUsername = 
"apikey-v2-58B528DF5397465BB6673E1B79482A8C"
servicePassword = 
"49c0c343d225623956157d94b25d574586f26d1211e8e589646b4713d5de4801"
serviceURL = 
"https://353466e8-47eb-45ce-b125-4a4e1b5a4f7e-bluemix.cloudant.com"
c
. 
Establish a connection to the service instance.
client = Cloudant(serviceUsername, servicePassword, url=serviceURL)
client.connect()
d
. 
Or replace 
ACCOUNT_NAME
 and 
API_KEY
 with the values from your IAM API service credentials.
client = Cloudant.iam(ACCOUNT_NAME
,
 API_KEY
,
 connect=True)
Now, your Python application can access the service instance on IBM Cloud.
Step 2: Creating a database within the service instance
Next, you create a database within the service instance, called 
databasedemo
.
a
. 
Create this instance by defining a variable in the Python application.
databaseName = 
"databasedemo"
b
. 
Create the database.
myDatabaseDemo = client.create_database(databaseName)
c
. 
Verify that the database was created successfully.
if
 myDatabaseDemo.exists():
    
print
(
"'{0}' successfully created.\n"
.
format
(databaseName))
Step 3: Storing a small collection of data as documents within the database
You want to store a small, simple collection of data in the database. This data is used in other tutorials, like 
Using IBM Cloudant Query to find data
.
a
. 
Create sample data.
sampleData = [
     [
1
, 
"one"
, 
"boiling"
, 
100
],
     [
2
, 
"two"
, 
"hot"
, 
40
],
     [
3
, 
"three"
, 
"hot"
, 
75
],
     [
4
, 
"four"
, 
"hot"
, 
97
],
Cloudant
   
98     [
5
, 
"five"
, 
"warm"
, 
20
],
     [
6
, 
"six"
, 
"cold"
, 
10
],
     [
7
, 
"seven"
, 
"freezing"
, 
0
],
     [
8
, 
"eight"
, 
"freezing"
, -
5
]
]
b
. 
Use a 
for
 statement to retrieve the fields in each row by going through each row in the array.
for
 document 
in
 sampleData:
    
# Retrieve the fields in each row.
    number = document[
0
]
    name = document[
1
]
    description = document[
2
]
    temperature = document[
3
]
c
. 
Create a JSON document that represents all the data in the row.
jsonDocument = {
    
"numberField"
: number,
    
"nameField"
: name,
    
"descriptionField"
: description,
    
"temperatureField"
: temperature
}
d
. 
Create a document by using the Database API.
newDocument = myDatabaseDemo.create_document(jsonDocument)
e
. 
Check that the document exists in the database.
if
 newDocument.exists():
    
print
(
"Document '{0}' successfully created."
.
format
(number))
Step 4: Retrieving data
To perform a minimal retrieval, you first request a list of all documents within the database. This list is returned as an array. You can then show the
content of an element in the array.
a
. 
Retrieve a minimal amount of data.
result_collection = Result (myDatabaseDemo.all_docs)
print
(
"Retrieved minimal document:\n{0}\n"
.
format
(result_collection[
0
]))
b
. 
See a result similar to the following example.
[
{
 
"id"
:
 '
60e19
edf809418e407fb6791a1d8fec4'
,
 
"key"
:
 '
60e19
edf809418e407fb6791a1d8fec4'
,
 
"value"
:
 
{
  
"rev"
:
 '
2
-3
d6dc27627114431c049ddecae9796e0'
 
}
}
]
In a relational database, the first document that is stored in a database is always the first document that is returned in a list of results. This notion
doesn't necessarily apply to NoSQL databases, such as IBM Cloudant.
Full retrieval of a document
Additionally, to perform a full retrieval, you request a list of all documents within the database, and specify that the document content must also be
returned. You run a full retrieval by using the 
include_docs
 option. As before, 
the results are returned as an array. You can then show the details of
an element in the array by including the full content of the document this time.
a
. 
Request the first document that is retrieved from the database.
result_collection = Result(myDatabaseDemo.all_docs, include_docs=
True
)
Cloudant
   
99print
(
"Retrieved minimal document:\n{0}\n"
.
format
(result_collection[
0
]))
b
. 
See the result, which is similar to the following example:
[
    
{
        
"value"
:
 
{
          
"rev"
:
 
"1-b2c48b89f48f1dc172d4db3f17ff6b9a"
        
}
,
        
"id"
:
 
"14746fe384c7e2f06f7295403df89187"
,
        
"key"
:
 
"14746fe384c7e2f06f7295403df89187"
,
        
"doc"
:
 
{
            
"temperatureField"
:
 
10
,
            
"descriptionField"
:
 
"cold"
,
            
"numberField"
:
 
6
,
            
"nameField"
:
 
"six"
,
            
"_id"
:
 
"14746fe384c7e2f06f7295403df89187"
,
            
"_rev"
:
 
"1-b2c48b89f48f1dc172d4db3f17ff6b9a"
        
}
    
}
]
Step 5: Calling an IBM Cloudant API endpoint directly
You can work with the IBM Cloudant API endpoints directly, from within a Python application.
In this example code, you again request a list of all the documents, including their content. However, this time you do so by invoking the IBM
Cloudant 
/_all_docs
 
endpoint.
a
. 
Identify the endpoint to contact and any parameters to supply with it.
end_point = 
'{0}/{1}'
.
format
(serviceURL, databaseName + 
"/_all_docs"
)
params = {
'include_docs'
: 
'true'
}
b
. 
Send the request to the service instance and show the results.
response = client.r_session.get(end_point, params=params)
print
(
"{0}\n"
.
format
(response.json()))
c
. 
See the result that is similar to the following 
abbreviated
 example.
{
 
"rows"
:
 
[
{
   
"value"
:
 
{
    
"rev"
:
 
"1-b2c48b89f48f1dc172d4db3f17ff6b9a"
   
}
,
   
"id"
:
 
"14746fe384c7e2f06f7295403df89187"
,
   
"key"
:
 
"14746fe384c7e2f06f7295403df89187"
,
   
"doc"
:
 
{
    
"temperatureField"
:
 
10
,
    
"descriptionField"
:
 
"cold"
,
    
"numberField"
:
 
6
,
    
"nameField"
:
 
"six"
,
    
"_id"
:
 
"14746fe384c7e2f06f7295403df89187"
,
    
"_rev"
:
 
"1-b2c48b89f48f1dc172d4db3f17ff6b9a"
   
}
  
}
,
  ...
{
   
"value"
:
 
{
    
"rev"
:
 
"1-7130413a8c7c5f1de5528fe4d373045c"
   
}
,
   
"id"
:
 
"49baa66cc66b4dda86ffb2852ae78eb8"
,
   
"key"
:
 
"49baa66cc66b4dda86ffb2852ae78eb8"
,
   
"doc"
:
 
{
    
"temperatureField"
:
 
40
,
    
"descriptionField"
:
 
"hot"
,
    
"numberField"
:
 
2
,
    
"nameField"
:
 
"two"
,
Cloudant
   
100    
"_id"
:
 
"49baa66cc66b4dda86ffb2852ae78eb8"
,
    
"_rev"
:
 
"1-7130413a8c7c5f1de5528fe4d373045c"
   
}
  
}
 
]
,
 
"total_rows"
:
 
5
,
 
"offset"
:
 
0
}
Step 6: Deleting the database
a
. 
Delete the database.
try
 :
    client.delete_database(databaseName)
except
 CloudantException:
    
print
(
"There was a problem deleting '{0}'.\n"
.
format
(databaseName))
else
:
    
print
(
"'{0}' successfully deleted.\n"
.
format
(databaseName))
b
. 
Review the basic error handling that was included to illustrate how problems can be caught and addressed.
Step 7: Closing the connection to the service instance
a
. 
Disconnect the Python client application from the service instance.
b
. 
Run the disconnect command.
client.disconnect()
Execute the complete Python script
This script is the complete Python script for steps 2, 3, and 4. When you run the script, it connects to your service instance, creates the database,
stores a small set of data in the database, and creates JSON documents.
a
. 
In the code example in the next step, replace the values for 
serviceUsername
, 
servicePassword
, and 
serviceURL
 with the values from
your service credentials.
For more information about where to find your credentials, see 
Locating your credentials
.
b
. 
Copy the following script into a text editor and name it 
demo.py
.
#!/usr/bin/env python
# Connect to service instance by running import statements.
from
 cloudant.client 
import
 Cloudant
from
 cloudant.error 
import
 CloudantException
from
 cloudant.result 
import
 Result, ResultByKey
# Add credentials to authenticate to the service instance.
serviceUsername = 
"apikey-v2-58B528DF5397465BB6673E1B79482A8C"
servicePassword = 
"680b037145f9dc8ef9e6a6d8b480783cbc1d1c12e71a0f4ced6b1eee30a243cd"
serviceURL = 
"serviceURL = "
https://0c869093-c3ee-4a3f-bcec-00f01c8df8d8-bluemix.cloudantnosqldb.appdomain.cloud
""
databaseName = 
"databasedemo"
# Define sample data.
sampleData = [
    [
1
, 
"one"
, 
"boiling"
, 
100
],
    [
2
, 
"two"
, 
"hot"
, 
40
],
    [
3
, 
"three"
, 
"hot"
, 
75
],
    [
4
, 
"four"
, 
"hot"
, 
97
],
    [
5
, 
"five"
, 
"warm"
, 
20
],
    [
6
, 
"six"
, 
"cold"
, 
10
],
    [
7
, 
"seven"
, 
"freezing"
, 
0
],
    [
8
, 
"eight"
, 
"freezing"
, -
5
]
]
Cloudant
   
101def
 
main
():
    
# Establish a connection with the service instance.
    client = Cloudant(serviceUsername, servicePassword, url=serviceURL)
    client.connect()
    
# Create database and verify it was created.
    myDatabaseDemo = client.create_database(databaseName)
    
if
 myDatabaseDemo.exists():
        
print
(
"'{0}' successfully created.\n"
.
format
(databaseName))
    
for
 document 
in
 sampleData:
        
# Retrieve the fields in each row.
        number = document[
0
]
        name = document[
1
]
        description = document[
2
]
        temperature = document[
3
]
        
#  Create a JSON document that represents all the data in the row.
        jsonDocument = {
            
"numberField"
: number,
            
"nameField"
: name,
            
"descriptionField"
: description,
            
"temperatureField"
: temperature
        }
        
# Create a document by using the Database API.
        newDocument = myDatabaseDemo.create_document(jsonDocument)
        
# Check that the documents exist in the database.
        
if
 newDocument.exists():
            
print
(
"Document '{0}' successfully created."
.
format
(number))
if
 __name__==
'__main__'
:
    main()
c
. 
From the command line, run 
demo.py
 by typing a command similar to the following one.
python3 demo.py
Once you run the script, return to 
Step 5. Retrieving data
 to complete the tutorial.
Cloudant
   
102Using IBM Cloudant Query
In this tutorial, we demonstrate how to create an index and use the index to query the database. You also learn to create different types of queries to
more easily find data.
Here you run the commands from the command line, but you can also complete these tasks with the IBM® Cloudant® for IBM Cloud® Dashboard,
which gives you a visual example of each task. For more information about the dashboard, see 
Using the IBM Cloudant Dashboard
 
tutorial.
Before you begin
Before you begin, follow these tutorials to create an instance, and then create and populate a database.
a
. 
Create an IBM Cloudant instance
.
b
. 
Create a database
.
c
. 
Populate the database
.
d
. 
(Optional) 
Create an 
acurl
 alias
.
If you decide not to set up 
acurl
, use the following URL with 
curl
 instead of the one provided in the exercises, 
curl
"https://$USERNAME:$PASSWORD@$ACCOUNT.cloudant.com/databasedemo"
.
The 
acurl
 alias is more secure. It prevents someone from reading your password over your shoulder as you type. It also makes sure that your
password isn’t sent in plain text over the network by enforcing HTTPS.
Now, we're ready to learn how to run queries against the database you created in step two of 
Before you begin
.
Step 1: Creating an index
IBM Cloudant Query uses Mongo-style query syntax to search for documents by using logical operators. IBM Cloudant Query is a combination of a
view and a search index.
When you use IBM Cloudant Query, the query planner looks at the selector (your query) to determine the correct index to choose from. In memory,
you filter out the documents by the selector, which is why, even without an index, you can still 
query with various fields.
To create an index, follow these steps:
a
. 
Copy the following sample JSON data into a file named 
query-demo-index.json
:
  
{
   
"index"
:
 
{
    
"fields"
:
 
[
     
"descriptionField"
,
     
"temperatureField"
    
]
,
    
"partial_filter_selector"
:
 
{
     
"descriptionField"
:
 
{
      
"$eq"
:
 
"hot"
     
}
,
     
"temperatureField"
:
 
{
      
"$gt"
:
 
50
     
}
    
}
   
}
,
   
"ddoc"
:
 
"query-demo-index"
,
   
"type"
:
 
"json"
  
}
b
. 
Run the following command to create an index:
  acurl 
"https://
$ACCOUNT
.cloudant.com/databasedemo/_index"
 \
    -X POST \
    -H 
"Content-Type: application/json"
 \
 Tip: 
If no available defined index matches the specified query, then IBM Cloudant uses the 
_all_docs
 index, which looks up documents by
ID. In the worst case scenario, it returns all the documents by ID (full table scan). Full table 
scans are expensive to process. It is
recommended that you create an index.
Cloudant
   
103    -d \@query-demo-index.json
c
. 
Review the results:
  
{
   
"result"
:
 
"created"
,
   
"id"
:
 
"_design/query-demo-index"
,
   
"name"
:
 
"490441584f9eddb8d09ef234d636b5f3b18e4ce6"
  
}
You aren't required to create an index to run a query. However, if you don't, the following warning is included with your results as an indicator that
creating an index reduces processing and makes your queries more effective. 
"Warning": "No matching index found, create an index to
optimize query time."
Step 2: Running a simple query
This example demonstrates how IBM Cloudant Query finds documents based on the 
descriptionField
 with the value 
boiling
.
To run the query, follow these steps:
a
. 
Copy the following sample JSON into a data file named 
query1.json
:
 
{
  
"selector"
:
 
{
    
"descriptionField"
:
 
"boiling"
   
}
 
}
b
. 
Run the following command to query the database:
  acurl 
"https://
$ACCOUNT
.cloudant.com/databasedemo/_find"
 \
    -X POST \
    -H 
"Content-Type: application/json"
 \
    -d \@query1.json
c
. 
Review the query results:
  
{
   
"docs"
:
 
[
{
    
"_id"
:
 
"91d1fa833d28efe15069604f98de701d"
,
    
"_rev"
:
 
"1-f998fc7b89d4466c1e7bb204b1b00f74"
,
  
"numberField"
:
 
1
,
    
"nameField"
:
 
"one"
,
    
"descriptionField"
:
 
"boiling"
,
    
"temperatureField"
:
 
100
    
}
]
,
   
"bookmark"
:
  
"g1AAAABweJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYorWBqmGKYlWhgbpxhZpKalGpoamFmaGZikWVqkpJobGKaA9HHA9BGlIwsAmn8eLw"
,
   
"warning"
:
 
"No matching index found, create an index to optimize query time."
   
}
Next, you find a document in the database by using two fields.
Step 3: Running a query with two fields
This example uses two fields to find a document with the values: 
freezing
 and 
-5
.
The search is described by using a 
'selector' expression
 that looks like the following example:
  
{
   
"selector"
:
 
{
    
"descriptionField"
:
 
"freezing"
,
    
"temperatureField"
:
 
-5
   
}
  
}
Cloudant
   
104You can tailor the results by adding more details within the selector expression. The 
fields
 parameter specifies the fields to include with the
results. In our example, the results include the 
nameField
, 
descriptionField
, 
and 
temperatureField
, as shown in the following example.
$ 
  
{
   ...
   
"fields"
:
 
[
    
"nameField"
,
    
"descriptionField"
,
    
"temperatureField"
   
]
  
}
To run the query, follow these steps:
a
. 
Copy the sample JSON into a data file named 
query2.json
.
  
{
   
"selector"
:
 
{
    
"descriptionField"
:
 
"freezing"
,
    
"temperatureField"
:
 
-5
   
}
,
   
"fields"
:
 
[
    
"nameField"
,
    
"descriptionField"
,
    
"temperatureField"
   
]
  
}
b
. 
Run the following command to query the database:
  acurl 
"https://
$ACCOUNT
.cloudant.com/databasedemo/_find"
 \
    -X POST \
    -H 
"Content-Type: application/json"
 \
    -d \@query2.json
c
. 
Review the query results:
{
 
"docs"
:
 
[
{
  
"nameField"
:
 
"eight"
,
  
"descriptionField"
:
 
"freezing"
,
  
"temperatureField"
:
 
-5
 
}
]
,
 
"bookmark"
:
 
"g1AAAABweJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYorpBiYGJolWaSZmaWYpFqmGBiYmKclphhappqZmRglG5uD9HHA9BGlIwsAms8eJw"
,
 
"warning"
:
 
"No matching index found, create an index to optimize query time."
}
Next, you find a document in the database by using multiple operators.
Step 4: Running a query with operators
In this example, the 
$gt
 (greater than) and 
$eq
 (equal) operators are used to search for documents that include a temperature that is greater than
20
 degrees and a description that contains the value 
hot
. 
The results include the 
descriptionField
 and 
temperatureField
, shown in
descending order by temperature.
You use a selector expression like the following example:
  
{
   
"selector"
:
 
{
    
"temperatureField"
:
 
{
     
"$gt"
:
 
50
    
}
,
    
"descriptionField"
:
 
{
     
"$eq"
:
 
"hot"
    
}
   
}
,
Cloudant
   
105   
"fields"
:
 
[
    
"descriptionField"
,
    
"temperatureField"
   
]
,
   
"sort"
:
 
[
{
    
"temperatureField"
:
 
"desc"
   
}
]
,
   
"use_index"
:
 
"_design/query-demo-index"
  
}
To run the query, follow these steps:
a
. 
Copy the following sample JSON to a file named 
query3.json
.
  
{
   
"selector"
:
 
{
    
"descriptionField"
:
 
{
     
"$eq"
:
 
"hot"
    
}
,
    
"temperatureField"
:
 
{
     
"$gt"
:
 
50
    
}
   
}
,
   
"fields"
:
 
[
    
"descriptionField"
,
    
"temperatureField"
   
]
,
   
"sort"
:
 
[
{
    
"temperatureField"
:
 
"desc"
   
}
]
,
   
"use_index"
:
 
"_design/query-demo-index"
  
}
b
. 
Run this query:
  acurl 
"https://
$ACCOUNT
.cloudant.com/databasedemo/_find"
 \
    -X POST \
    -H 
"Content-Type: application/json"
 \
    -d \@query3.json
c
. 
Review the query results:
{
 
"docs"
:
 
[
{
   
"descriptionField"
:
 
"hot"
,
   
"temperatureField"
:
 
97
  
}
,
  
{
   
"descriptionField"
:
 
"hot"
,
   
"temperatureField"
:
 
75
  
}
 
]
,
 
"bookmark"
:
 
"g1AAAABbeJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYorJBoYmKWaWVokpZkamJtaGJskm5slmSenGhulWpibJhqC9HHA9OWATErUAGlkzsgvycoCAE
sUF_A"
}
Now you know how to extract data from your database by using IBM Cloudant Query. For more information, see the 
IBM Cloudant documentation
.
Cloudant
   
106Creating a backup
This tutorial demonstrates how to use the 
CouchBackup
 utility to back up and restore a CouchDB or IBM® Cloudant® for IBM Cloud® instance.
CouchBackup backs up the database to a file. If 
the database fails, you can use the backup file to restore the information to an existing database.
Objectives
a
. 
Install CouchBackup.
b
. 
Create a sample database with documents.
c
. 
Set an environment variable.
d
. 
Back up a database.
e
. 
Create a log file.
f
. 
Restore a backup from a text file.
Step 1: Installing CouchBackup
Install CouchBackup by running the 
install
 command.
npm install -g @cloudant/couchbackup
Step 2: Creating a sample database
Create a sample 
couchbackup-demo
 database for use with this tutorial.
a
. 
Create a database by running this command.
curl 
"https://username:password@myhost.cloudant.com/couchbackup-demo"
 -X PUT
b
. 
Review the results.
{
  
"ok"
:
 
true
}
Step 3: Creating documents in the sample database
The documents that you create in this exercise contain the data that you back up and restore in later exercises.
a
. 
Copy the sample text to a data file named 
bulkcreate.dat
 to create all five documents.
{
    
"docs"
:
 
    
[
        
{
 
            
"_id"
:
 
"doc1"
,
            
"firstname"
:
 
"Sally"
,
            
"lastname"
:
 
"Brown"
,
            
"age"
:
 
16
,
            
"location"
:
 
"New York City, NY"
        
}
,
        
{
 
            
"_id"
:
 
"doc2"
,
            
"firstname"
:
 
"John"
,
            
"lastname"
:
 
"Brown"
,
            
"age"
:
 
21
,
            
"location"
:
 
"New York City, NY"
        
}
,
        
{
            
"_id"
:
 
"doc3"
,
            
"firstname"
:
 
"Greg"
,
            
"lastname"
:
 
"Greene"
,
            
"age"
:
 
35
,
            
"location"
:
 
"San Diego, CA"
        
}
,
Cloudant
   
107        
{
            
"_id"
:
 
"doc4"
,
            
"firstname"
:
 
"Anna"
,
            
"lastname"
:
 
"Greene"
,
            
"age"
:
 
44
,
            
"location"
:
 
"Baton Rouge, LA"
        
}
,
        
{
            
"_id"
:
 
"doc5"
,
            
"firstname"
:
 
"Lois"
,
            
"lastname"
:
 
"Brown"
,
            
"age"
:
 
33
,
            
"location"
:
 
"Syracuse, NY"
        
}
    
]
}
b
. 
Run this command to create the documents.
curl 
"https://username:password@myhost.cloudant.com/couchbackup-demo/_bulk_docs"
 -X POST -H 
"Content-Type:
 
application/json"
 -d \@bulkcreate.dat
c
. 
Review the results.
[
  
{
    
"ok"
:
 
true
,
    
"id"
:
 
"doc1"
,
    
"rev"
:
 
"1-57a08e644ca8c1bb8d8931240427162e"
  
}
,
  
{
    
"ok"
:
 
true
,
    
"id"
:
 
"doc2"
,
    
"rev"
:
 
"1-bf51eef712165a9999a52a97e2209ac0"
  
}
,
  
{
    
"ok"
:
 
true
,
    
"id"
:
 
"doc3"
,
    
"rev"
:
 
"1-9c9f9b893fcdd1cbe09420bc4e62cc71"
  
}
,
  
{
    
"ok"
:
 
true
,
    
"id"
:
 
"doc4"
,
    
"rev"
:
 
"1-6aa4873443ddce569b27ab35d7bf78a2"
  
}
,
  
{
    
"ok"
:
 
true
,
    
"id"
:
 
"doc5"
,
    
"rev"
:
 
"1-d881d863052cd9681650773206c0d65a"
  
}
]
Step 4: Setting an environment variable
You can use environment variables or options to specify the URL and database for the CouchDB or IBM Cloudant instance that you want to work with
CouchBackup.
In this tutorial, you set the 
COUCH_URL
 and specify the database by using the 
--db
 parameter.
Set the 
COUCH_URL
 environment variable to specify the URL for the CouchDB or IBM Cloudant instance.
export
 COUCH_URL=https://username:password@myhost.cloudant.com
Step 5: Backing up a database
The CouchBackup utility backs up your database to a text file to preserve your data and make it easier to restore.
Cloudant
   
108a
. 
Run the 
couchbackup
 command to direct the contents of your database to a text file.
couchbackup --db couchbackup-demo > couchbackup-demo-backup.txt
b
. 
Review the results.
================================================================================
Performing backup on https://****:****@myhost.cloudant.com/couchbackup-demo using configuration:
{
    
"bufferSize"
: 500,
    
"log"
: 
"/var/folders/r7/vtctv4695hj_njxmr2hj4jyc0000gn/T/tmp-3132gHPWk9A9yGVe.tmp"
,
    
"mode"
: 
"full"
,
    
"parallelism"
: 5
}
================================================================================
Streaming changes to disk:
 batch 0
    couchbackup:backup written 0  docs:  5 Time 0.604 +0ms
    couchbackup:backup finished { total: 5 } +4ms
c
. 
Check the directory to verify that the 
couchbackup-demo-backup.txt
 file was created.
d
. 
Open the file and review the list of documents that are backed up from the database.
[
    
{
      
"_id"
:
 
"doc2"
,
      
"_rev"
:
 
"1-2c5ee70689bb75af6f65b0335d1c92f4"
,
      
"firstname"
:
 
"John"
,
      
"lastname"
:
 
"Brown"
,
      
"age"
:
 
21
,
      
"location"
:
 
"New York City, NY"
,
      
"_revisions"
:
 
{
        
"start"
:
 
1
,
        
"ids"
:
 
[
          
"2c5ee70689bb75af6f65b0335d1c92f4"
        
]
      
}
    
}
,
    
{
      
"_id"
:
 
"doc3"
,
      
"_rev"
:
 
"1-f6055e3e09f215c522d45189208a1bdf"
,
      
"firstname"
:
 
"Greg"
,
      
"lastname"
:
 
"Greene"
,
      
"age"
:
 
35
,
      
"location"
:
 
"San Diego, CA"
,
      
"_revisions"
:
 
{
        
"start"
:
 
1
,
        
"ids"
:
 
[
          
"f6055e3e09f215c522d45189208a1bdf"
        
]
      
}
    
}
,
    
{
      
"_id"
:
 
"doc1"
,
      
"_rev"
:
 
"1-cce7796c7113c5498b07d8e11d7e0c12"
,
      
"firstname"
:
 
"Sally"
,
      
"lastname"
:
 
"Brown"
,
      
"age"
:
 
16
,
      
"location"
:
 
"New York City, NY"
,
      
"_revisions"
:
 
{
        
"start"
:
 
1
,
        
"ids"
:
 
[
          
"cce7796c7113c5498b07d8e11d7e0c12"
        
]
      
}
    
}
,
    
{
Cloudant
   
109      
"_id"
:
 
"doc4"
,
      
"_rev"
:
 
"1-0923b723c62fe5c15531e0c33e015148"
,
      
"firstname"
:
 
"Anna"
,
      
"lastname"
:
 
"Greene"
,
      
"age"
:
44
,
      
"location"
:
 
"Baton Rouge, LA"
,
      
"_revisions"
:
 
{
        
"start"
:
 
1
,
        
"ids"
:
 
[
          
"0923b723c62fe5c15531e0c33e015148"
        
]
      
}
    
}
,
    
{
        
"_id"
:
 
"doc5"
,
        
"_rev"
:
 
"1-19f7ecbc68090bc7b3aa4e289e363576"
,
        
"firstname"
:
 
"Lois"
,
        
"lastname"
:
 
"Brown"
,
        
"age"
:
 
33
,
        
"location"
:
 
"Syracuse, NY"
,
        
"_revisions"
:
 
{
            
"start"
:
 
1
,
            
"ids"
:
 
[
              
"19f7ecbc68090bc7b3aa4e289e363576"
            
]
        
}
    
}
]
Step 6: Creating a log file
A log file records the progress of your backup. With CouchBackup, you use the 
--log
 parameter to create the log file. You can also use it to restart a
backup from where it stopped and specify the output file name.
The 
couchbackup
 command uses these parameters to specify the database, log file, and resume option.
--db
couchbackup-demo
--log
couchbackup-demo.log
--resume
true
a
. 
Run the 
couchbackup
 command to create a log file.
couchbackup --db couchbackup-demo --
log
 couchbackup-demo-backup.log > couchbackup-demo-backup-log.txt
b
. 
Review the results.
================================================================================
Performing backup on https://****:****@myhost.cloudant.com/couchbackup-demo using configuration:
    {
      
"bufferSize"
: 500,
      
"log"
: 
"couchbackup-demo-backup.log"
,
      
"mode"
: 
"full"
,
      
"parallelism"
: 5
    }
================================================================================
Streaming changes to disk:
 batch 0
    [{
"_id"
:
"doc2"
,
"_rev"
:
"1-2c5ee70689bb75af6f65b0335d1c92f4"
,
        
"firstname"
:
"John"
,
"lastname"
:
"Brown"
,
"age"
:21,
        
"location"
:
"New York City, NY"
,
Cloudant
   
110        
"_revisions"
:{
"start"
:1,
"ids"
:[
"2c5ee70689bb75af6f65b0335d1c92f4"
]}},
    {
"_id"
:
"doc4"
,
"_rev"
:
"1-0923b723c62fe5c15531e0c33e015148"
,
        
"firstname"
:
"Anna"
,
"lastname"
:
"Greene"
,
"age"
:44,
        
"location"
:
"Baton Rouge, LA"
,
        
"_revisions"
:{
"start"
:1,
"ids"
:[
"0923b723c62fe5c15531e0c33e015148"
]}},
    {
"_id"
:
"doc1"
,
"_rev"
:
"1-cce7796c7113c5498b07d8e11d7e0c12"
,
        
"firstname"
:
"Sally"
,
"lastname"
:
"Brown"
,
"age"
:16,
        
"location"
:
"New York City, NY"
,
        
"_revisions"
:{
"start"
:1,
"ids"
:[
"cce7796c7113c5498b07d8e11d7e0c12"
]}},
    {
"_id"
:
"doc5"
,
"_rev"
:
"1-19f7ecbc68090bc7b3aa4e289e363576"
,
        
"firstname"
:
"Lois"
,
"lastname"
:
"Brown"
,
"age"
:33,
        
"location"
:
"Syracuse, NY"
,
        
"_revisions"
:{
"start"
:1,
"ids"
:[
"19f7ecbc68090bc7b3aa4e289e363576"
]}},
    {
"_id"
:
"doc3"
,
"_rev"
:
"1-f6055e3e09f215c522d45189208a1bdf"
,
        
"firstname"
:
"Greg"
,
"lastname"
:
"Greene"
,
"age"
:35,
        
"location"
:
"San Diego, CA"
,
        
"_revisions"
:{
"start"
:1,
"ids"
:[
"f6055e3e09f215c522d45189208a1bdf"
]}}]
            couchbackup:backup written 0  docs:  5 Time 0.621 +0ms
            couchbackup:backup finished { total: 5 } +4ms
c
. 
Open the log file, 
couchbackup-demo-backup.log
, and review the actions that are taken during the backup or restore.
:t batch0 [
    {
"id"
:
"doc1"
},
    {
"id"
:
"doc5"
},
    {
"id"
:
"doc3"
},
    {
"id"
:
"doc4"
},
    {
"id"
:
"doc2"
}  ]
:changes_complete 5-g1AAAAXkeJyl1MFNwzAUBmBDk
    RAnugEc4Nji2ImTnOgGsAH4-dkqVZoi1J5hA9gANoA
    NYAPYADaADUqMEYlBIWl7caTI-l7e_-xkhJDusINkD
    0FNLvQAIenDuKdUD2XWo7yvsskMZT7t53qaFbvXJYH
    t-Xw-GnYkGRcvNsM0lRwAydYsR23Oco2-GDWI0C1W2
    PFQFCYwKf2N7v-gAWtSd6168K2ufaksoQwD3dbx2wi
    aClJb8NBvQyVIk6Q-m6a0YWDRIw8NKA85M_Vo2IQe
    W_TEi0YIGiETLZlFZ3FqC068LqgBpHFQ30Vj3ucWv
    fRQYTAGwZbPO98oVnJVPAr3uoSTIGYcw3qYt4JvHHx
    b-WIpIqpwhYPu5Dsn35eyxNRI-c-9bArYwQ8OfqwcFY
    ghEdCSWib_J1fz2dZcdxcpAh2lpiW1zGheXM3XMsBY
    CcHonxO68GjenPxeyopyrXW86mg-HFz9NZiQh1FUhUefOhzMIg
:d batch0
Step 7: Restoring from a backup text file
From the 
couchbackup-demo-backup.txt
 file, you can restore your data to a new, empty database by using the 
couchrestore
 command.
a
. 
(Prerequisite) Create a new, empty database where you can restore your data.
curl 
"https://username:password@myhost.cloudant.com/couchbackup-demo-restore"
 -X PUT
b
. 
Run the 
couchrestore
 command.
cat couchbackup-demo-backup.txt | couchrestore --db couchbackup-demo-restore
c
. 
Review the results.
================================================================================
Performing restore on https://****:****@myhost.cloudant.com/couchbackup-demo-restore using configuration:
{
  
"bufferSize"
: 500,
  
"parallelism"
: 5
 Tip: 
Restoring a backup is only supported when you restore into an empty database. If you delete all documents from a database, document
deletion records are still present for replication consistency purposes. A database that contains only deleted 
documents is not considered
empty, and so cannot be used as the target when you restore a backup.
Cloudant
   
111}
================================================================================
  couchbackup:restore restored 5 +0ms
  couchbackup:restore finished { total: 5 } +1ms
You completed the backup and restore of a database and created a log file. For more information, see 
Disaster recovery and backup
, 
Configuring
IBM Cloudant for cross-region disaster recovery
, and 
IBM Cloudant backup and recovery
.
Cloudant
   
112Locating your Db2 Warehouse on Cloud credentials
To find alternatives to IBM Cloudant's IBM® Db2® Warehouse on Cloud feature, see the 
data-flow-examples repository
 for tutorials on extracting IBM
Cloudant documents and writing the data to a Db2 Warehouse on Cloud table.
Before you can sign in to the Db2 Warehouse on Cloud console, you need the URL and credentials. This information is located in the 
warehouser
document.
Objectives
a
. 
Locate your Db2 Warehouse on Cloud credentials.
b
. 
Sign in to Db2 Warehouse on Cloud console.
Step 1: How to find your service credentials
a
. 
To retrieve information from the 
warehouser
 document, you must run the following curl command.
curl -u 
$USERNAME
:
$PASSWORD
 
"https://
$ACCOUNT
.cloudant.com/_warehouser/
$DOCUMENT_ID
"
b
. 
Before you run the command, replace 
$DOCUMENT_ID
 with 
example@source-db
. In this case, 
example
 is the 
warehouser
 document's
name. 
source-db
 is the source database's name that 
is used for replicating IBM Cloudant to DB2.
curl -u 
$USERNAME
:
$PASSWORD
 
"https://
$ACCOUNT
.cloudant.com/_warehouser/example@source-db"
c
. 
See the example response when you search for information in the 
warehouser
 document.
{
  "_id": "example@source-db",
  "dashboard_url": "https://dashdb-entry-yp-lon02-01.services.eu-gb.bluemix.net/login",
  "dynamite_token": "XXXXXXXX",
  "target": "jdbc:db2://dashdb-entry-yp-lon02-01.services.eu-gb.bluemix.net:50000/BLUDB",
  "dynamite_user": "dash12345",
  ...
}
The information that is returned in the previous example is described in the following list:
_id
ID of the 
_warehouser
 document.
dashboard_url
URL of the Db2 Warehouse on Cloud console.
dynamite_token
DB2 password.
target
DB2 JDBC connection URL, only used if the value for 
dashboard_url
 is null.
dynamite_user
DB2 username.
Step 2: Sign in to the Db2 Warehouse on Cloud console
a
. 
To sign in to the Db2 Warehouse on Cloud console, you must remember the values for each of the following fields that are taken from the
previous response example: 
dynamite_user
, 
dynamite_token
, and 
dashboard_url
.
 Deprecated: 
This tutorial shows you how to find your Db2 Warehouse on Cloud credentials. Keep in mind that the Db2 Warehouse on Cloud
feature is deprecated.
Cloudant
   
113b
. 
From a browser, go to the Db2 Warehouse on Cloud console by using the value in the 
dashboard_url
 field.
c
. 
To sign in, use the value of the 
dynamite_user
 field as your username and the 
dynamite_token
 field as your password.
 Note: 
To sign in to the Db2 Warehouse on Cloud console, use the value from the 
dashboard_url
 field. If the value for the
dashboard_url
 field is 
null
, you can use the host value from the 
target
 
field to create the URL for signing in to the console. For
example, the host value for the 
target
 field from the previous example output is 
dashdb-entry-yp-lon02-01.services.eu-
gb.bluemix.net
. If you add the protocol 
https
 and the Postfix 
login
, you can sign in with the following URL, 
https://dashdb-
entry-yp-lon02-01.services.eu-gb.bluemix.net/login
.
Cloudant
   
114Using IBM Cloudant
If you never use IBM Cloudant or NoSQL databases in general, scan this introduction and some best practices before you read further. It describes
the most important things you need to know about IBM Cloudant and how to use it best. The rest of 
the documentation assumes that you know these
basics.
You can find more information about IBM Cloudant in the following sections:
Client Libraries
API and SDK reference
Connecting to IBM Cloudant
To access IBM Cloudant, you must have an 
IBM Cloud® account
.
HTTP API
All requests to IBM Cloudant go over the web. This statement means that any system that can speak to the web can speak to IBM Cloudant. All
language-specific libraries for IBM Cloudant are just wrappers that provide some convenience and linguistic 
niceties to help you work with a simple
API. Many users choose to use raw HTTP libraries for working with IBM Cloudant.
For more information about how IBM Cloudant uses HTTP, see 
HTTP
 in the API reference.
IBM Cloudant supports the following HTTP request methods:
GET
Request the specified item. As with normal HTTP requests, the format of the URL defines what is returned. With IBM Cloudant, this definition
can include static items, database documents, and configuration and statistical information. In most 
cases, the information is returned in the
form of a JSON document.
HEAD
The 
HEAD
 method retrieves the HTTP header of a 
GET
 request without the body of the response.
POST
Upload data. In IBM Cloudant's API, the 
POST
 method sets values, uploads documents, sets document values, and starts some administration
commands.
PUT
Used to "store" a specific resource. In IBM Cloudant's API, 
PUT
 creates new objects, including databases, documents, views, and design
documents.
DELETE
Deletes the specified resource, including documents, views, and design documents.
COPY
A special method that copies documents and objects.
If the client (such as some web browsers) doesn't support the use of HTTP methods, 
POST
 can be used instead with the 
X-HTTP-Method-Override
request header set to the actual HTTP method.
Method not allowed error
If you use an unsupported HTTP request type with a URL that doesn't support the specified type, a 
405
 error is returned. The error that lists the
supported 
HTTP methods, as shown in the following example.
Example error message in response to an unsupported request
{
    
"error"
:
"method_not_allowed"
,
    
"reason"
:
"Only GET,HEAD allowed"
}
Cloudant
   
115JSON
IBM Cloudant stores documents that use JSON (JavaScript Object Notation) encoding, so anything encoded into JSON can be stored as a document.
Files that include media, such as images, videos, and audio, are called BLOBs (Binary Large Objects). 
BLOBs can be stored as attachments
associated with documents.
More information about JSON can be found in the 
JSON Guide
.
Distributed systems
By using IBM Cloudant's API, you can interact with a collaboration of numerous machines, called a cluster. The machines in a cluster must be in the
same datacenter, but can be within different "pods" in that datacenter. Using different 
pods helps improve the High Availability characteristics of IBM
Cloudant.
An advantage of clustering is that when you need more computing capacity, you add more machines. This method is often more cost-effective and
fault-tolerant than scaling up or enhancing an existing single machine.
For more information about IBM Cloudant and distributed system concepts, see the 
CAP Theorem
 guide.
Replication
Replication
 is a procedure followed by IBM Cloudant, 
CouchDB
, 
PouchDB
, and other distributed databases. Replication synchronizes the state of
two databases so that their contents are identical.
You can replicate continuously. Continuous replication means that a target database updates every time the source database changes. Continuous
replication can be used for backups of data, aggregating data across many databases, or for sharing 
data.
However, continuous replication means testing continuously for any source database changes. This testing requires continuous internal calls, which
might impact performance or the cost of using the database.
Using the proper tool for the job
IBM Cloudant is a scalable, durable, highly available, operational JSON document store with an HTTP API. It's suitable for the following purposes:
Powering your always-on web application.
Being the server-side data store for mobile applications.
Storing time-series data in time-boxed databases before you archive to object storage and delete the original.
Storing application objects as JSON while queries are delivered from secondary indexes.
Replicating data sets across geographies for disaster recovery, extra capacity, or moving data nearer to your users.
IBM Cloudant doesn't include the following features:
Low latency, in-memory data store. For more information, see 
IBM Cloud® Databases for Redis
.
Limitless object store for archiving data. For more information, see 
IBM Cloud Object Storage
.
Relational database with SQL querying, stored procedures, and constraints and triggers. For more information, see 
IBM Cloud Databases for
PostgreSQL
.
Data warehouse for ad hoc querying. For more information, see 
IBM® Db2® Warehouse on Cloud
.
A queue. For more information, see 
IBM MQ
.
For more information, see the 
Best and worst practice
 blog.
Organizing documents and databases
IBM Cloudant data is organized in a hierarchy of databases and documents. A document is a JSON object with a unique identifier: its 
_id
. A
database is a collection of documents with a primary index that allows documents to be retrieved 
by 
_id
. It also has optional secondary indexes
that allow documents to be queried by other attributes in the object.
When developers start a project, they sometimes struggle with the following questions:
How much data can I put into a single object?
 Note: 
Continuous replication can result in many internal calls. These calls might affect costs for multi-tenant users of IBM Cloudant systems.
Continuous replication is disabled by default.
Cloudant
   
116Must I store different document types in the same collection or one database per document type?
It is important for a document to include all the data about an object that is modeled by your application, for example, a user, an order, or a product.
This practice ensures you fetch the entire object from the database in one API call. IBM 
Cloudant doesn't have the concept of 
joins
 like a relational
database, so data isn't 
normalized
. However, data can repeat across objects. For example, an 
order
 document can include a subset of the 
product
documents that were purchased.
It's common to store several object types in the same database: a convention is that a 
type
 attribute is used to denote the object type. This option
is a good one if you need to perform queries that return several object types or 
if a database needs to be replicated to another location altogether.
Otherwise, separate databases, for example, 
users
, 
orders
, 
products
, might be better so that secondary indexes are specific to each 
object
type.
If you're storing arrays of objects within a document, consider whether the array items must really be their own document. For example, a 
product
and each 
product review
 must be stored in separate documents, but a 
user
 
and each of that user's 
orders
 must have their own document.
If you have an ever-growing data set, then you probably don't want to store data in a single, ever-growing database. Data is best stored in 
time-boxed
databases
 that allow older data to be archived and deleted cleanly. Deleting an IBM 
Cloudant document leaves a 
tombstone
 document behind, so
don't rely on deleting documents to recover disk space. Instead, you must rely on deleting whole databases.
JSON doesn't offer a native way to store dates or timestamps. Choose your 
date format
 carefully if you intend to query it later.
The maximum document size is 1 MB, but documents must be much smaller than that size, typically a few KB.
For more information, see the following blog posts:
Optimal IBM Cloudant Indexing
Time-series Data Storage
Partitioned databases - data design
Making the most of the primary index
IBM Cloudant has a primary index on the document's 
_id
 attribute. This index allows documents to be retrieved by 
_id
 (
GET /db/id
) or a range
of 
_ids
 (
GET /db/_all_docs?startkey="a"&endkey="z"
). 
By storing data in the primary key and ensuring that each 
_id
 is unique, the primary
index can be used to fetch documents and ranges of documents without secondary indexing. See the following list of ideas:
If you have something unique in your object that would be useful to query against, use it as your 
_id
 field, for example,
bob.smith@gmail.com
, 
isbn9780241265543
, or 
oakland,ca
.
If your objects contain a hierarchy, model that in your 
_id
: 
usa:ca:oakland
 or 
books:fiction:9780241265543
. The hierarchy goes from
largest to smallest, so you can use the primary index to find 
all the cities in 
usa
 
or 
all the cities in 
usa:ca
, without secondary indexing.
If you're storing time-series data, encoding time at the start of your 
_id
 sorts the primary index by time, for example,
001j40Ox1b2c1B2ubbtm4CsuLB4L35wQ
.
Partitioned databases group documents that share a partition key together. A partition key must have many values and must not include hot
spots to avoid directing a large proportion of your application's traffic to a few partitions.
For more information, see the following blog posts:
Time-sortable _ids
Introduction to partitioned databases
Querying and secondary indexes
IBM Cloudant allows queries to run against a single database that returns an array of matching documents and a bookmark, which allows access to
the next block of search results. Achieving better query performance depends on having your queries 
that are supported by suitable secondary
indexes. An index allows the database to answer a query without having to trawl through every document in the database, yielding much faster
performance.
See the following tips:
It's sometimes difficult to measure the performance of your queries until your data set is large enough to expose slow operations. Generate
enough realistic data so that you can test your indexing and query performance before you get to production.
IBM Cloudant might return data to you without an index, but you must never rely on this data for production workloads. If your result set
includes the warning, 
No matching index found. Create an index to optimize query time,
 then 
you need to revisit your indexing
strategy. Use the 
explain
 feature to see which index is being selected for each query.
With several object types in the same database, many use cases can be serviced by a few indexes on fixed attributes. For more information,
see 
Optimal IBM Cloudant Indexing
.
Cloudant
   
117Give your indexes meaningful names, and specify the index name at query-time, so that it's obvious which index corresponds to which of your
application's queries.
For more information, see the following blog posts:
Generating sample data
Optimal IBM Cloudant Indexing
Cloudant
   
118Managing your accounts
Working with your IBM Cloudant account
Your account is your entry point for the IBM® Cloudant® for IBM Cloud® API. You access your account by using the address prefix
https://$ACCOUNT.cloudant.com
.
For your IBM Cloudant Dashboard, you always use this address: 
https://$ACCOUNT.cloudant.com/dashboard.html
.
If you don't have an account yet, sign in to 
IBM Cloudant
.
To see whether your IBM Cloudant account is accessible, make a 
GET
 against 
https://$ACCOUNT.cloudant.com
. If you misspell your account
name, you might get the following error, 
503: Service unavailable
. You can see the types of authentication that are available in the following list:
IBM Cloud® Identity and Access Management (IAM)
Basic authentication
Cookie authentication
IAM authentication
You can perform the following tasks with IAM:
Centrally manage access management across IBM Cloud.
Allow a user or service to access many different resources by using the same set of credentials (for example, same username and password or
IAM API key).
IAM API keys can be granted access to account management functions, like creating new databases.
For more information, see 
Managing access
 or an overview of 
IAM
.
Authentication
Authentication means proving who you are. You prove your identity by supplying your user credentials for verification.
Basic authentication is similar to showing an ID at a door to be checked every time that you want to enter. Cookie authentication is similar to having a
key to the door so that you can let yourself in whenever you want. Within IBM Cloudant, 
the key is a cookie that is named 
AuthSession
.
Basic authentication
To use Basic authentication, pass your credentials as part of every request. You pass your credentials by adding an 
Authorization
 header to the
request.
The header includes the authentication scheme (
Basic
), followed by the 
BASE64
 encoding of a string created by concatenating:
Your username
The 
:
 character
Your password
In practice, many application libraries that are used for creating HTTP requests can do this encoding for you.
For more information, see 
Security scheme
 on basic authentication.
Cookie authentication
Cookie authentication requires that you supply a valid username and password one time, at the start of a series of tasks (the session). The response
includes a cookie, generated by the server, that confirms you successfully authenticated. 
After the cookie is created, you send the cookie with all
requests that require authentication.
The presence of a valid cookie is sufficient to ensure that your call request is processed rather than rejected immediately as unauthenticated. You
can use the cookie until it expires.
Using the 
DELETE
 method logs out the user because the cookie is considered expired by the server.
 Note: 
When you create or use performance-critical IBM Cloudant applications, cookie authentication has more benefits when compared with
Basic authentication. We encourage you to use cookie authentication whenever possible.
Cloudant
   
119Table 1. Cookie authentication and methods
Method
Path
Description
Headers
Form
Parameters
POST
/_session
Do cookie-based user login.
Content-Type: application/x-www-form-
urlencoded
name
, 
password
GET
/_session
Returns cookie-based login user
information.
AuthSession cookie returned by POST request.
DELETE
/_session
Log out cookie-based user.
AuthSession cookie returned by POST request.
For more information, see 
Security scheme
 on basic authentication.
Authorization
After authenticating, the next test is to decide whether you're allowed to do certain tasks. This decision is called authorization.
When you authenticate with the IBM Cloudant system, it "knows" who you are. The next question is, what tasks are you allowed to do?
You might create a complete list of all the possible tasks that you can do, for each aspect of an IBM Cloudant system, such as a database or a
document. Although simple, this approach would require many lengthy lists. Keeping those lists accurate 
and complete is impractical.
A better approach uses the idea of "roles". The various tasks can be grouped into collections that are typical of some generic roles. For example, the
task of creating or deleting a database is characteristic of someone with an administrative 
role. Similarly, the task of creating or updating a document
is characteristic of someone with a "writing" role.
Rather than explicitly listing every task you can do, you're given one or more roles. If you have a role, then you can do all the tasks that are associated
with that role.
Roles
The following section applies only to legacy credentials. For more information about using roles with IAM credentials, see 
IBM Cloudant roles
.
IBM Cloudant has a number of roles available. The roles can be assigned to user accounts or 
API keys
.
The three core roles are defined in the following table:
Table 2. Core roles
Role
Description
_admin
Change security settings, including adding roles.
_reader
Read documents from the database.
_writer
Create, update, and delete documents (except design documents) in the database.
You might want to assign more than one role. For example, a user might need to read from or write to documents within a database, but wouldn't
need full administrative control over the database. To fulfill this requirement, the user's account 
is granted the 
_reader
 and 
_writer
 roles, but not
the 
_admin
 role.
A number of "focused" roles are also available. These provide permissions for specific API endpoints. The focused role permissions are similar to the
core role permissions, but apply 
only
 to the specific API endpoint.
The focused roles are defined in the following table:
Role
Description
API Endpoints
 Tip: 
The 
_reader
 and 
_writer
 roles are exclusive. If a user has the 
_writer
 role, they can't read documents that they create unless they
also
 have the 
_reader
 role.
Cloudant
   
120Table 3. Focused roles
_design
Allows create, read, modify, or delete access to design documents.
_design
, 
_find
, 
_index
_replicator
Allows read access to replicate data from a database, and write access to create
checkpoints.
_local
, 
_replicate
,
_replicator
_security
Allows read and write access to the 
/$DATABASE/_security
 endpoint.
_security
The nature of the access that is granted depends on the specific API endpoint. For example, the 
_design
 role provides access that allows a user or
API key
 
to create, read, modify, or delete design documents. If you grant access this way, the advantage is that you're not required to assign the
more widely applicable 
_reader
 or 
_writer
 roles. This distinction is useful 
because otherwise the authorized account might read from or write to
documents within the database, other than the design documents.
The credentials that you use to log in to the dashboard automatically have the 
_admin
 role for all databases you create. Everyone and everything
else, including users that you share databases with, and API keys you create, must 
be given a role explicitly to do corresponding tasks.
The special 
nobody
 username applies for anyone or any application that tries to do tasks, but that didn't authenticate with the system. In other
words, the 
nobody
 username applies to all unauthenticated connection attempts. 
For example, if an application tries to read data from a database,
but didn't identify itself, the task can continue only if the 
nobody
 user has the role 
_reader
.
It's possible to grant more powerful roles to an 
un
authenticated user than to an authenticated user. For example, if the 
nobody
 username is
intentionally granted 
_admin
, 
_reader
, and 
_writer
 roles, but an authenticated user account such as 
alexone
 is granted only the 
_reader
role. In this case, it's possible that an unauthenticated user might have a more 
powerful role than the authenticated 
alexone
 user.
Determining the role to assign
First, determine the role or roles to assign to a user account or API key. It's best to assign a role with the least permissions necessary to do the tasks
for that account or API key.
If the tasks are for a specific aspect, such as working with design documents or security settings, then assign a focused role, such as 
_design
 or
_security
.
API keys
The following section applies only to legacy credentials. For more information about using API keys with IAM credentials, see 
IAM API keys
.
Use API keys to enable database access for a person or application, but without creating a new IBM Cloudant account for that person or application.
An API key is a randomly generated username and password. The key is given the wanted access 
permissions for a database.
When a key is generated, and granted the required access permissions, the API key can be used in the same way as a normal user account.
However, API keys aren't the same as normal user accounts. An API key doesn't have access to the dashboard.
An API key is primarily used to enable applications to access a database, with a determined level of access control.
Creating API keys
You can create an API key in the following two ways:
a
. 
Use the dashboard.
b
. 
Use the IBM Cloudant API to 
modify the permissions
.
 Tip: 
It's important to understand that the 
nobody
 username is 
not
 a way of supplying a default set of permissions. Instead, the 
nobody
username is used to determine permissions for 
unauthenticated
 users.
 Tip: 
All IBM Cloudant instances that are deployed from the IBM Cloud® Public Germany region are deployed in EU-managed environments.
Any IBM Cloudant account or API key that is generated outside an EU-managed environment can't be granted access to 
an EU-managed IBM
Cloudant instance. For more information about IBM Cloudant in an EU-managed environment, see 
Locations and tenancy
.
 Deprecated: 
An earlier method of generating API keys by issuing the 
POST
 command to the
https://cloudant.com/api/generate_api_key
 endpoint is deprecated.
Cloudant
   
121No matter what method you choose, remember to record the key name and password. These values are both randomly generated, and can't be
retrieved if lost or forgotten.
Using API keys
API keys are typically generated by using an account that has at least one database. It's possible to use the API key with other databases, or even
with other accounts.
By default, an API key has no permissions. It must be given permissions explicitly.
After you generate the API key, grant the key access-specific permissions for a specific database by sending a 
PUT
 request to
https://$ACCOUNT.cloudant.com/_api/v2/db/$DATABASE/_security
.
The database isn't required to be in the same account as the account used for generating the API key initially.
To give an existing API key permission to access a database in another account, follow these steps:
a
. 
Retrieve the existing 
security permissions
 for the database.
b
. 
Add
 the details of the API key to the database security permissions, along with the roles required.
For an example of this process, see the blog article: 
Using an IBM Cloudant API key with multiple IBM Cloudant databases and accounts
.
Deleting API keys
It's not possible to delete an API key. An API key is always available for use if you know the key and its password. However, the API key is only useful
when you assign it to a database, and assign permissions for working with the database.
To "delete" an API key, remove it from the database. All the permissions that were previously assigned to the API key for it to work with that
database are then removed.
To remove an API key by using the Dashboard
a
. 
Click 
Databases
 > 
Permissions
.
b
. 
Hover over the API key that you would like to delete.
c
. 
Click the "
X
" that appears when you hover over the API key.
To remove an API key by using the IBM Cloudant API
Use the 
modifying permissions
 technique to remove the API key from the list of users with access permission.
This technique works because an API key is similar to a user, and is granted access permissions. By removing the API key from the list of users that
have access permissions, you remove the API key from the list of users that have access 
to the database.
To remove the API key, send an HTTP 
PUT
 request to the same 
_security
 API endpoint you used to 
create the API key
. This request 
removes the
API key from the list of users with access permission. Provide an updated list of the usernames that have access permission. The updated list must
not include the API key.
Using the 
_users
 database with IBM Cloudant
The following section applies only to legacy credentials.
You can use the 
_users
 database
 to manage roles in IBM Cloudant.
User documents that are stored in the 
_users
 database must be structured and populated to comply with 
Apache CouchDB requirements
.
You can disable the IBM Cloudant authorization checks by setting the 
couchdb_auth_only:true
 parameter. To disable IBM Cloudant security, 
PUT
a JSON document to the 
_security
 endpoint of the database. For example, 
https://$ACCOUNT.cloudant.com/$DATABASE/_security
.
See the following example that uses HTTP to submit a modification request:
PUT
 
/$DATABASE/_security
 
HTTP/1.1
Content-Type
: 
application/json
See the following example to submit a modification request:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X PUT 
"
$SERVICE_URL
/products/_security"
 -H 
"Content-Type:
 
Cloudant
   
122application/json"
 --data 
'{"members": {"names": ["user1", "user2"], "roles": ["developers"]}}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PutSecurityOptions;
import
 com.ibm.cloud.cloudant.v1.model.SecurityObject;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
SecurityObject
 
members
 
=
 
new
 
SecurityObject
.Builder()
    .names(Arrays.asList(
"user1"
, 
"user2"
))
    .roles(Arrays.asList(
"developers"
))
    .build();
PutSecurityOptions
 
securityOptions
 
=
    
new
 
PutSecurityOptions
.Builder()
        .db(
"products"
)
        .members(members)
        .build();
Ok
 
response
 
=
    service.putSecurity(securityOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
members
: 
Cloudant
V1.
SecurityObject
 = {
  
names
: [
'user1'
, 
'user2'
],
  
roles
: [
'developers'
]
};
service.
putSecurity
({
  
db
: 
'products'
,
  
members
: members
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, SecurityObject
service = CloudantV1.new_instance()
members = SecurityObject(
  names=[
'user1'
, 
'user2'
],
  roles=[
'developers'
]
)
response = service.put_security(
  db=
'products'
,
  members=members
).get_result()
print
(response)
Go
Cloudant
   
123putSecurityOptions := service.NewPutSecurityOptions(
  
"products"
,
)
putSecurityOptions.SetMembers(&cloudantv1.SecurityObject{
  Names: []
string
{
"user1"
, 
"user2"
},
  Roles: []
string
{
"developers"
},
})
ok, response, err := service.PutSecurity(putSecurityOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See the following example modification request in JSON format:
{
 
"couchdb_auth_only"
:
 
true
,
 
"members"
:
 
{
  
"names"
:
 
[
"member"
]
,
"roles"
:
[
]
 
}
,
 
"admins"
:
 
{
  
"names"
:
 
[
"admin"
]
,
"roles"
:
[
]
 
}
}
See the following example response from a modification request:
{
 
"ok"
 
:
 
true
}
Working with curl
Curl
 by itself is not secure. We suggest 
acurl
, which can run 
curl
 IBM® Cloudant® for IBM Cloud® commands to URLs without entering your
username and password repeatedly.
You use curl examples in the following steps.
For the curl samples
You can supply the username and password data for a request in three ways.
a
. 
If you use the 
-u $ACCOUNT
 parameter, curl prompts you to enter your password interactively on the command line before you perform the
request.
This option is used for the curl examples in the IBM Cloudant API reference.
b
. 
[Caution: this option isn't secure]
 Entering the combination parameter 
-u $ACCOUNT:$PASSWORD
 as part of your command means that you
aren't asked to enter your password interactively.
However, a plain text copy of your password appears in the terminal log.
Cloudant
   
124If you use a safer variation of this method, you can define a curl control file that includes the following details:
$ 
--user 
"
$ACCOUNT
:
$PASSWORD
"
--globoff
--proto 
"=https"
You can then define an "alias" that enables the curl command to apply the control file, for example:
alias acurl="curl -s --config <full_path_and_name_of_config_file> "
Remember to exclude the control file from backups, since it includes the password in clear text.
c
. 
[Caution: this option isn't secure.]
 For an 
https
 curl request, you can supply the username and password as part of the following URL:
... https://$ACCOUNT:$PASSWORD@$ACCOUNT.cloudant.com ...
However, a plain text copy of your password appears in the terminal log.
An alternative approach is to use a hashed version of your username and password combination, and supply that data in your curl command. The
next section on 
authorized curl
 explains how to create a more 
complex 
acurl
 command that uses this technique.
Authorized curl - 
acurl
(The following section is based on a blog article that was written by Samantha Scharr: [ "Authorized curl, also known as 
acurl
"] originally published 27
November 2013.)
You no longer need to write a simple 
GET
 request to a database as 
https://$ACCOUNT:$PASSWORD@$ACCOUNT.cloudant.com/foo
. Instead, you can
use, 
https://$ACCOUNT.cloudant.com/foo
.
Not only does this cut down on annoyingly long URLs, but the 
acurl
 alias is also more secure. It prevents someone from reading your password
over your shoulder as you type. It also makes sure that your password isn’t sent in plain 
text over the network by enforcing HTTPS.
It takes the following three steps:
a
. 
Encode username and password
.
b
. 
Create an alias
.
c
. 
Activate the alias
.
Encode username and password
First, you base64-encode your IBM Cloudant username and password. This encoding gives us a base64 character sequence as output.
The command to base64-encode some data is similar to the following example:
python3 -c 
'import base64; print(base64.urlsafe_b64encode("$ACCOUNT:$PASSWORD".encode("utf-8")).decode("utf-8"))'
The output is called 
<OUTPUT-OF-BASE64>
.
For example, if you use the following command:
python3 -c 
'import base64; print(base64.urlsafe_b64encode("$ACCOUNT:$PASSWORD".encode("utf-8")).decode("utf-8"))'
You then get the following output:
NTFkZGM5YTAtZmE2MC00M2Q1LTgyNmJeKGNmYjBhNTVkMzFiLWJsdWVtaXguY2xvdWRhbnQuY29tOjY4ODIyZGQ5YTU5YzNhZjA1NDY5YzRhMGRjODUzZjVhYjQz
MmQxMDI0NTFiNTQ0ZTUxZjA5MjkwODU2NDcxNWM=
 Tip: 
If you're using a Windows™ computer, you can specify your username and password from the command line.
 Note: 
$ACCOUNT
 is the 
username
 field in your service credentials. For more information, see 
Locating your service credentials
.
 Note: 
Remember your password is still stored in plain text on your computer. Base64-encoding isn't encryption. If you use base64-encode
Cloudant
   
125Create an alias
Now, you create an alias for 
curl
 that includes these credentials, so you don’t have to enter them every time you write a 
curl
 command.
Add the following line to your 
~/.bashrc
 or 
~/.bash_profile
:
alias
 acurl=
"curl -s --proto '=https' -g -H 'Authorization: Basic <OUTPUT-OF-BASE64>'"
This alias adds an authorization header instead of including the authorization credentials in the URL you enter on the command line. It also forces the
use of HTTPS, which is recommended over plain HTTP. HTTPS encrypts your data and credentials 
in transit and helps you be sure you’re connecting
to IBM Cloudant systems.
Activate the alias
Now, start a new shell, or run 
source ~/.bash_profile
 (or 
~/.bashrc
 if you used that), to make the alias functional.
Test 
acurl
Now, let's make sure everything is set up correctly. Go ahead and run the following command:
acurl 
"https://
$ACCOUNT
.cloudant.com/_all_dbs"
If you get the list of your databases back, 
acurl
 is set up and ready to go.
How Cross-origin resource sharing (CORS) works
CORS
 is a mechanism that allows resources such as JSON documents in an IBM® Cloudant® for IBM Cloud® database to be requested from
JavaScript.
In this case, the JavaScript is running on a website that is loaded from another domain.
These "cross-domain" requests would normally be forbidden by web browsers. The requests use the 
same origin security policy
.
CORS defines a way in which the browser and the server interact to determine whether or not to allow the request. For IBM Cloudant, CORS might be
a good solution in the following use cases.
a
. 
You have a website on 
https://www.example.com
, and you want scripts on this website that can access data from
https://example.cloudant.com
.
To make this access possible, add 
https://www.example.com
 to your list of allowed origins. The effect is that scripts that are loaded from
this domain are then permitted to make Ajax requests to your IBM Cloudant databases. By 
using HTTP authorization with CORS requests, users
of your application can access only their database.
b
. 
You want to allow third parties access to your database.
For example, if you have a database that includes product information, add their domain to your list of allowed origins. After that, you can give
sales partners access to the information from JavaScript running on their domain. The effect 
is that scripts that run on their website can access
your IBM Cloudant database.
Browser support
CORS is supported by all current versions of commonly used browsers.
Security
Storing sensitive data in databases that can be accessed by using CORS is a potential security risk. When you place a domain in the list of allowed
origins, you're trusting all the JavaScript from the domain. If the web application that runs 
on the domain is running malicious code or has security
vulnerabilities, sensitive data in your database might be exposed.
on the same character sequence, you always get the same corresponding character output sequence.
 Note: 
Versions of Microsoft™ Internet Explorer before version 10 offer partial support for CORS. Versions of Microsoft™ Internet Explorer
before version 8 don't support CORS.
Cloudant
   
126Also, allowing scripts to be loaded by using HTTP rather than HTTPS, and then accessing data by using CORS, introduces the risk that a man-in-the-
middle attack might modify the scripts.
To reduce the risk of man-in-the-middle attacks, follow these guidelines:
Don't allow CORS requests from all origins. In other words, do not set 
"origins": ["*"]
 unless you're certain that you want to meet the
following conditions:
You want to allow all data in your databases to be publicly accessible.
User credentials that give permission to modify data are never used in a browser.
Allow CORS requests only from HTTPS origins, not HTTP.
Ensure that web applications that run on allowed origin domains are trusted and do not have security vulnerabilities.
For more information, see the 
API and SDK documentation
 about the configuration endpoints for CORS.
Dashboard
CORS support is available in the IBM Cloudant Dashboard.
You can update your CORS settings by using the CORS tab within the dashboard. See the following screenshot:
Figure 1. CORS dashboard
To see the current CORS configuration, open 
Account
 > 
CORS
 in the dashboard.
You can enable or disable CORS by using 
Enable CORS
. This setting corresponds to the 
enable_cors
 option
. when you change the CORS
configuration from within an application.
To specify that CORS is enabled for all domains, select the 
All domains (*)
 option.
To specify that CORS is enabled only for exact origin domains, list each of the domains or subdomains by using the 
Restrict to specific
domains
 option. For each domain, provide a full URL, preferably by using the 
https
 
prefix for better security.
How HTTP works with IBM Cloudant
Learn details about the HTTP headers you need to know when you use IBM® Cloudant® for IBM Cloud®.
HTTP headers
Because IBM Cloudant uses HTTP for all external communication, you need to ensure that the correct HTTP request headers are supplied and
processed on retrieval. This course of action ensures that you get the correct format and encoding. Different 
environments and clients are more or
less strict on the effect of these HTTP headers, especially when they are not present. To reduce the likelihood of problems or unexpected behavior,
you must be as specific as possible.
Request headers
The supported HTTP request headers are shown in the following list:
Accept
Content-Type
Cloudant
   
127Content-Encoding
If-None-Match
Accept
The 
Accept
 header specifies the list of potential data types that are returned by the server that would be accepted and understood by the client.
The format is a list of one or more MIME types, which are separated by colons.
For the most requests, the accepted list must include JSON data (
application/json
).
For attachments, you can either specify the MIME type explicitly, or use 
*/*
 to specify that all file types are supported.
If the 
Accept
 header is not supplied, then the server assumes the 
*/*
 MIME type, which means that the client accepts all formats.
See the following example of sending a request without an explicit 
Accept
 header, or when you specify 
*/*
:
GET
 
/recipes
 
HTTP/1.1
Host
: 
username.cloudant.com
Accept
: 
*/*
See the following example of a returned header when the client is assumed to accept all formats.
Server
: 
CouchDB/1.0.2 (Erlang OTP/R14B)
Date
: 
Thu, 13 Jan 2011 13:39:34 GMT
Content-Type
: 
text/plain;charset=utf-8
Content-Length
: 
#7
Cache-Control
: 
must-revalidate
The use of 
Accept
 in queries to IBM Cloudant is not required, but is highly recommended as it helps to ensure that the data returned can be
processed by the client.
If you specify a data type that uses the 
Accept
 header, IBM Cloudant honors the specified type in the 
Content-type
 header field of responses. For
example, if you explicitly request 
application/json
 
in the 
Accept
 of a request, the returned HTTP headers use this value in the returned
Content-type
 field.
See the following example request that explicitly specifies the 
Accept
 header:
GET
 
/recipes
 
HTTP/1.1
Host
: 
username.cloudant.com
Accept
: 
application/json
See the following example of the headers returned in response, including the 
application/json
 content type:
Server
: 
CouchDB/1.0.2 (Erlang OTP/R14B)
Date
: 
Thu, 13 Jan 2011 13:40:11 GMT
Content-Type
: 
application/json
Content-Length
: 
#7
Cache-Control
: 
must-revalidate
Content-Type for request headers
The 
Content-Type
 header specifies the content type of the information that is supplied within the request. The specification uses MIME type
specifications. For most requests, the content type is JSON (
application/json
).
For some settings, the MIME type is plain text.
In particular, when you upload attachments the type must be the corresponding MIME type for the attachment or binary (
application/octet-
stream
).
The use of the 
Content-Type
 on a request is highly recommended.
Content-Encoding
The 
Content-Encoding
 header specifies the encoding of the request body. The supported value is 
gzip
. If the header is used, the request body
must be encoded with the corresponding format.
 Note: 
The returned content type is 
text/plain
 even though the information that is returned by the request is in JSON format.
Cloudant
   
128See the following example of creating a compressed (
gzipped
) request body:
# create gzipped document
echo
 
'{"foo":"bar"}'
 | gzip > doc.gzip
See the following example of sending a gzip-encoded request body to create a document by using HTTP:
PUT
 
/db/doc
 
HTTP/1.1
HOST
: 
example.cloudant.com
Content-Encoding
: 
gzip
See the following example of sending a gzip-encoded request body to create a document by using the command line:
curl 
"https://example.cloudant.com/db/doc"
 \
 -X PUT \
 -T doc.gzip \
 -H 
"Content-Encoding: gzip"
If-None-Match
The 
If-None-Match
 header is optional. You might send it to determine whether a document was modified since it was last read or updated. The
value of the 
If-None-Match
 header must match the last 
Etag
 
value received. If the value matches the current revision of the document, the server
sends a 
304 Not Modified
 status code, and the response 
itself has no body.
If the document was modified, you get a normal 
200
 response
, provided the document still exists and no other errors occurred.
Response headers
Response headers are returned by the server when you send back content. They include a number of different fields. Many of the fields are standard
HTTP response headers and have no significance regarding how IBM Cloudant operates. The supported 
HTTP response headers that are important
to IBM Cloudant are as shown in the following list.
Cache-Control
Content-Length
Content-Type
Etag
Cache-Control
The 
Cache-Control
 HTTP response header provides a suggestion for the client cache mechanisms on how to treat the returned information. IBM
Cloudant typically returns the 
must-revalidate
 value, which indicates that 
the information must be revalidated if possible. Revalidation ensures
that the dynamic nature of the content is correctly updated.
Content-Length
The 
Content-Length
 header reports the length in bytes of the returned content.
Content-Type for response headers
The 
Content-Type
 header specifies the MIME type of the returned data. For most request, the returned MIME type is 
text/plain
. All text is
encoded in Unicode (UTF-8), which is explicitly stated in the returned 
Content-Type
 
as 
text/plain;charset=utf-8
.
Etag
The 
Etag
 header is used to show the revision for a document. For documents, the value is identical to the revision of the document. The value can
be used with an 
If-None-Match
 request header to get a 
304 Not Modified
 response if the revision is still current.
ETags cannot currently be used with views, since the ETags returned from those requests are random numbers that change on every request.
How JavaScript Object Notation (JSON) works
Most requests and responses to and from IBM® Cloudant® for IBM Cloud® use 
JSON
 for formatting the content and structure of the data and
 Tip: 
By default, the SDKs compress the request body.
Cloudant
   
129responses.
In IBM Cloudant databases, the JSON object is used to represent various structures, including all documents in a database.
Parsing JSON into a JavaScript object is supported through the 
JSON.parse()
 function in JavaScript, or through various 
libraries
 that perform the
parsing 
of the content into a JavaScript object for you. Libraries for parsing and generating JSON are available for many major programming
languages.
JSON is used because it's the simplest and easiest solution for working with data that uses a web browser. As a result, JSON structures can be
evaluated and used as JavaScript objects within the web browser environment. JSON also integrates with 
the server-side JavaScript used within IBM
Cloudant. JSON documents are always UTF-8 encoded.
Be careful to follow these guidelines:
Your JSON structures are valid.
You normalize strings in JSON documents retrieved from IBM Cloudant.
JSON supports the same basic types that are supported by JavaScript: numbers, strings, Booleans, arrays, and objects.
Numbers
Numbers can be integer or floating point values.
Example of a number in JSON format
123
Strings
Strings must be enclosed by double quotation marks. Strings support Unicode characters and escaping a backslash.
Example of a string in JSON format
"A String"
Booleans
A 
true
 or 
false
 value.
Example of a boolean in JSON format
{
  
"value"
:
 
true
}
Arrays
A list of values enclosed in brackets. The values that are enclosed can be any valid JSON.
Example of an array in JSON format
[
    
"one"
,
    
2
,
    
"three"
,
    
[
]
,
    
true
,
    
{
        
"foo"
:
        
"bar"
    
}
]
Cloudant
   
130Example of an array in JSON format (linear)
[
 
"one"
,
 
2
,
 
"three"
,
 
[
]
,
 
true
,
 
{
 
"foo"
:
 
"bar"
 
}
 
]
Objects
A set of 
key-value
 pairs, such as an associative array, or a hash. The key must be a string, but the value can be any of the supported JSON values.
Example of a JSON object
{
    
"servings"
 
:
 
4
,
    
"subtitle"
 
:
 
"Easy to make in advance, and then cook when ready"
,
    
"cooktime"
 
:
 
60
,
    
"title"
 
:
 
"Chicken Coriander"
}
Cloudant
   
131Working with databases
Database overview
IBM® Cloudant® for IBM Cloud® databases contain JSON objects. These JSON objects are called 
documents
.
All documents must be contained in a database. For more information, see 
partitioned databases
.
The 
Grouping related documents together in IBM Cloudant
 guide provides an example of how documents 
for an e-commerce application might be
used within an IBM Cloudant database.
Partitioned databases
IBM Cloudant supports two types of databases:
Partitioned
Nonpartitioned
A partitioned database offers significant query performance and cost advantages but requires you to specify a logical partitioning of your data. The
partitioning is specified as part of each document's ID. A partitioned database provides both 
global and partition queries. Partition queries target
queries at a single, given document partition, meaning they need to process less data to return results. Therefore, partition queries offer significant
performance advantages, and also 
often provide cost advantages over global queries. Global queries target the entire database, which leads to extra
complexity, slower performance, and increased cost, but offers results that draw from all data.
Alternatively, a nonpartitioned database might be created. This type of database can be less complex to work with since no partitioning scheme
needs to be defined, but you can create only global secondary indexes.
IBM Cloudant strongly encourages you to use a partitioned database for best long-term database performance where the data model allows for
logical partitioning of documents.
The partitioning type of a database is set at database creation time. When you create a database, use the 
partitioned
 query string parameter to
set whether the database is partitioned. The default for 
partitioned
 is 
false
, maintaining compatibility with an earlier version.
The partitioning type can't be changed for an existing database.
For more information, see 
Database partitioning
.
Creating a database
To create a database, submit a 
PUT
 request with the following format:
Method
PUT /$DATABASE?partitioned=$BOOLEAN
Request body
None
Response
Success or failure of operation.
Roles permitted
_admin
See the following example that uses HTTP to create a partitioned database:
PUT
 
/$DATABASE?partitioned=true
 
HTTP/1.1
HOST
: 
$ACCOUNT.cloudant.com
See the following example that uses HTTP to create a nonpartitioned database:
PUT
 
/$DATABASE?partitioned=false
 
HTTP/1.1
HOST
: 
$ACCOUNT.cloudant.com
Cloudant
   
132Example - Creating a partitioned database
To create a partitioned database, see the following example:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X PUT 
"
$SERVICE_URL
/products?partitioned=true"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PutDatabaseOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PutDatabaseOptions
 
databaseOptions
 
=
 
new
 
PutDatabaseOptions
.Builder()
    .db(
"products"
)
    .partitioned(
true
)
    .build();
Ok
 
response
 
=
    service.putDatabase(databaseOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
putDatabase
({
  
db
: 
'products'
,
  
partitioned
: 
true
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.put_database(db=
'products'
, partitioned=
True
).get_result()
print
(response)
Go
putDatabaseOptions := service.NewPutDatabaseOptions(
  
"products"
,
)
putDatabaseOptions.SetPartitioned(
true
)
ok, response, err := service.PutDatabase(putDatabaseOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Cloudant
   
133Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Example - Creating a nonpartitioned database
To create a nonpartitioned database, see the following example:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X PUT 
"
$SERVICE_URL
/products"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PutDatabaseOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PutDatabaseOptions
 
databaseOptions
 
=
 
new
 
PutDatabaseOptions
.Builder()
    .db(
"products"
)
    .build();
Ok
 
response
 
=
    service.putDatabase(databaseOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
putDatabase
({
  
db
: 
'products'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.put_database(db=
'products'
).get_result()
print
(response)
Go
putDatabaseOptions := service.NewPutDatabaseOptions(
  
"products"
,
)
ok, response, err := service.PutDatabase(putDatabaseOptions)
Cloudant
   
134if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Query arguments
Table 1. Query arguments
Argument
Description
Optional
Type
Default
Supported values
partitioned
Determines whether the database is partitioned.
Yes
Boolean
false
true
, 
false
Database naming
The database name must start with a lowercase letter, and contain only the following characters:
Lowercase characters (a-z)
Digits (0-9)
Any of the following special characters: _, $, (, ), +, -, and /
If your database is successfully created, you get a 201 or 202 response. An error response uses the HTTP status code to indicate what went wrong.
Table 2. HTTP status codes
Code
Description
201
Database created successfully.
202
The database was successfully created on some nodes, but the number of nodes is less than the write quorum.
400
Invalid database name.
412
Database exists.
See the following example response that is received after a database is created successfully:
HTTP/1.1
 
201
 Created
{
    
"ok"
:
 
true
}
Database topology
It's possible to modify the configuration of a sharding topology for a database on dedicated database clusters. This modification can be done when
the database is created. However, poor choices for configuration parameters can adversely affect 
database performance.
For more information about modifying database configuration in a dedicated database environment, contact IBM Cloudant support.
Cloudant
   
135Getting database details
Sending a 
GET
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE
 returns details about the database, such as how many documents it
contains.
See the following example of using HTTP to get database details:
GET
 
/$DATABASE
 
HTTP/1.1
See the following example to get database details:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/products"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DatabaseInformation;
import
 com.ibm.cloud.cloudant.v1.model.GetDatabaseInformationOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetDatabaseInformationOptions
 
databaseInfoOptions
 
=
    
new
 
GetDatabaseInformationOptions
.Builder()
        .db(
"products"
)
        .build();
DatabaseInformation
 
response
 
=
    service.getDatabaseInformation(databaseInfoOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getDatabaseInformation
({
db
: 
'products'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_database_information(db=
'products'
).get_result()
print
(response)
Go
getDatabaseInformationOptions := service.NewGetDatabaseInformationOptions(
  
"products"
,
)
databaseInformation, response, err := service.GetDatabaseInformation(getDatabaseInformationOptions)
if
 err != 
nil
 {
  
panic
(err)
 Note: 
It isn't possible to modify the configuration that is used for databases on multi-tenant clusters.
Cloudant
   
136}
b, _ := json.MarshalIndent(databaseInformation, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The elements of the returned structure are shown in the following table:
Table 1. Database details
Field
Description
compact_running
Set to true if the database compaction routine is operating on this database.
db_name
The name of the database.
disk_format_version
The version of the physical format that is used for the data that is stored on disk.
disk_size
Size in bytes of the data as stored on the disk. Views indexes aren't included in the calculation.
doc_count
A count of the documents in the specified database.
doc_del_count
Number of deleted documents.
instance_start_time
Always 0.
other
JSON object that contains a 
data_size
 field.
purge_seq
The number of purge operations on the database.
sizes
A JSON object, containing 
file
, 
external
, and 
active
 sizes. 
active
 is the size in bytes of data that is stored
internally (excluding old revisions). 
external
 is the size in 
bytes of decompressed user data. This value is the billable
data size. The 
other/data_size
 field is an alias for the 
external
 field. 
file
 is the size in bytes of data that is stored
on the disk. Indexes 
aren't included in the calculation. The 
disk_size
 field is an alias for the 
file
 field. This size
includes data that is waiting for compaction.
update_seq
An opaque string that describes the state of the database. Don't rely on this string for counting the number of
updates.
partitioned_indexes
A JSON object that appears only if the database is partitioned. 
count
 is the number of partitioned indexes. 
indexes
list the type of partitioned indexes, and 
limit
 shows the maximum number of allowed 
partitioned indexes.
See the following example (abbreviated) response that contains database details:
{
 
"update_seq"
:
 
"982...uUQ"
,
 
"db_name"
:
 
"db"
,
 
"sizes"
:
 
{
  
"file"
:
 
46114703224
,
  
"external"
:
 
193164408719
,
  
"active"
:
 
34961621142
 
}
,
Cloudant
   
137 
"purge_seq"
:
 
0
,
 
"other"
:
 
{
  
"data_size"
:
 
193164408719
 
}
,
 
"doc_del_count"
:
 
5564
,
 
"doc_count"
:
 
9818541
,
 
"disk_size"
:
 
46114703224
,
 
"disk_format_version"
:
 
6
,
 
"compact_running"
:
 
true
,
 
"instance_start_time"
:
 
"0"
,
 
"partitioned_indexes"
:
 
{
  
"count"
:
 
7
,
  
"indexes"
:
 
{
   
"search"
:
 
1
,
   
"view"
:
 
6
  
}
,
  
"limit"
:
 
10
 
}
}
Getting a list of all databases in the account
To list all the databases in an account, send a 
GET
 request to 
https://$ACCOUNT.cloudant.com/_all_dbs
.
See the following example of using HTTP to list all databases:
GET
 
/_all_dbs
 
HTTP/1.1
See the following example to list all databases:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/_all_dbs"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.GetAllDbsOptions;
import
 java.util.List;
Cloudant
 
service
 
=
 Cloudant.newInstance();
List<String> response =
    service.getAllDbs().execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getAllDbs
().
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_all_dbs().get_result()
print
(response)
Cloudant
   
138Go
getAllDbsOptions := service.NewGetAllDbsOptions()
result, response, err := service.GetAllDbs(getAllDbsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(result, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See the following example response that is a JSON array with all the database names:
[
 
"_users"
,
 
"contacts"
,
 
"docs"
,
 
"invoices"
,
 
"locations"
]
Getting documents
To list all the documents in a database, send a 
GET
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE/_all_docs
.
The 
_all_docs
 endpoint accepts the following query string and JSON body arguments:
Argument
Description
Optional
Type
Default
conflicts
Can be set only if 
include_docs
 is 
true
. Adds information about conflicts to each
document.
Yes
Boolean
False
deleted_conflicts
Returns information about deleted conflicted revisions.
Yes
Boolean
False
descending
Return the documents in descending key order.
Yes
Boolean
False
endkey
Stop returning records when the specified key is reached.
Yes
String
endkey_docid
Stop returning records when the specified document ID is reached. If 
endkey
isn't set, this argument is ignored.
Yes
String
include_docs
Include the full content of the documents in the return.
Yes
Boolean
False
inclusive_end
Include rows whose key equals the "
endkey
" value.
Yes
Boolean
True
key
Return only documents with IDs that match the specified key.
Yes
String
keys
Return only documents with IDs that match one of the specified keys.
Yes
List of
strings
Cloudant
   
139Table 1. Query string and JSON body arguments
limit
Limit the number of returned documents to the specified number.
Yes
Numeric
meta
Short-hand combination of the following three arguments: 
conflicts
,
deleted_conflicts
, and 
revs_info
. Using 
meta=true
 is the same as using
conflicts=true&deleted_conflicts=true&revs_info=true
.
Yes
Boolean
False
r
Specify the 
read quorum
 value.
Yes
Numeric
2
revs_info
Includes detailed information for all known document revisions.
Yes
Boolean
False
skip
Skip this number of records before returning the results.
Yes
Numeric
0
startkey
Return records, starting with the specified key.
Yes
String
startkey_docid
Return records, starting with the specified document ID. If 
startkey
 isn't set,
this argument is ignored.
Yes
String
Notes
a
. 
Using 
include_docs=true
 might have 
performance implications
.
b
. 
When you use the 
keys
 argument, it might be easier to send a 
POST
 request rather than a 
GET
 request if you require multiple strings to list
the keys you want.
c
. 
When you use the 
keys
 argument and the revision is deleted, the 
value
 attribute that is returned is a JSON object with the current 
_rev
 of
the document and a 
_deleted
 attribute. The 
doc
 
attribute is only populated if you specified 
include_docs=true
 in the request and is
null
 if the document is deleted.
See the following example that uses HTTP to list all documents in a database:
GET
 
/_all_docs
 
HTTP/1.1
See the following example to list all documents in a database:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/orders/_all_docs"
 -H 
"Content-Type:
 
application/json"
 --data 
'{ "include_docs": true, "startkey": "abc", "limit": 10}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostAllDocsOptions
 
docsOptions
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .includeDocs(
true
)
        .startKey(
"abc"
)
        .limit(
10
)
        .build();
AllDocsResult
 
response
 
=
    service.postAllDocs(docsOptions).execute().getResult();
System.out.println(response);
Node
Cloudant
   
140const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postAllDocs
({
  
db
: 
'orders'
,
  
includeDocs
: 
true
,
  
startKey
: 
'abc'
,
  
limit
: 
10
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_all_docs(
  db=
'orders'
,
  include_docs=
True
,
  start_key=
'abc'
,
  limit=
10
).get_result()
print
(response)
Go
postAllDocsOptions := service.NewPostAllDocsOptions(
  
"orders"
,
)
postAllDocsOptions.SetIncludeDocs(
true
)
postAllDocsOptions.SetStartKey(
"abc"
)
postAllDocsOptions.SetLimit(
10
)
allDocsResult, response, err := service.PostAllDocs(postAllDocsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(allDocsResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See the following example that uses HTTP to list all documents in a database that match at least one of the specified keys:
GET
 
/_all_docs?keys=["somekey","someotherkey"]
 
HTTP/1.1
See the following example to list all documents in a database that match at least one of the specified keys:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/orders/_all_docs"
 -H 
"Content-Type:
 
Cloudant
   
141application/json"
 --data 
'{
  "include_docs": true,
  "keys": ["somekey", "someotherkey"],
  "limit": 10
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostAllDocsOptions
 
docsOptions
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .includeDocs(
true
)
        .keys(Arrays.asList(
"somekey"
, 
"someotherkey"
))
        .limit(
10
)
        .build();
AllDocsResult
 
response
 
=
    service.postAllDocs(docsOptions).execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postAllDocs
({
  
db
: 
'orders'
,
  
includeDocs
: 
true
,
  
keys
: [
'somekey'
, 
'someotherkey'
],
  
limit
: 
10
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_all_docs(
  db=
'orders'
,
  include_docs=
True
,
  keys=[
'somekey'
, 
'someotherkey'
],
  limit=
10
).get_result()
print
(response)
Go
postAllDocsOptions := service.NewPostAllDocsOptions(
  
"orders"
,
 )
 postAllDocsOptions.SetIncludeDocs(
true
)
 postAllDocsOptions.SetKeys([]
string
{
"somekey"
, 
"someotherkey"
})
 postAllDocsOptions.SetLimit(
10
)
 
Cloudant
   
142 allDocsResult, response, err := service.PostAllDocs(postAllDocsOptions)
 
if
 err != 
nil
 {
  
panic
(err)
 }
 
 b, _ := json.MarshalIndent(allDocsResult, 
""
, 
"  "
)
 fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The response is a JSON object that contains all documents in the database that match the parameters. The following table describes the meaning of
the individual fields:
Table 2. JSON object fields
Field
Description
Type
offset
Offset where the document list started.
Numeric, Null (The type can be 
null
 when 
keys
 are
specified.)
rows
Array of document objects.
Array
total_rows
Number of documents in the database or view that match the
parameters of the query.
Numeric
pdate_seq
Current update sequence for the database.
String
See the following example response after a request for all documents in a database:
{
 
"total_rows"
:
 
3
,
 
"offset"
:
 
0
,
 
"rows"
:
 
[
  
{
   
"id"
:
 
"5a049246-179f-42ad-87ac-8f080426c17c"
,
   
"key"
:
 
"5a049246-179f-42ad-87ac-8f080426c17c"
,
   
"value"
:
 
{
    
"rev"
:
 
"2-9d5401898196997853b5ac4163857a29"
   
}
  
}
,
  
{
   
"id"
:
 
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
   
"key"
:
 
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
   
"value"
:
 
{
    
"rev"
:
 
"2-ff7b85665c4c297838963c80ecf481a3"
   
}
  
}
,
  
{
   
"id"
:
 
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
   
"key"
:
 
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
   
"value"
:
 
{
    
"rev"
:
 
"2-cbdef49ef3ddc127eff86350844a6108"
   
}
  
}
 
]
}
Cloudant
   
143Sending multiple queries to a database
Now, the following instructions describe how to send multiple queries to a database by using 
_all_docs
 and 
_view
 endpoints.
Sending multiple queries to a database by using 
_all_docs
To send multiple queries to a specific database, send a 
POST
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE/_all_docs/queries
.
See the following example that uses HTTP to send multiple queries to a database:
POST
 
/$DATABASE/_all_docs/queries
 
HTTP/1.1
See the following example to multi-query the list of all documents in a database:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/products/_all_docs/queries"
 -H 
"Content-Type:
 
application/json"
 --data 
'{
  "queries": [
    {
      "keys": [
        "small-appliances:1000042",
        "small-appliances:1000043"
      ]
    },
    {
      "limit": 3,
      "skip": 2
    }
  ]
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsQuery;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsQueriesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsQueriesOptions;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
AllDocsQuery
 
query1
 
=
 
new
 
AllDocsQuery
.Builder()
    .keys(Arrays.asList(
"small-appliances:1000042"
,
        
"small-appliances:1000043"
))
    .build();
AllDocsQuery
 
query2
 
=
 
new
 
AllDocsQuery
.Builder()
    .limit(
3
)
    .skip(
2
)
    .build();
PostAllDocsQueriesOptions
 
queriesOptions
 
=
    
new
 
PostAllDocsQueriesOptions
.Builder()
        .queries(Arrays.asList(query1, query2))
        .db(
"products"
)
        .build();
AllDocsQueriesResult
 
response
 
=
    service.postAllDocsQueries(queriesOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
Cloudant
   
144const
 service = 
Cloudant
V1.
newInstance
({});
const
 
allDocsQueries
: 
Cloudant
V1.
AllDocsQuery
[] = [{
    
keys
: [
'small-appliances:1000042'
, 
'small-appliances:1000043'
],
  },
  {
    
limit
: 
3
,
    
skip
: 
2
}];
service.
postAllDocsQueries
({
  
db
: 
'products'
,
  
queries
: allDocsQueries
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 AllDocsQuery, CloudantV1
service = CloudantV1.new_instance()
all_docs_query1 = AllDocsQuery(
  keys=[
'small-appliances:1000042'
, 
'small-appliances:1000043'
]
)
all_docs_query2 = AllDocsQuery(
  limit=
3
,
  skip=
2
)
response = service.post_all_docs_queries(
  db=
'products'
,
  queries=[all_docs_query1, all_docs_query2]
).get_result()
print
(response)
Go
allDocsQueries := []cloudantv1.AllDocsQuery{
  {
    Keys: []
string
{
      
"small-appliances:1000042"
,
      
"small-appliances:1000043"
,
    },
  },
  {
    Limit: core.Int64Ptr(
3
),
    Skip:  core.Int64Ptr(
2
),
  },
}
postAllDocsQueriesOptions := service.NewPostAllDocsQueriesOptions(
  
"products"
,
  allDocsQueries,
)
allDocsQueriesResult, response, err := service.PostAllDocsQueries(postAllDocsQueriesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(allDocsQueriesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Cloudant
   
145Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
If you 
POST
 to the 
_all_docs/queries
 endpoint, it runs multiple specified built-in view queries of all documents in this database. You can use this
endpoint to request multiple queries in a single request, instead of 
multiple 
POST /$DATABASE/_all_docs
 requests.
The request JSON object must have a 
queries
 field. It represents an array of query objects with fields for the parameters of each individual view
query to be run. The field names and their meaning are the same as the query parameters 
of a regular 
_all_docs
 request.
The results are returned by using the following response JSON object:
Table 1. Response JSON object
Response JSON
object
Description
Type
results
An array of result objects - one for each query. Each result object contains the same fields as the response to a
regular 
_all_docs
 request.
Array
See the following example request with multiple queries:
{
POST /db/_all_docs/queries HTTP/
1.1
Content-Type
:
 application/json
Accept
:
 application/json
Host
:
 localhost
:
5984
{
    
"queries"
:
 
[
        
{
            
"keys"
:
 
[
                
"meatballs"
,
                
"spaghetti"
            
]
        
}
,
        
{
            
"limit"
:
 
3
,
            
"skip"
:
 
2
        
}
    
]
}
See the following example response for multiple queries:
HTTP/
1.1
 
200
 OK
Cache-Control
:
 must-revalidate
Content-Type
:
 application/json
Date
:
 Wed
,
 
20
 Dec 
2017
 
11
:
17
:
07
 GMT
ETag
:
 
"1H8RGBCK3ABY6ACDM7ZSC30QK"
Server
:
 CouchDB (Erlang/OTP)
Transfer-Encoding
:
 chunked
{
    
"results"
 
:
 
[
        
{
            
"rows"
:
 
[
                
{
                    
"id"
:
 
"SpaghettiWithMeatballs"
,
                    
"key"
:
 
"meatballs"
,
                    
"value"
:
 
1
                
}
,
Cloudant
   
146                
{
                    
"id"
:
 
"SpaghettiWithMeatballs"
,
                    
"key"
:
 
"spaghetti"
,
                    
"value"
:
 
1
                
}
,
                
{
                    
"id"
:
 
"SpaghettiWithMeatballs"
,
                    
"key"
:
 
"tomato sauce"
,
                    
"value"
:
 
1
                
}
            
]
,
            
"total_rows"
:
 
3
        
}
,
        
{
            
"offset"
 
:
 
2
,
            
"rows"
 
:
 
[
                
{
                    
"id"
 
:
 
"Adukiandorangecasserole-microwave"
,
                    
"key"
 
:
 
"Aduki and orange casserole - microwave"
,
                    
"value"
 
:
 
[
                        
null
,
                        
"Aduki and orange casserole - microwave"
                    
]
                
}
,
                
{
                    
"id"
 
:
 
"Aioli-garlicmayonnaise"
,
                    
"key"
 
:
 
"Aioli - garlic mayonnaise"
,
                    
"value"
 
:
 
[
                        
null
,
                        
"Aioli - garlic mayonnaise"
                    
]
                
}
,
                
{
                    
"id"
 
:
 
"Alabamapeanutchicken"
,
                    
"key"
 
:
 
"Alabama peanut chicken"
,
                    
"value"
 
:
 
[
                        
null
,
                        
"Alabama peanut chicken"
                    
]
                
}
            
]
,
            
"total_rows"
 
:
 
2667
        
}
    
]
}
Sending multiple view queries to a database by using 
_view
To send multiple view queries to a specific database, send a 
POST
 request to
https://$ACCOUNT.cloudant.com/$DATABASE/_design/$DDOC/_view/$VIEW/queries
.
See the following example that uses HTTP to send multiple queries to a database:
POST
 
/_view/$VIEW/queries
 
HTTP/1.1
See the following example that runs multiple specified view queries against the view function from the specified design document:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST
 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails/queries"
 -H 
"Content-Type: application/json"
 --data 
'{
 
"queries": [ { "include_docs": true, "limit": 5 },{ "descending": true, "skip": 1 } ]}'
Java
 Note: 
Multiple queries are also supported in 
/$DATABASE/_design_docs/queries
, which is similar to 
/$DATABASE/_all_docs/queries
.
Cloudant
   
147import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewQueriesOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewQueriesResult;
import
 com.ibm.cloud.cloudant.v1.model.ViewQuery;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
ViewQuery
 
query1
 
=
 
new
 
ViewQuery
.Builder()
    .includeDocs(
true
)
    .limit(
5
)
    .build();
ViewQuery
 
query2
 
=
 
new
 
ViewQuery
.Builder()
    .descending(
true
)
    .skip(
1
)
    .build();
PostViewQueriesOptions
 
queriesOptions
 
=
    
new
 
PostViewQueriesOptions
.Builder()
        .db(
"users"
)
        .ddoc(
"allusers"
)
        .queries(Arrays.asList(query1, query2))
        .view(
"getVerifiedEmails"
)
        .build();
ViewQueriesResult
 
response
 
=
    service.postViewQueries(queriesOptions).execute()
        .getResult();
System.out.println(response);
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, ViewQuery
service = CloudantV1.new_instance()
query1 = ViewQuery(
  include_docs=
True
,
  limit=
5
)
query2 = ViewQuery(
  descending=
True
,
  skip=
1
)
response = service.post_view_queries(
  db=
'users'
,
  ddoc=
'allusers'
,
  queries=[query1, query2],
  view=
'getVerifiedEmails'
).get_result()
print
(response)
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
viewQueries
: 
Cloudant
V1.
ViewQuery
[] = [
  {
    
include_docs
: 
true
,
    
limit
: 
5
  },
  {
Cloudant
   
148    
descending
: 
true
,
    
skip
: 
1
  }
];
service.
postViewQueries
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
queries
: viewQueries,
  
view
: 
'getVerifiedEmails'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Go
postViewQueriesOptions := service.NewPostViewQueriesOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
  []cloudantv1.ViewQuery{
    {
      IncludeDocs: core.BoolPtr(
true
),
      Limit:       core.Int64Ptr(
5
),
    },
    {
      Descending: core.BoolPtr(
true
),
      Skip:       core.Int64Ptr(
1
),
    },
  },
)
viewQueriesResult, response, err := service.PostViewQueries(postViewQueriesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewQueriesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The previous example requires the getVerifiedEmails view to exist. To create the design document with this view, see 
Create or modify a design
document
.The 
previous Go example also requires an import for 
github.com/IBM/go-sdk-core/v5/core
.
Multiple queries are supported by the 
_view
 endpoint, 
/$DATABASE/_design/$DDOC/_view/$VIEW/queries
.
The request JSON object must have a 
queries
 field. It represents an array of query objects with fields for the parameters of each individual view
query to be executed. The field names and their meaning are the same as the query 
parameters of a regular 
_view
 request.
Getting changes to documents in the database
Sending a 
GET
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE/_changes
 returns a list of changes that were made to documents in the
database, including insertions, updates, and deletions.
When a 
_changes
 request is received, one replica for each shard of the database is asked to provide a list of changes. These responses are
combined and returned to the original requesting client.
Cloudant
   
149The 
_changes
 endpoint accepts several optional query arguments:
Table 1. Query arguments for _changes endpoint
Argument
Description
Supported
values
Default
conflicts
Can be set only if 
include_docs
 is 
true
. Adds information about conflicts to each
document.
Boolean
False
descending
Return the changes in sequential order.
Boolean
False
doc_ids
To be used only when 
filter
 is set to 
_doc_ids
. Filters the feed so that only changes to
the specified documents are sent. 
Note
: The 
doc_ids
 parameter works only with versions
of IBM 
Cloudant that are compatible with CouchDB 2.0. For more information, see 
GET /
documentation.
A JSON array
of document
IDs
feed
Type of feed required. For more information, see the 
feed
 information
.
"continuous"
,
"longpoll"
,
"normal"
"normal"
filter
Name of 
filter function
 to use to get updates. The filter is defined in a 
design document
.
string
No filter.
heartbeat
If no changes occurred during 
feed=longpoll
 or 
feed=continuous
, an empty line is sent
after this time in milliseconds.
Any positive
number
No
heartbeat
include_docs
Include the document as part of the result.
Boolean
False
limit
Maximum number of rows to return.
Any non-
negative
number
None
seq_interval
Specifies how frequently the 
seq
 value is included in the response. Set a higher value to
increase the throughput of 
_changes
 and decrease the response size. 
Note
: In non-
continuous 
_changes
 
mode, the 
last_seq
 value is always populated.
Any positive
number
1
since
Start the results from changes after the specified sequence identifier. For more
information, see the 
since
 information
.
Sequence
identifier or
now
0
style
Specifies how many revisions are returned in the changes array. The 
main_only
 style
returns only the current "winning" revision. The 
all_docs
 style returns all leaf revisions,
including conflicts and deleted 
former conflicts.
main_only
,
all_docs
main_only
timeout
Wait this number of milliseconds for data, then stop the response. If the 
heartbeat
 setting
is also supplied, it takes precedence over the 
timeout
 setting.
Any positive
number
See the following example that uses HTTP to get a list of changes made to documents in a database:
GET
 
/$DATABASE/_changes
 
HTTP/1.1
See the following example to get a list of changes made to documents in a database:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/orders/_changes?limit=1"
Changes in a distributed database
 Important: 
Using 
include_docs=true
 might have 
performance implications
.
Cloudant
   
150IBM Cloudant databases are distributed. They have shard and fault-tolerant characteristics. These characteristics mean that the responses that are
provided by the 
_changes
 request might be different from the behavior you expect.
In particular, if you ask for a list of changes 
_since
 a sequence identifier, you get the requested information in response. But you might also get
changes that were made before the change indicated by the sequence identifier. The 
reason these extra changes are included, along with the
implications for applications, is explained in the 
Replication guide
.
Any application that uses the 
_changes
 request must be able to process a list of changes correctly as shown in the following list:
A different order for the changes that are listed in the response, when compared with an earlier request for the same information.
Changes that occur before the change specified by the sequence identifier.
The 
feed
 argument
The 
feed
 argument changes how IBM Cloudant sends the response. By default, 
_changes
 reports all changes, then the connection closes. This
behavior is the same as using the 
feed=normal
 argument.
If you set 
feed=longpoll
, requests sent to the server stay open until changes are reported. This option helps when monitoring changes
continuously.
If you set 
feed=continuous
, new changes are reported as they occur. This option means that the database connection stays open for a while. The
response may end at any time and clients should reconnect if they wish to continue receiving 
changes.
Each line in the continuous response is either empty or a JSON object that represents a single change. The option ensures that the following
guidelines are met:
The format of the report entries reflects the continuous nature of the changes.
Validity of the JSON output is maintained.
See the following example (abbreviated) responses from a continuous changes feed:
{
 
"seq"
:
 
"1-g1A...qyw"
,
 
"id"
:
 
"2documentation22d01513-c30f-417b-8c27-56b3c0de12ac"
,
 
"changes"
:
 
[
  
{
   
"rev"
:
 
"1-967a00dff5e02add41819138abb3284d"
  
}
 
]
}
,
{
 
"seq"
:
 
"2-g1A...ssQ"
,
 
"id"
:
 
"1documentation22d01513-c30f-417b-8c27-56b3c0de12ac"
,
 
"changes"
:
 
[
  
{
   
"rev"
:
 
"1-967a00dff5e02add41819138abb3284d"
  
}
 
]
}
,
{
 
"seq"
:
 
"3-g1A...qyy"
,
 
"id"
:
 
"1documentation22d01513-c30f-417b-8c27-56b3c0de12ac"
,
 
"changes"
:
 
[
  
{
   
"rev"
:
 
"2-eec205a9d413992850a6e32678485900"
  
}
 
]
,
 
"deleted"
:
 
true
}
,
{
 
"seq"
:
 
"4-g1A...qyz"
,
 
"id"
:
 
"2documentation22d01513-c30f-417b-8c27-56b3c0de12ac"
,
 
"changes"
:
 
[
  
{
   
"rev"
:
 
"2-eec205a9d413992850a6e32678485900"
  
}
 
]
,
 
"deleted"
:
 
true
}
Cloudant
   
151The 
filter
 argument
The 
filter
 argument designates a pre-defined 
filter function
 to apply to the changes feed. Additionally, several built-in filters are available:
_design
The 
_design
 filter accepts only changes to design documents.
_doc_ids
This filter accepts only changes for documents whose ID is specified in the 
doc_ids
 parameter.
_selector
Returns changes for documents that match the 
selector
 request body parameter. The 
selector syntax
 is the same as the syntax that is used
for 
_find
. If you want to use a selector filter, you must use the 
POST
 changes feed (as you can't supply a document body with a GET request).
Use the 
_selector
 method 
of filtering instead of the 
_view
 filtering method because it's faster and easier to use.
For more information, see the 
API documentation
.
_view
Enables use of an existing 
map function
 as the filter.
The 
since
 argument
Use the 
since
 argument to get a list of changes that occurred after a specified sequence identifier. If the 
since
 identifier is 0 (the default), or
omitted, the request returns all changes. If the 
since
 
identifier is 
now
, the request asks for changes that are made after the current time.
The distributed nature of IBM Cloudant can affect the results that you get in a response. For example, if you request a list of changes twice, by using
the same 
since
 sequence identifier both times, the order of changes in the resulting 
list might not be the same.
You might also see some results that appear to be from before the 
since
 parameter. The reason is that you might be getting results from a different
replica of a shard (a shard replica).
Shard replicas automatically and continuously replicate to each other and eventually have the same data. However, at any point in time, a shard
replica might differ from another shard replica because the replication between them isn't yet complete.
When you request a list of changes, normally the same replicas are used to respond. But if the node that holds the shard replica isn't available, the
system substitutes a corresponding shard replica that is held on another node. To help ensure 
that you see all the applicable changes, the most
recent checkpoint between the replicas is used. Using the checkpoint is effectively "rolling back" the list of changes to the most recent point in time
when the shard replicas were 
confirmed to agree with each other. This "rolling back" means you might see changes listed that took place "before"
the 
since
 sequence identifier you supplied.
Your application must be able to handle a change that is reported more than one time if you make a 
_changes
 request several times.
For more information about the behavior of the 
_changes
 response, see the 
replication guide
.
Responses from the 
_changes
 request
The response from a 
_changes
 request is a JSON object that contains a list of the changes that were made to documents within the database. The
following table describes the meaning of the individual fields:
Field
Description
Type
changes
An array that lists the changes that were made to the specific document.
Array
deleted
Boolean indicating whether the corresponding document was deleted. If present, it always has the value 
true
.
Boolean
id
Document identifier.
String
last_seq
Identifier of the last of the sequence identifiers. Currently, this identifier is the same as the sequence identifier of the
last item in the 
results
.
String
Cloudant
   
152Table 2. JSON object response fields for _changes
results
Array of changes that were made to the database.
Array
seq
Update sequence identifier.
String
See the following example (abbreviated) response to a 
_changes
 request:
{
 
"results"
:
 
[
  
{
   
"seq"
:
 
"1-g1A...sIg"
,
   
"id"
:
 
"foo"
,
   
"changes"
:
 
[
    
{
     
"rev"
:
 
"1-967...84d"
    
}
   
]
  
}
 
]
,
 
"last_seq"
:
 
"1-g1A...sIg"
,
 
"pending"
:
 
0
}
Important notes about 
_changes
The results that are returned by 
_changes
 are partially ordered. In other words, the order might not be preserved for multiple calls. You might
decide to get a current list by using 
_changes
 and including the 
last_seq
 value
. 
The resulting list provides the starting point for subsequent
_changes
 lists that use the 
since
 query argument.
Although shard copies of the same range contain the same data, their 
_changes
 history is often unique. This difference is a result of how
writes were applied to the shard. For example, they might be applied in a different order. 
To be sure that all changes are reported for your
specified sequence, it might be necessary to go further back into the shard's history to find a suitable starting point. The changes are then
reported from that starting point. This "rolling 
back" might give the appearance of duplicate updates, or updates that are apparently before the
specified 
since
 value.
_changes
 reported by a shard are always presented in order. But the ordering between all the contributing shards might appear to be
different. For more information, see 
A Changes Feed Example
.
Sequence values are unique for a shard, but might vary between shards. This variation means that, if you have sequence values from different
shards, you can't assume that the same sequence value refers to the same document within the different 
shards.
Using 
POST
 to get changes
Instead of 
GET
, you can also use 
POST
 to query the changes feed. The only difference, if you're using 
POST
 and you're using either of the
docs_ids
 or 
selector
 filters, is that 
it's possible to include the 
"doc_ids" : [...]
 or 
"selector": {...}
 parts in the request body. All other
parameters are expected to be in the query string, the same as using 
GET
.
See the following example that uses HTTP to 
POST
 to the 
_changes
 endpoint:
POST
 
/$DATABASE/_changes?filter=_selector
 
HTTP/1.1
Host
: 
$ACCOUNT.cloudant.com
Content-Type
: 
application/json
See the following example to 
POST
 to the 
_changes
 endpoint:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/orders/_changes"
 -H 
"Content-Type:
 
application/json"
'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
   
153Cloudant
 
service
 
=
 Cloudant.newInstance();
PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"orders"
)
    .build();
ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postChanges
({
  
db
: 
'orders'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'orders'
).get_result()
print
(response)
Go
postChangesOptions := service.NewPostChangesOptions(
  
"orders"
,
)
changesResult, response, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
When you 
POST
 to the 
_changes
 endpoint, you see an example similar to the following JSON object:
{
"results"
:
[
{
"seq"
:
"1-g1AAAA..."
,
"id"
:
"0007741142412418284"
,
"changes"
:
[
{
"rev"
:
"1-9d0c2676941ec3a3b3cc2f08fe9a51e0"
}
]
}
,
{
"seq"
:
"2-g1AAAA..."
,
"id"
:
"_design/applianceId"
,
"changes"
:
[
{
"rev"
:
"1-b1f67a8b672c1324680d6d7dc1e1fd3c"
}
]
}
,
...
Cloudant
   
154]
,
"last_seq"
:
"18-g1AAAA..."
,
"pending"
:
0
}
Deleting a database
To delete a database and its contents, send a 
DELETE
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE
.
See the following example that uses HTTP to delete an IBM Cloudant database:
DELETE
 
/$DATABASE
 
HTTP/1.1
Host
: 
$ACCOUNT.cloudant.com
See the following example to delete an IBM Cloudant database:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X DELETE 
"
$SERVICE_URL
/
$DB_NAME
"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DeleteDatabaseOptions;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteDatabaseOptions
 
databaseOptions
 
=
    
new
 
DeleteDatabaseOptions
.Builder()
        .db(
"<db-name>"
)
        .build();
Ok
 
response
 
=
    service.deleteDatabase(databaseOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
deleteDatabase
({
db
: 
'<db-name>'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_database(db=
'<db-name>'
).get_result()
print
(response)
Go
deleteDatabaseOptions := service.NewDeleteDatabaseOptions(
  
"<db-name>"
,
)
ok, response, err := service.DeleteDatabase(deleteDatabaseOptions)
 Note: 
No additional check is made to ensure that you really intended to delete the database.
Cloudant
   
155if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
If deletion succeeds, you get a 200 or 202 response. An error response uses the HTTP status code to indicate what went wrong.
Table 1. HTTP status codes
Code
Description
200
Database deleted successfully.
202
Database was successfully deleted on some nodes, but the number of nodes is less than the write quorum.
404
Database does not exist on all of the nodes.
See the following example response that is received after a database is deleted successfully:
{
 
"ok"
:
 
true
}
How is data stored in IBM Cloudant?
Every database in IBM® Cloudant® for IBM Cloud® is formed of one or more distinct shards, where the number of shards is referred to as 
Q
. A shard
is a distinct subset of documents from the database.
Concepts
All 
Q
 shards together contain the data within a database. Each shard is stored in three separate copies. Each shard copy is called a shard replica.
Each shard replica is stored on a different server. The servers are available within 
a single Region. If the Region supports Availability Zones, the
replicas are stored on servers in different Zones. The collection of servers in a Region is called a cluster.
Cloudant
   
156Figure 1. Data storage
A document is assigned to a particular shard by using consistent hashing of its ID. This assignment means that a document is always stored on a
known shard and a known set of servers.
Figure 2. Document consistent hashing
Occasionally, shards are rebalanced. Rebalancing involves moving replicas to different servers. Rebalancing occurs for several reasons, for example,
when server monitoring suggests that a server is more heavily or lightly used than other servers, 
or when a server must be taken out of service
temporarily for maintenance. The number of shards and replicas stays the same, and documents remain assigned to the same shard, but the server
storage location for a shard replica changes.
The default value for 
Q
 varies for different clusters. The value can be tuned over time.
The number of replicas (copies of a shard) is also configurable. In practice, observation and measurement of many systems suggests that three
replicas are a pragmatic number in most cases to achieve a good balance between performance and data 
safety. It would be exceptional and unusual
for an IBM Cloudant system to use a different replica count.
How does sharding affect performance?
The number of shards for a database is configurable because it affects database performance in a number of ways.
When a request comes into the database from a client application, one server or 'node' in the cluster is assigned as the coordinator of the request.
This coordinator makes internal requests to the nodes that hold the data relevant to the request, 
determines the response to the request, and
returns this response to the client.
The number of shards for a database can affect the performance in two ways:
a
. 
Each document in the database is stored on a single shard.
Therefore, having many shards enables greater parallelism for any single document request. The reason is that the coordinator sends requests
only to the nodes that hold the document. Therefore, if the database has many shards, there are 
likely to be many other nodes that do not
need to respond to the request. These nodes can continue to work on other tasks without interruption from the coordinator request.
b
. 
To respond to a query request, a database must process the results from all the shards.
Therefore, having more shards introduces a greater processing demand. The reason is that the coordinator must make one request per shard,
then combine the results before it returns the response to the client.
To help determine a suitable shard count for your database, begin by identifying the most common types of requests that are made by the
applications. For example, consider whether the requests are mostly for single document operations, or are 
the requests mostly queries? Are any of
the operations time-sensitive?
For all queries, the coordinator issues read requests to all replicas. This approach is used because each replica maintains its own copy of the indexes
that help answer queries. An important consequence of this configuration is that having more 
shards enables parallel index building if document
writes tend to be evenly distributed across the shards in the cluster.
In practice, it is hard to predict the likely indexing load across the nodes in the cluster. Furthermore, predicting indexing load tends to be less useful
than addressing request patterns. The reason is that indexing might be required after 
a document write, but not after a document request. Therefore,
considering indexing alone does not provide sufficient information to estimate an appropriate shard count.
When you consider data size, an important consideration is the number of documents per shard. Each shard holds its documents in a large 
B-tree
 on
Cloudant
   
157disk. Indexes are stored in the same way. As more documents are added to a shard, the number of steps that are used to traverse the B-tree during
a typical document lookup or query increases. This 'depth increase' tends to slow down requests because more data must be read from caches or
disk.
In general, avoid having more than 10 million documents per shard. In terms of overall shard size, keeping shards under 10 GB is helpful for
operational reasons. For example, smaller shards are easier to move over the network during rebalancing.
Given the conflicting requirements to avoid having too many documents and keeping shard size low, a single 
Q
 value cannot work optimally for all
cases. IBM Cloudant tunes the defaults for clusters over time as usage patterns change.
Nevertheless, for a specific database, it is often useful to take the time to consider observed request patterns and sizing. You can use this information
to guide the future selection of an appropriate number of shards. Testing with representative 
data and request patterns is essential for better
estimation of good 
Q
 values. Be prepared for production experience to alter those expectations.
The following simple guidelines might be helpful during the early planning stages. Remember to validate your proposed configuration by testing with
representative data, particularly for larger databases:
If your data is trivial in size, such as a few tens or hundreds of MB, or thousands of documents, then there is little need for more than a single
shard.
For databases of a few GB or few million documents, then a single-digit shard count such as 8 is likely to be acceptable.
For larger databases of tens to hundreds of millions of documents or tens of GB, consider configuring your database to use 16 shards.
For even larger databases, consider manually sharding your data into several databases. For such large databases, go to the 
IBM Cloud
Support portal
 for advice.
Working with shards
Setting shard count
The number of shards, 
Q
, for a database is set when the database is created. The 
Q
 value cannot be changed later.
To specify the 
Q
 when you create a database, use the 
q
 query string parameter.
If you attempt to set the 
Q
 value where it is not available, the result is a 
403
 response
 with a JSON body similar to the following 
example:
{
 
"error"
:
 
"forbidden"
,
 
"reason"
:
 
"q is not configurable"
}
Setting the replica count
In CouchDB version 2 onwards, you are allowed to 
specify the replica count
 when you create a database. However, you 
are not allowed to change
the replica count value from the default of 3. In particular, it is not possible to specify a different replica count value when you create a database. For
further help, go to the 
IBM Cloud Support portal
.
What are the 
R
 and 
W
 arguments?
Some requests can have arguments that affect the coordinator's behavior when it answers the request. These arguments are known as 
R
 and 
W
after their names in the request query string. They can be used for single 
document operations only. They have no effect on general 'query style'
requests.
In practice, it is rarely useful to specify 
R
 and 
W
 values. For example, specifying either 
R
 or 
W
 does not alter consistency for the read or write.
 Tip: 
The numbers in these guidelines are derived from observation and experience rather than precise calculation.
 Note: 
You can configure 
Q
. However, you want to prohibit large values of 
Q
 since they have a deleterious effect on the service with no
performance gain for the user.
 Important: 
It's possible to modify the configuration of a sharding topology for a database on dedicated database clusters. This modification
can be done when the database is created. However, poor choices for configuration parameters can adversely affect 
database performance.
For more information about modifying database configuration in a dedicated database environment, contact IBM Cloudant support.
Cloudant
   
158What is 
R
?
The 
R
 argument can be specified on single document requests only. 
R
 affects how many responses must be received by the coordinator before it
replies to the client. The responses must come from the nodes that host the replicas of the shard that contains the document.
Setting 
R
 to 1 might improve the overall response time because the coordinator can return a response more quickly. The reason is that the
coordinator must wait only for a single response from any one of the replicas that host 
the appropriate shard.
The default value for 
R
 is 2. This value corresponds to most of the replicas for a typical database that uses three shard replicas. If the database has
multiple replicas that are greater than or less than 3, the default value 
for 
R
 changes correspondingly.
What is 
W
?
W
 can be specified on single document write requests only.
W
 is similar to 
R
 because it affects how many responses must be received by the coordinator before it replies to the client.
The value of 
W
 does not affect whether the document is written within the database or not. By specifying a 
W
 value, the client can inspect the HTTP
status code in the response to determine whether 
W
 
replicas responded to the coordinator. The coordinator waits until a pre-determined timeout
for 
W
 responses from nodes that host copies of the document before it returns the response to the client.
Document versioning and MVCC
Multi-version concurrency control (MVCC)
 is how IBM® Cloudant® for IBM Cloud® databases ensures that all of the nodes in a database's 
cluster
contain only the 
newest version
 of a document.
Since IBM Cloudant databases are 
eventually consistent
, it is necessary to prevent inconsistencies from arising between nodes as a result of
synchronizing between outdated documents.
Multi-Version Concurrency Control (MVCC) enables concurrent read and write access to an IBM Cloudant database. MVCC is a form of 
optimistic
concurrency
. 
It makes both read and write operations on IBM Cloudant databases faster because the database locks on either read or write
operations isn't necessary. MVCC also enables synchronization between IBM Cloudant database nodes.
Revisions
Every document in an IBM Cloudant database has a 
_rev
 field that indicates its revision number.
A revision number is added to your documents by the server when you insert or modify them. The number is included in the server response when
you make changes or read a document. The 
_rev
 value is constructed by using a combination 
of a simple counter and a hash of the document.
The two main uses of the revision number are to help in the following cases:
a
. 
Determine what documents must be replicated between servers.
b
. 
Confirm that a client is trying to modify the latest version of a document.
You must specify the previous 
_rev
 when you 
update a document
 or else your request fails and returns a 
409 error
.
However, you can query a particular revision by using its 
_rev
, but older revisions are regularly deleted by a process called 
compaction
. You can
query a particular document revision by using its 
_rev
 in order to obtain a history of revisions to your document. 
However, a consequence of
compaction is that you cannot rely on a successful response. If you need a version history of your documents, a solution is to 
create a new document
for each revision.
Distributed databases and conflicts
Distributed databases work without a constant connection to the main database on IBM Cloudant, which is itself distributed, so updates based on
the same previous version can still be in conflict.
 Note: 
If you reduce the 
R
 value, it increases the likelihood that the returned response is not based on the most up-to-date data. This state
occurs because of the 
eventual consistency
 
model used by IBM Cloudant. Using the default 
R
 value helps mitigate this effect.
 Note: 
W
 does not affect the actual write behavior in any way.
 Note: 
_rev
 must not be used to build a version control system because it is an internal value that is used by the server. Therefore, older
revisions of a document are transient, and removed regularly.
Cloudant
   
159To find conflicts, add the query parameter 
conflicts=true
 when you retrieve a document. The response contains a 
_conflicts
 array with all
conflicting 
revisions.
To find conflicts for multiple documents in a database, write a view.
The following map function is an example that emits all conflicting revisions for every document that has a conflict.
See the following example of a map function to find documents with a conflict:
function
 (
doc
) {
    
if
 (doc.
_conflicts
) {
        
emit
(
null
, [doc.
_rev
].
concat
(doc.
_conflicts
));
    }
}
You might regularly query this view and resolve conflicts as needed, or query the view after each replication.
Steps to resolve conflicts
After you find a conflict, you can resolve it in four steps: get, merge, upload, and delete, as shown later.
Let's consider an example of how to resolve a conflict. Suppose that you have a database of products for an online shop. The first version of a
document might look like the following example:
{
    
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
    
"_rev"
:
 
"1-7438df87b632b312c53a08361a7c3299"
,
    
"name"
:
 
"Samsung Galaxy S4"
,
    
"description"
:
 
""
,
    
"price"
:
 
650
}
As the document doesn't have a description yet, someone might add one.
See the second version of the document, which is created by adding a description:
{
    
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
    
"_rev"
:
 
"2-61ae00e029d4f5edd2981841243ded13"
,
    
"name"
:
 
"Samsung Galaxy S4"
,
    
"description"
:
 
"Latest smartphone from Samsung"
,
    
"price"
:
 
650
}
At the same time, someone else - working with a replicated database - reduces the price.
See a different revision, conflicting with the previous one because of different 
price
 value:
{
    
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
    
"_rev"
:
 
"2-f796915a291b37254f6df8f6f3389121"
,
    
"name"
:
 
"Samsung Galaxy S4"
,
    
"description"
:
 
""
,
    
"price"
:
 
600
}
The two databases are then replicated. The difference in document versions results in a conflict.
Get conflicting revisions
You identify documents with conflicts by using the 
conflicts=true
 option.
See the following example of finding documents with conflicts:
https://$ACCOUNT.cloudant.com/products/$_ID?conflicts=true
See the following example response that shows conflicting revisions that affect documents:
Cloudant
   
160{
    
"_id"
:
"74b2be56045bed0c8c9d24b939000dbe"
,
    
"_rev"
:
"2-f796915a291b37254f6df8f6f3389121"
,
    
"name"
:
"Samsung Galaxy S4"
,
    
"description"
:
""
,
    
"price"
:
600
,
    
"_conflicts"
:
[
"2-61ae00e029d4f5edd2981841243ded13"
]
}
The version with the changed price was chosen arbitrarily as the latest version of the document. The conflict with another version is noted by
providing the ID of that other version in the 
_conflicts
 array. In most cases, this 
array has only one element, but many conflicting revisions might
exist.
Merge the changes
To compare the revisions to see what changed, your application gets all of the versions from the database.
See the following example commands to retrieve all versions of a document from the database:
https://$ACCOUNT.cloudant.com/products/$_ID
https://$ACCOUNT.cloudant.com/products/$_ID?rev=2-61ae00e029d4f5edd2981841243ded13
https://$ACCOUNT.cloudant.com/products/$_ID?rev=1-7438df87b632b312c53a08361a7c3299
Since the conflicting changes are for different fields of the document, it is easy to merge them.
For more complex conflicts, other resolution strategies might be required:
Time based - use the first or last edit.
User intervention - report conflicts to users and let them decide on the best resolution.
Sophisticated algorithms - for example, 3-way merges of text fields.
For a practical example of how to implement a merge of changes, see this project with 
sample code
.
Upload the new revision
The next step is to create a document that resolves the conflicts, and update the database with it.
See the following example document that merges changes from the two conflicting revisions:
{
    
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
    
"_rev"
:
 
"3-daaecd7213301a1ad5493186d6916755"
,
    
"name"
:
 
"Samsung Galaxy S4"
,
    
"description"
:
 
"Latest smartphone from Samsung"
,
    
"price"
:
 
600
}
Delete old revisions
Finally, you delete the old revisions by sending a 
DELETE
 request to the URLs with the revision you want to delete.
See the following example request to delete an old document revision by using HTTP:
DELETE https://$ACCOUNT.cloudant.com/products/$_ID?rev=2-61ae00e029d4f5edd2981841243ded13
See the following example request to delete an old document revision:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X DELETE 
"
$SERVICE_URL
/events/0007241142412418284?rev=2-
9a0d1cd9f40472509e9aac6461837367"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DeleteDocumentOptions;
Cloudant
   
161import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteDocumentOptions
 
documentOptions
 
=
    
new
 
DeleteDocumentOptions
.Builder()
        .db(
"events"
)
        .docId(
"0007241142412418284"
)
        .rev(
"2-9a0d1cd9f40472509e9aac6461837367"
)
        .build();
DocumentResult
 
response
 
=
    service.deleteDocument(documentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
deleteDocument
({
  
db
: 
'events'
,
  
docId
: 
'0007241142412418284'
,
  
rev
: 
'2-9a0d1cd9f40472509e9aac6461837367'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_document(
  db=
'events'
,
  doc_id=
'0007241142412418284'
,
  rev=
'2-9a0d1cd9f40472509e9aac6461837367'
).get_result()
print
(response)
Go
deleteDocumentOptions := service.NewDeleteDocumentOptions(
  
"events"
,
  
"0007241142412418284"
,
)
deleteDocumentOptions.SetRev(
"2-9a0d1cd9f40472509e9aac6461837367"
)
documentResult, response, err := service.DeleteDocument(deleteDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
Cloudant
   
162)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Now, conflicts affecting the document are resolved. You can verify the status by running 
GET
 to the document again with the 
conflicts
 parameter
set to 
true
.
Database partitioning
IBM® Cloudant® for IBM Cloud® supports two types of databases:
Partitioned
Non-partitioned
A 
partitioned
 database offers significant performance and cost advantages but requires you to specify a logical partitioning of your data. This process
is described more in the following text.
Alternatively, you can create a 
non-partitioned
 database. This type of database might be easier to work with as no partitioning scheme needs to be
defined, but only global secondary indexes can be created.
IBM Cloudant strongly recommends that you use a partitioned database for best long-term database performance where the data model allows for
logical partitioning of documents.
You can decide whether to partition at database creation time. When you create a database, use the 
partitioned
 query string parameter to set
whether the database is partitioned. The default for 
partitioned
 is 
false
, 
maintaining compatibility with an earlier version.
The partitioning type can't be changed for an existing database.
Database shards
Before you read this document, you must understand the 
sharding concept
 within IBM Cloudant.
Non-partitioned databases
A non-partitioned database is the older type of IBM Cloudant database, and the one that is familiar if you used CouchDB or IBM Cloudant previously.
Within a non-partitioned database, documents are distributed to shards in an arbitrary manner based on a transformation of their document ID.
Therefore, no real relation exists between a document's ID and the shard it ends up on. Documents with 
similar document IDs are unlikely to be
placed onto the same shard.
A non-partitioned database offers only global querying, described in more detail later.
Partitioned databases
A partitioned database is the newest type of IBM Cloudant database. Within a partitioned database, documents are formed into logical partitions by
use of a 
partition key
. The partition key is part of the document ID for documents within 
a partitioned database. All documents are assigned to a
partition, and many documents are typically given the same partition key. A partition's primary JSON data and its indexes end up colocated, meaning
that the database can query data within 
a partition more efficiently.
A partitioned database offers both partitioned and global querying. Partitioned querying takes advantage of the data layout within the database
cluster to deliver improved and more scalable query performance. Partition queries are also often 
cheaper than global queries.
As partitioned databases offer the advantages of both global and partition querying, IBM Cloudant recommends that new applications take
advantage of them.
What makes a good partition key?
If you're thinking of using IBM Cloudant's new 
partitioned database
 feature, then the choice of a partition key is important. A partition key must have:
Many values - lots of small partitions are better than a few large ones. A million partitions are perfectly fine, but keep each partition under 10
GB in total size.
No hot spots - avoid designing a system that makes one partition handle a high proportion of the workload. If the work is evenly distributed
around the partitions, the database performs more smoothly.
Repeating - If each partition key is unique, one document per partition exists. To get the best out of partitioned databases, multiple documents
Cloudant
   
163per partition must exist - documents that logically belong together.
Let's look at some use cases and some good and bad choices for a partition key.
Table 1. Good and bad choices for a partition key
Use Case
Description
Partition
Key
Effectiveness
E-commerce
system - orders
One document
per order
order_id
Neutral - one document per partition is fine, but it doesn't provide the benefits of
Partition Queries.
E-commerce
system - orders
One document
per order
user_id
Good - all of a user's orders are kept together.
E-commerce
system - orders
One document
per order
status
Bad - grouping orders by a handful of status values (provisional, paid, refunded,
cancelled) create too few over-large partitions.
Blogging platform
One document
per blog post
author_id
Good - if many authors participate. Easy to query each author's posts.
IOT - sensor
readings
One document
per reading
device_id
Good - if many devices exist, make sure that one device isn't producing many more
readings than the others.
IOT - sensor
readings
One document
per reading
date
Bad - current readings cause a "hot spot" on the current date's partition.
Some use cases exist where no viable choice for a partition key exists. In these situations, it's likely a non-partitioned database is the best choice. For
example, a database of users that stores email addresses, password hashes, and last-login 
dates. None of these fields make for a suitable partition
key, so a normal non-partitioned database must be used instead.
Querying
IBM Cloudant's query types are available for global and partition queries. See also a brief overview of the underlying querying mechanism that you
use to select the query mechanism that is best for each query your application needs to make.
Global querying
You can make global queries to the following index types:
IBM Cloudant Query
Views
Search
When you make a global query, the database must perform a scatter-gather operation across all data in the database. This action means making
requests of many individual database servers. The API coordination node receives the responses from 
all these servers and combines them to form a
single response to the client. This response might involve buffering data and delaying the response to the client if, for example, data requires sorting.
Partition querying
You can make partition queries to the following index types:
IBM Cloudant Query
Views
Search
When you make a partition query, the database can query just the data within a single partition. A partition's data resides in just one shard (with three
replicas). The API coordination node can make a request directly to servers that host 
that data rather than needing to combine responses from many
servers. The API coordination node is also free from buffering the response since it has no combination step to carry out. As a result, the data arrives
at the client more quickly.
As the size of a database increases, the number of shards must also increase. The increase in shards directly increases the number of queries that
the API coordination node needs to make to servers that host data when you use global queries. 
However, when you use partition queries, the
number of shards has no effect on the number of servers the API coordination node needs to contact. As this number stays small, increasing data
Cloudant
   
164size has no effect on query latency, unlike global 
queries.
Partitioned databases tutorials
You can see two examples of using partitioned databases:
a
. 
Read about 
partitioned databases and Node.js
 in this blog article that includes how to create a partitioned 
database, search, views, and a
global index.
b
. 
Read the following example about using views and the 
_all_docs
 endpoint.
Example - Partitioning IoT reading data
This discussion is abstract; let's make it concrete with an example. We take the Internet of Things domain and look at using IBM Cloudant as a
historian for device readings. Say that the devices provide sensor readings on pieces of infrastructure 
like roads or bridges.
Review the following assumptions:
Hundreds or thousands of devices that report readings.
Each device has a unique ID.
Each piece of infrastructure has a unique ID.
Devices aren't moved between pieces of infrastructure.
Each device writes a reading to IBM Cloudant every 10 seconds. Likely this reading is delivered by using a message bus to IBM Cloudant.
In a non-partitioned database, you might allow IBM Cloudant to generate document IDs. Another alternative is to name documents by device ID and
record timestamp.
Using the second approach, we'd end up with document IDs like the following example:
device-123456:20181211T11:13:24.123456Z
The timestamp could also be an epoch timestamp.
This approach allows the data for each device to be queried efficiently by using partitioned indexes. However, global indexes might need to be used
to create views over multiple devices, for example, all devices on a specific piece of infrastructure.
For illustrative purposes, let's make the scenario a bit more complicated. Assume that the application mostly needs to read all sensor data for a
specific piece of infrastructure rather than for individual devices.
In this application, you query by infrastructure item to be most efficient, so partitioning the data by piece of infrastructure makes a lot more sense
than by ID. This practice would allow all the devices for a specific piece of infrastructure 
to be efficiently queried as a group.
For the rare queries by device, you use two approaches:
a
. 
Build a global index that is keyed by device and query it. This approach is more effective if queries to individual devices are rare and not
repeated.
b
. 
Build a global index-mapping device to infrastructure, then issue partition queries to the infrastructure partition. This approach makes sense if
repeated queries to specific devices are used as the mapping can be cached. This approach is 
used for this application.
Let's look at how this approach works out. Let's look at four queries:
a
. 
Readings for all time for a piece of infrastructure.
b
. 
Readings for today for a piece of infrastructure.
c
. 
Readings for all time for a specific device.
d
. 
Readings for today for a specific device.
Creating the database
To create a partitioned database, pass 
true
 as the 
partitioned
 argument to the database creation request:
All tutorials in this section will use 
readings
 as the example database.
Curl
curl -X PUT 
"
$SERVICE_URL
/readings?partitioned=true"
Cloudant
   
165Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PutDatabaseOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PutDatabaseOptions
 
databaseOptions
 
=
 
new
 
PutDatabaseOptions
.Builder()
.db(
"readings"
)
.partitioned(
true
)
.build();
Ok
 
response
 
=
service.putDatabase(databaseOptions).execute()
.getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
putDatabase
({
  
db
: 
'readings'
,
  
partitioned
: 
true
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.put_database(db=
'readings'
, partitioned=
True
).get_result()
print
(response)
Go
putDatabaseOptions := service.NewPutDatabaseOptions(
"readings"
,
)
putDatabaseOptions.SetPartitioned(
true
)
ok, response, err := service.PutDatabase(putDatabaseOptions)
if
 err != 
nil
 {
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
Cloudant
   
166examples.
Document structure
First, let's define a simple document format to work with:
{
  
"deviceID"
:
 
"device-123456"
,
  
"infrastructureID"
:
 
"bridge-9876"
,
  
"ts"
:
 
"20181211T11:13:24.123456Z"
,
  
"reading"
:
 
{
    
"temperature"
:
 
{
      
"value"
:
 
12
,
      
"unit"
:
 
"c"
    
}
  
}
}
This document uses the partitioning scheme based on a piece of infrastructure. The document ID might include the infrastructure ID as the partition
key, and include both device and timestamp as the document key:
bridge-9876:device-123456-20181211T11:13:24.123456Z
Creating indexes
For the queries described previously, you need two indexes:
a
. 
A global index-mapping device ID to infrastructure ID
b
. 
A partitioned index-mapping device ID to reading
Creating a global view index
A view index is the most efficient way to do the simple device ID to infrastructure ID mapping. To define it, upload a design document with
options.partitioned
 set to 
false
 as this index is global. While in a real 
map
 function you'd want to be more defensive around field existence,
this document would look something like this:
{
  
"options"
:
 
{
    
"partitioned"
:
 
false
  
}
,
  
"views"
:
 
{
    
"by-device"
:
 
{
      
"map"
:
 
"function(doc) { emit(doc.deviceID, doc.infrastructureID) }"
    
}
  
}
}
Assuming the previous document in 
./view.json
, this document is uploaded to the database by using the following command:
curl -X PUT 
"
$SERVICE_URL
/readings/_design/infrastructure-mapping"
 -H 
'Content-Type: application/json'
 --data @view.json
For more language examples that show creating a global view, see the 
Storing the view definition
 guide, or 
the Create or modify a design document
section in API Docs
.
Creating a partitioned IBM Cloudant Query index
To return the readings for a specific device from a partition, you can use an IBM Cloudant Query index. For this document, use 
POST
 to 
_index
 with
an index definition that includes the 
partitioned
 field 
set to 
true
.
For these queries, you need two partitioned indexes:
a
. 
By timestamp
b
. 
By device ID and timestamp
 Note: 
For Query index definitions, the 
partitioned
 field isn't nested inside an 
options
 object.
Cloudant
   
167Uploading partitioned index by timestamp
Upload the index by timestamp to the database by using this command:
Curl
curl -X POST 
"
$SERVICE_URL
/readings/_index"
 -H 
'Content-Type: application/json'
 --data 
'{
   "index": {
      "fields": [
         {"ts": "asc"}
      ]
   },
   "name": "timestamped-readings",
   "type": "json",
   "partitioned": true
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.IndexDefinition;
import
 com.ibm.cloud.cloudant.v1.model.IndexField;
import
 com.ibm.cloud.cloudant.v1.model.IndexResult;
import
 com.ibm.cloud.cloudant.v1.model.PostIndexOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
IndexField
 
indexField
 
=
 
new
 
IndexField
.Builder()
    .add(
"ts"
, 
"asc"
)
    .build();
IndexDefinition
 
index
 
=
 
new
 
IndexDefinition
.Builder()
    .addFields(indexField)
    .build();
PostIndexOptions
 
indexOptions
 
=
 
new
 
PostIndexOptions
.Builder()
    .db(
"readings"
)
    .index(index)
    .name(
"timestamped-readings"
)
    .type(
"json"
)
    .partitioned(
true
)
    .build();
IndexResult
 
response
 
=
    service.postIndex(indexOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 indexField = {
  
ts
: 
'asc'
}
const
 index = {
  
fields
: [indexField]
}
service.
postIndex
({
  
db
: 
'readings'
,
  
name
: 
'timestamped-readings'
,
  
index
: index,
  
type
: 
'json'
,
  
partitioned
: 
true
Cloudant
   
168}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, IndexDefinition, IndexField
service = CloudantV1.new_instance()
index_field = IndexField(ts=
'asc'
)
index = IndexDefinition(
    fields=[index_field]
)
response = service.post_index(
    db=
'readings'
,
    name=
'timestamped-readings'
,
    index=index,
    
type
=
'json'
,
    partitioned=
True
).get_result()
print
(response)
Go
var
 indexField cloudantv1.IndexField
indexField.SetProperty(
"ts"
, core.StringPtr(
"asc"
))
postIndexOptions := service.NewPostIndexOptions(
  
"readings"
,
  &cloudantv1.IndexDefinition{
    Fields: []cloudantv1.IndexField{
      indexField,
    },
  },
)
postIndexOptions.SetName(
"timestamped-readings"
)
postIndexOptions.SetType(
"json"
)
postIndexOptions.SetPartitioned(
true
)
indexResult, response, err := service.PostIndex(postIndexOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(indexResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Uploading partitioned index by device ID and timestamp
Upload the index by device ID and timestamp to the database by using this command:
Cloudant
   
169Curl
curl -X POST 
"
$SERVICE_URL
/readings/_index"
 -H 
'Content-Type: application/json'
 --data 
'{
   "index": {
      "fields": [
         {"deviceID": "asc"},
         {"ts": "asc"}
      ]
   },
   "name": "deviceID-readings",
   "type": "json",
   "partitioned": true
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.IndexDefinition;
import
 com.ibm.cloud.cloudant.v1.model.IndexField;
import
 com.ibm.cloud.cloudant.v1.model.IndexResult;
import
 com.ibm.cloud.cloudant.v1.model.PostIndexOptions;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
IndexField
 
indexField1
 
=
 
new
 
IndexField
.Builder()
    .add(
"deviceID"
, 
"asc"
)
    .build();
IndexField
 
indexField2
 
=
 
new
 
IndexField
.Builder()
    .add(
"ts"
, 
"asc"
)
    .build();
IndexDefinition
 
index
 
=
 
new
 
IndexDefinition
.Builder()
    .fields(Arrays.asList(indexField1, indexField2))
    .build();
PostIndexOptions
 
indexOptions
 
=
 
new
 
PostIndexOptions
.Builder()
    .db(
"readings"
)
    .index(index)
    .name(
"deviceID-readings"
)
    .type(
"json"
)
    .partitioned(
true
)
    .build();
IndexResult
 
response
 
=
    service.postIndex(indexOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 indexField1 = {
  
deviceID
: 
'asc'
}
const
 indexField2 = {
  
ts
: 
'asc'
}
const
 index = {
  
fields
: [indexField1, indexField2]
}
Cloudant
   
170service.
postIndex
({
  
db
: 
'readings'
,
  
name
: 
'deviceID-readings'
,
  
index
: index,
  
type
: 
'json'
,
  
partitioned
: 
true
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, IndexDefinition, IndexField
service = CloudantV1.new_instance()
index_field1 = IndexField(deviceID=
'asc'
)
index_field2 = IndexField(ts=
'asc'
)
index = IndexDefinition(
    fields=[index_field1, index_field2]
)
response = service.post_index(
    db=
'readings'
,
    name=
'deviceID-readings'
,
    index=index,
    
type
=
'json'
,
    partitioned=
True
).get_result()
print
(response)
Go
var
 indexField1 cloudantv1.IndexField
var
 indexField2 cloudantv1.IndexField
indexField1.SetProperty(
"deviceID"
, core.StringPtr(
"asc"
))
indexField2.SetProperty(
"ts"
, core.StringPtr(
"asc"
))
postIndexOptions := service.NewPostIndexOptions(
  
"readings"
,
  &cloudantv1.IndexDefinition{
    Fields: []cloudantv1.IndexField{
      indexField1,
      indexField2,
    },
  },
)
postIndexOptions.SetName(
"deviceID-readings"
)
postIndexOptions.SetType(
"json"
)
postIndexOptions.SetPartitioned(
true
)
indexResult, response, err := service.PostIndex(postIndexOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(indexResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
Cloudant
   
171   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Making queries
Overall, you want to make four queries:
a
. 
Readings for all time for a piece of infrastructure.
b
. 
Readings for today for a piece of infrastructure.
c
. 
Readings for all time for a specific device.
d
. 
Readings for today for a specific device.
Finding all readings for a piece of infrastructure
These partitions are infrastructure-based, so you can use 
_all_docs
 for a partition. For example, query all readings for the 
bridge-9876
infrastructure piece by using the following command.
Curl
curl -X POST 
"
$SERVICE_URL
/readings/_partition/bridge-9876/_all_docs"
 -H 
'Content-Type: 
application/json'
 --data 
'{"include_docs": true}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionAllDocsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostPartitionAllDocsOptions
 
allDocsOptions
 
=
    
new
 
PostPartitionAllDocsOptions
.Builder()
        .db(
"readings"
)
        .partitionKey(
"bridge-9876"
)
        .includeDocs(
true
)
        .build();
AllDocsResult
 
response
 
=
    service.postPartitionAllDocs(allDocsOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postPartitionAllDocs
({
  
db
: 
'readings'
,
  
partitionKey
: 
'bridge-9876'
,
  
includeDocs
: 
true
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_all_docs(
Cloudant
   
172  db=
'readings'
,
  partition_key=
'bridge-9876'
,
  include_docs=
True
).get_result()
print
(response)
Go
postPartitionAllDocsOptions := service.NewPostPartitionAllDocsOptions(
  
"readings"
,
  
"bridge-9876"
,
)
postPartitionAllDocsOptions.SetIncludeDocs(
true
)
allDocsResult, response, err := service.PostPartitionAllDocs(postPartitionAllDocsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(allDocsResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Finding recent readings for a piece of infrastructure
This query needs to use 
the partitioned 
timestamped-readings
 index
. You can issue a query to the partition to get the readings for today, assuming
today is 13 December 
2018.
The partition is embedded in the HTTP path when you issue the request to IBM Cloudant:
Curl
curl -X POST 
"
$SERVICE_URL
/readings/_partition/bridge-9876/_find"
 -H 
'Content-Type: 
application/json'
 --data 
'{
    "selector": {
        "ts": { "$gte": "20181213"}
    }
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionFindOptions;
import
 com.ibm.cloud.cloudant.v1.model.Selector;
import
 java.util.HashMap;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map
 
greaterThanOrEqualWithTs
 
=
 
new
 
HashMap
<>();
greaterThanOrEqualWithTs.put(
"$gte"
, 
"20181213"
);
Selector
 
selector
 
=
 
new
 
Selector
();
Cloudant
   
173selector.put(
"ts"
, greaterThanOrEqualWithTs);
PostPartitionFindOptions
 
findOptions
 
=
    
new
 
PostPartitionFindOptions
.Builder()
        .db(
"readings"
)
        .partitionKey(
"bridge-9876"
)
        .selector(selector)
        .build();
FindResult
 
response
 
=
    service.postPartitionFind(findOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
selector
: 
Cloudant
V1.
Selector
 = {
  
ts
: {
'$gte'
: 
'20181213'
}
}
service.
postPartitionFind
({
  
db
: 
'readings'
,
  
partitionKey
: 
'bridge-9876'
,
  
selector
: selector
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_find(
  db=
'readings'
,
  partition_key=
'bridge-9876'
,
  selector={
'ts'
: {
'$gte'
: 
'20181213'
}}
).get_result()
print
(response)
Go
selector := 
map
[
string
]
interface
{}{
  
"ts"
: 
map
[
string
]
string
{
    
"$gte"
: 
"20181213"
,
  },
}
postPartitionFindOptions := service.NewPostPartitionFindOptions(
  
"readings"
,
  
"bridge-9876"
,
  selector,
)
findResult, response, err := service.PostPartitionFind(postPartitionFindOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Cloudant
   
174Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Finding the infrastructure ID for a device
The two queries we've yet to perform are shown in the following list:
a
. 
Readings for all time for a specific device.
b
. 
Readings for today for a specific device.
For these two queries, you need to find the partition for the devices by using the global 
by-device
 index. Then, you can query the individual
partition for readings. While you might use a global index to query for the readings 
for individual devices, the mapping from device to infrastructure
ID is highly cache-able. It never changes! With this approach, you can mostly use the cheaper and more efficient partitioned query for most requests.
Using a global index to query directly for device readings might be more efficient if caching the device to infrastructure mapping doesn't work well for
a specific application.
To find the relevant partition for a device, you query the 
by-device
 view, sending the device ID as the key:
curl -X POST 
"
$SERVICE_URL
/readings/_design/infrastructure-mapping/_view/by-device' -H 'Content-Type: application/json' --
data '{
"
keys
": ["
device-123456
"], "
limit
": 1 
}'
For more language examples that show querying a global view, see the 
Query a MapReduce view in API Docs
.
The previous command returns the following response:
{
  
"total_rows"
:
 
5
,
  
"offset"
:
 
0
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"bridge-9876:device-123456-20181211T11:13:24.123456Z"
,
      
"key"
:
 
"device-123456"
,
      
"value"
:
 
"bridge-9876"
    
}
  
]
}
The partition key is in the 
value
 field of the included row: 
bridge-9876
.
Querying for all results for a device
To get the results for a device, you issue a partition query for the device within the 
bridge-9876
 partition. A standard IBM Cloudant Query selector
is used, as if one were issuing a global query.
The partition is embedded in the HTTP path when you issue the request to IBM Cloudant:
Curl
curl -X POST 
"
$SERVICE_URL
/readings/_partition/bridge-9876/_find"
 -H 
'Content-Type: 
application/json'
 --data 
'{
   "selector": {
      "deviceID": {
         "$eq": "device-123456"
      }
   }
}'
Cloudant
   
175Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionFindOptions;
import
 com.ibm.cloud.cloudant.v1.model.Selector;
import
 java.util.HashMap;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map
 
equalWithDeviceID
 
=
 
new
 
HashMap
<>();
equalWithDeviceID.put(
"$eq"
, 
"device-123456"
);
Selector
 
selector
 
=
 
new
 
Selector
();
selector.put(
"deviceID"
, equalWithDeviceID);
PostPartitionFindOptions
 
findOptions
 
=
    
new
 
PostPartitionFindOptions
.Builder()
        .db(
"readings"
)
        .partitionKey(
"bridge-9876"
)
        .selector(selector)
        .build();
FindResult
 
response
 
=
    service.postPartitionFind(findOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
selector
: 
Cloudant
V1.
Selector
 = {
  
deviceID
: {
'$eq'
: 
'device-123456'
}
}
service.
postPartitionFind
({
  
db
: 
'readings'
,
  
partitionKey
: 
'bridge-9876'
,
  
selector
: selector
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_find(
  db=
'readings'
,
  partition_key=
'bridge-9876'
,
  selector={
'deviceID'
: {
'$eq'
: 
'device-123456'
}}
).get_result()
print
(response)
Go
selector := 
map
[
string
]
interface
{}{
"deviceID"
: 
map
[
string
]
string
{
"$eq"
: 
"device-123456"
,
},
}
Cloudant
   
176postPartitionFindOptions := service.NewPostPartitionFindOptions(
"readings"
,
"bridge-9876"
,
selector,
)
findResult, response, err := service.PostPartitionFind(postPartitionFindOptions)
if
 err != 
nil
 {
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Querying for recent results for a device
To get the results for a device, you issue a partition query for the device within the 
bridge-9876
 partition. The selector is only slightly more
complicated, but still the same as an equivalent global query.
Query for recent results assuming today is 13 December 2018
The partition is embedded in the HTTP path when issuing the request to IBM Cloudant:
Curl
curl -X POST 
"
$SERVICE_URL
/readings/_partition/bridge-9876/_find"
 -H 
'Content-Type: application/json'
 --data 
'{
   "selector": {
      "deviceID": {
         "$eq": "device-123456"
      },
      "ts": {
         "$gte": "20181213"
      }
   }
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionFindOptions;
import
 com.ibm.cloud.cloudant.v1.model.Selector;
import
 java.util.HashMap;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map
 
equalWithDeviceID
 
=
 
new
 
HashMap
<>();
equalWithDeviceID.put(
"$eq"
, 
"device-123456"
);
Map
 
greaterThanOrEqualWithTs
 
=
 
new
 
HashMap
<>();
greaterThanOrEqualWithTs.put(
"$gte"
, 
"20181213"
);
Cloudant
   
177Selector
 
selector
 
=
 
new
 
Selector
();
selector.put(
"deviceID"
, equalWithDeviceID);
selector.put(
"ts"
, greaterThanOrEqualWithTs);
PostPartitionFindOptions
 
findOptions
 
=
    
new
 
PostPartitionFindOptions
.Builder()
        .db(
"readings"
)
        .partitionKey(
"bridge-9876"
)
        .selector(selector)
        .build();
FindResult
 
response
 
=
    service.postPartitionFind(findOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
selector
: 
Cloudant
V1.
Selector
 = {
  
deviceID
: {
'$eq'
: 
'device-123456'
},
  
ts
: {
'$gte'
: 
'20181213'
}
}
service.
postPartitionFind
({
  
db
: 
'readings'
,
  
partitionKey
: 
'bridge-9876'
,
  
selector
: selector
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_find(
  db=
'readings'
,
  partition_key=
'bridge-9876'
,
  selector={
      
'deviceID'
: {
'$eq'
: 
'device-123456'
},
      
'ts'
: {
'$gte'
: 
'20181213'
}
  }
).get_result()
print
(response)
Go
selector := 
map
[
string
]
interface
{}{
"deviceID"
: 
map
[
string
]
string
{
"$eq"
: 
"device-123456"
,
},
"ts"
: 
map
[
string
]
string
{
"$gte"
: 
"20181213"
,
},
}
postPartitionFindOptions := service.NewPostPartitionFindOptions(
"readings"
,
"bridge-9876"
,
selector,
)
Cloudant
   
178findResult, response, err := service.PostPartitionFind(postPartitionFindOptions)
if
 err != 
nil
 {
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Conflicts
In distributed databases, copies of data might be stored in more than one location. The natural network and system characteristics of the network
might mean that changes made to a document stored in one location can't instantly update or replicate 
to other parts of the database.
In other words, independent updates can be made to different copies of documents. The effect of these updates might be to introduce disagreement
or "conflicts" as to what is the correct, definitive content for the document.
IBM® Cloudant® for IBM Cloud® tries to help you avoid conflicts by warning you of potential problems. It warns you by returning a 
409
 response
 to 
a
problematic update request. However, a 
409
 response might not be received if the database update is requested on a system that isn't currently
connected to the network. For example, the database might be on a mobile device that 
is temporarily disconnected from the Internet, which makes
it impossible to check whether other potentially conflicting updates were made.
If you request a document that is in a conflict situation, IBM Cloudant returns the document as expected. However, an internal algorithm considers a
number of factors before it determines which document version to return. You must not assume that 
the returned document is the most recent
version.
For example, if you don't check for conflicts, or fail to address them, your IBM Cloudant database can exhibit the following behaviors:
Increasing inconsistencies in document content because more conflicting documents occur.
Increasing database size because all conflicting documents must be kept until the conflict is resolved.
Decreasing performance because IBM Cloudant must work harder in response to each request as it tries to identify the "best possible" version
of a conflicted document.
The following suggested practices might help you decide when to check for, and resolve, conflicts:
Table 1. Suggested practices
Application characteristic
Frequency of document
update
Check for conflicts at
retrieval?
Check for conflicts at
update?
Always connected to the network, for example, a
server.
Often
Y
Always connected to the network.
Occasionally
Y
Often but not always connected to the network, for
example, a laptop.
Often
Y
Often but not always connected to the network.
Occasionally
Y
Occasionally connected to the network, for example, a
tablet.
Often
Y
Cloudant
   
179Finding conflicts
To find any conflicts that might be affecting a document, add the query parameter 
conflicts=true
 when you retrieve a document. When returned,
the resulting document includes a 
_conflicts
 array, which includes a list 
of all the conflicting revisions.
See the following example map function to find document conflicts:
$ 
function
 (doc) {
  
if
 (doc._conflicts) {
    emit(null, [doc._rev].concat(doc._conflicts));
  }
}
To find conflicts for multiple documents in a database, write a 
view
. Using a map function such as the example provided, you can find all the
revisions for every document with 
a conflict.
When you have such a view, you can use it to find and resolve conflicts as needed. Alternatively, you might query the view after each replication to
identify and resolve conflicts immediately.
How to resolve conflicts
After you find a conflict, you can resolve it by following the four steps that are described next.
Get
Merge
Upload
Delete
See the following example document of the first version:
$ 
{
  
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
  
"_rev"
:
 
"1-7438df87b632b312c53a08361a7c3299"
,
  
"name"
:
 
"Samsung Galaxy S4"
,
  
"description"
:
 
""
,
  
"price"
:
 
650
}
Let's consider a scenario for this example. Suppose you have a database of products for an online shop. The first version of a document might look
like the example provided.
See the following second version (first revision) of the document that adds a description:
$ 
{
  
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
  
"_rev"
:
 
"2-61ae00e029d4f5edd2981841243ded13"
,
  
"name"
:
 
"Samsung Galaxy S4"
,
  
"description"
:
 
"Latest smartphone from Samsung"
,
  
"price"
:
 
650
}
The document doesn't have a description yet, so someone might add one.
See the following 
alternative
 second version that introduces a price reduction data change to the first version of the document:
$ 
{
  
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
  
"_rev"
:
 
"2-f796915a291b37254f6df8f6f3389121"
,
  
"name"
:
 
"Samsung Galaxy S4"
,
  
"description"
:
 
""
,
  
"price"
:
 
600
}
At the same time, someone else, working with a replicated database, reduces the price. This change is made to the first version of the document.
Therefore, the price reduction change doesn't "know" about the description change.
Cloudant
   
180Later, when the two databases are replicated, it might not be clear which of the two alternative versions of the document is correct. This example is a
conflict scenario.
Get conflicting revisions
To find any conflicting revisions for a document, retrieve that document as normal, but include the 
conflicts=true
 parameter, similar to the
following example:
https://ACCOUNT.cloudant.com/products/$_ID?conflicts=true
See the following example response to document retrieval that shows conflicting revisions:
$ 
{
  
"_id"
:
"74b2be56045bed0c8c9d24b939000dbe"
,
  
"_rev"
:
"2-f796915a291b37254f6df8f6f3389121"
,
  
"name"
:
"Samsung Galaxy S4"
,
  
"description"
:
""
,
  
"price"
:
600
,
  
"_conflicts"
:
[
"2-61ae00e029d4f5edd2981841243ded13"
]
}
If the document has any conflicts, you would get a response similar to the example provided, which is based on the changed description or changed
price problem.
The version with the changed price was chosen 
arbitrarily
 as the latest version of the document. Do not assume that the most recently updated
version of the document is the latest version for conflict resolution purposes.
In this example, consider a conflict between the retrieved document, which has the 
_rev
 value 
2-f796915a291b37254f6df8f6f3389121
, and
another document, which has the 
_rev
 value 
2-61ae00e029d4f5edd2981841243ded13
. 
The conflicting document details are noted in the
_conflicts
 array.
Often, you might find that the array has only one element, but it's possible for there to be many conflicting revisions. Each revision is listed in the
array.
Merge the changes
Your application must identify all the potential changes, and reconcile them, effectively merging the correct and valid updates to produce a single,
non-conflicting version of the document.
To compare the revisions and identify what changed, your application must retrieve all the versions from the database. You begin by retrieving a
document and details of any conflicting versions. To start the retrieval, use a command similar 
to the following one, which also requests the
_conflicts
 array:
https://$ACCOUNT.cloudant.com/products/$_ID?conflicts=true
This retrieval gives you a current version of the document that you store, 
and
 a list of all the other conflicting documents that must also be retrieved,
for example 
...rev=2-61ae00e029d4f5edd2981841243ded13
 and 
...rev=1-7438df87b632b312c53a08361a7c3299
. Each of these other conflicting
versions is also retrieved and stored, for example:
https://$ACCOUNT.cloudant.com/products/$_ID?rev=2-61ae00e029d4f5edd2981841243ded13
https://$ACCOUNT.cloudant.com/products/$_ID?rev=1-7438df87b632b312c53a08361a7c3299
Once you have all of the conflicting revisions of a document available, you can resolve the conflicts.
In an earlier scenario, the differences between the versions of the document were for different fields within the document, making it easier to merge
them.
More complicated conflicts are likely to require correspondingly more analysis. To help, you might choose from various conflict resolution strategies,
such as:
Time based - uses a simple test of the first or most recent edit.
User assessment - the conflicts are reported to users, who then decide on the best resolution.
Sophisticated merging algorithms - often used with 
version control systems
. An example is the 
3-way merge
.
For a practical example of how to implement these changes, see 
this project with sample code
.
Upload the new revision
Cloudant
   
181See the following final revisions after you resolve and merge changes from the previous conflicting revisions:
$ 
{
  
"_id"
:
 
"74b2be56045bed0c8c9d24b939000dbe"
,
  
"_rev"
:
 
"3-daaecd7213301a1ad5493186d6916755"
,
  
"name"
:
 
"Samsung Galaxy S4"
,
  
"description"
:
 
"Latest smartphone from Samsung"
,
  
"price"
:
 
600
}
After you assess and resolve the conflicts, you create a document that includes the current and definitive data. This fresh document is uploaded into
the database.
Delete old revisions
See the following example requests to delete the old revisions:
$ 
DELETE https://$ACCOUNT.cloudant.com/products/$_ID?rev=2-61ae00e029d4f5edd2981841243ded13
DELETE https://$ACCOUNT.cloudant.com/products/$_ID?rev=2-f796915a291b37254f6df8f6f3389121
In the final step, you delete the old revisions. You delete the old revisions by sending a 
DELETE
 request, specifying the revisions to delete.
When the older versions of a document are deleted, the conflicts that are associated with that document are marked as resolved. You can verify that
no conflicts remain by requesting the document again. Set the 
conflicts
 parameter 
to true, and use 
find conflicts
 as before.
CAP Theorem
IBM® Cloudant® for IBM Cloud® uses an 
"Eventually Consistent"
 model. When you make an update to one part of IBM Cloudant, the update is
eventually seen by other parts of the system.
To understand how this model works, and why it's an essential part of using IBM Cloudant, consider what is meant by Consistency.
Consistency is one of the four 
"ACID"
 properties that are necessary for transactions within a database to be processed and reported reliably.
Additionally, consistency is one of the three attributes in the 
"CAP"
 theorem. The attributes are 
C
onsistency, 
A
vailability, and 
P
artition tolerance. The
theorem states that it's not possible for a distributed computer system such as IBM Cloudant to guarantee three attributes 
simultaneously
:
Consistency, where all nodes see the same data at the same time.
Availability, which guarantees that every request receives a response about whether it succeeded or failed.
Partition tolerance, where the system continues to operate even if any one part of the system is lost or fails.
The impossibility of guaranteeing all three attributes at the same time means that IBM Cloudant doesn't guarantee the Consistency attribute. As the
update propagates, the system is said to "converge" on complete consistency.
Eventual consistency is good for performance. With a strong consistency model, a system must wait for any updates to propagate completely and
successfully before a write or update request can be completed. With an eventually consistent model, 
the write or update request can return almost
immediately, while the propagation across the system continues 
behind the scenes
.
A database can demonstrate only two of these three attributes for both theoretical and practical reasons. A database prioritizing consistency and
availability is simple: a single node stores a single copy of your data. But this model is difficult 
to scale as you must upgrade the node to get more
performance, rather than use extra nodes. And, even a minor system failure can shut down a single-node system, while any message loss means
significant data loss. To endure, the system must become 
more sophisticated.
Tradeoffs in partition tolerance
A database that prioritizes consistency and partition tolerance commonly employs a primary-secondary setup, where one node of the many in the
system is elected leader. Only the leader approves data writes, while all secondary nodes replicate 
data from the leader to handle reads. If the
leader loses connection to the network, or can't communicate with many of the system's nodes, the remainder elects a new leader. This election
process differs between systems, and might be a source 
of 
significant problems
.
IBM Cloudant prioritizes availability and partition tolerance by employing a primary-primary setup, such that every node can accept both writes and
reads to its portion of your data. Multiple nodes include copies of each portion of your data. 
Each node copies data with other nodes. If a node
becomes inaccessible, others can serve in its place while the network heals. This way, the system returns your data in a timely manner despite
arbitrary node failure, and maintains 
eventual consistency
. The tradeoff in deprioritizing absolute consistency is that it takes time for all nodes to see
the same data. As a result, some responses might include old data while the new data 
propagates through the system.
Cloudant
   
182Changing the approach
Maintaining one consistent view of data is logical and easy to understand because a relational database does this work for you. The expectation is
that web-based services that interact with database systems behave in this way. But that expectation 
doesn't mean that they do work this way.
Consistency isn't a given, and it takes a little work to change the approach.
In fact, consistency isn't necessarily essential for many enterprise cloud services. Large, heavily used systems bring with them a high probability that
a portion of the system might fail. A database that is engineered around the need to prioritize 
availability and eventual consistency is better suited to
keeping your application online. The consistency of application data can be addressed after the fact.
Application availability versus consistency in the enterprise
A look at popular web-based services shows that people already expect high availability, and happily trade this availability for eventually consistent
data, often without realizing they're doing so.
Many applications mislead users for the sake of availability. Consider ATMs: inconsistent banking data is why it's still possible to overdraft money
without realizing it. It's unrealistic to present a consistent view of your account balance 
throughout the entire banking system if every node in the
network must halt and record this figure before operations continue. A better choice is to make the system highly available.
The banking industry figured it out back in the 1980s, but many IT organizations are still worried about sacrificing consistency for the sake of
availability. Think about the number of support calls placed when your sales team can't access their 
CRM app. Now consider whether they would
even notice when it takes a few seconds for a database update to propagate throughout the application.
Availability trumps consistency more than you might expect. Online shopping cart systems, HTTP caches, and DNS are a few more examples.
Organizations must consider the cost of downtime such as user frustration, productivity loss, and missed 
opportunities.
From theory to implementation
Addressing high availability is vital for cloud applications. Otherwise, global database consistency stays a major bottleneck as you scale. Highly
available applications need to maintain constant contact with their data, even if that data isn't 
up to date. That's the concept of eventual consistency,
and it's nothing to be scared of. Sometimes, with a large scale, it's better to serve answers that aren't perfectly correct than to not serve them at all.
Database systems hide the complexities of availability versus consistency in different ways, but they always exist. IBM Cloudant, CouchDB, and other
NoSQL database teams believe that the best policy requires developers to address these complexities 
early in the design process. By doing the hard
work up front, you reduce surprises because applications are ready to scale from day one.
Combining IBM Cloudant with other IBM services
Each database technology has its own strengths and weaknesses. Some are built for high availability and data durability (at the expense of more
hardware and extra cost). Others favor speed and can churn out blazingly fast queries (but might lose 
data in a sudden power failure).
In this tutorial, you combine two IBM® services, IBM® Cloudant® for IBM Cloud® and IBM Cloud® Databases for Redis to optimize for speed and cost
by implementing a caching system for database queries.
This tutorial takes less than an hour to complete. It is not entirely cost-free because the Databases for Redis service does not come with a free tier.
However, if you deprovision the services after you finish with them, you should not have to 
pay more than a few dollars.
The Project - Team Directory
Team Directory
 is a web app that contains the details of all divisional employees. These employees are assigned to six different color-coded teams
(Red, Orange, Green, Blue, Yellow, and Purple). When you visit the app, you can 
select one team and see the names of all the members of that team.
The app also shows you whether this list of team members was obtained from the IBM Cloudant database or from the Databases for Redis cache and
how long the query took. You 
can see just how much quicker cached data is to retrieve.
Objectives
a
. 
Learn how to provision multiple services on the IBM Cloud® by using Terraform.
b
. 
Learn how to use the IBM Cloudant NodeJS SDK to access your IBM Cloud® services.
Prerequisites
You need the following items:
Cloudant
   
183a
. 
An 
IBM Cloud®
 pay-as-you-go account
b
. 
Access to a Mac or Linux™ terminal
c
. 
Git
d
. 
Node.js and npm
e
. 
Terraform
f
. 
Jq
, a command-line tool to process JSON data
Step 1. Obtain an API key to deploy infrastructure to your account
Follow the steps in 
this document
 to create an API key and make a note of it.
Step 2. Clone the code repo and cd into the Terraform directory
Now, you get the code and create a credentials file.
a
. 
In a terminal window, type the following command:
git 
clone
 https://github.com/IBM-Cloud/team-directory.git
cd
 team-directory
b
. 
Create a document called 
terraform.tfvars
 with the following fields:
ibmcloud_api_key = 
"<your_api_key_from_step_1>"
region = 
"eu-gb"
redis_password  = 
"<make_up_a_password>"
Step 3. Create the infrastructure
a
. 
Create all the infrastructure that you need by running the Terraform script:
terraform apply --auto-approve
The Terraform folder contains a number of simple scripts, which you can see in the following list:
main.tf
Tells Terraform to use the IBM Cloud.
variables.tf
Contains the variable definitions whose values are populated from terraform.tfvars.
redis.tf
Creates a Databases for Redis instance and some credentials to access it.
cloudant.tf
Creates an IBM Cloudant free-tier instance and some credentials to access it.
It takes several minutes for the resources to be ready. Now you have an IBM Cloudant instance and a Databases for Redis instance that you
can access.
b
. 
Check out these instances by visiting the Resources section of your IBM Cloud® account.
The Terraform script outputs several bits of information that you use in the next steps.
Step 4. Run the service
In this step, you run a script that creates all the environment variables that your service needs and then runs the service.
 Note: 
You can have only one free-tier instance per account. If you already have one, you must delete it, or change the 
plan
 variable to
standard
.
Cloudant
   
184In the terminal, type the following command:
./build.sh
When you run this script, it takes the data output from the Terraform script and uses the 
jq
 facility to parse the content and create the environment
variables needed. It then runs the script (
server.js
) that initializes 
the database and populates it with data.
Step 5. Visit your website
a
. 
Open a browser and visit 
https://localhost:8080
. See the button for each team in the following screen capture:
Figure 1. Team Directory team selectors
b
. 
Click any of the colored buttons and obtain a list of team members.
c
. 
Look at where the data came from, IBM Cloudant (cache = false) or Databases for Redis (cache = true) and how long it took.
d
. 
Click the same button that you clicked in step two. You can see the data that comes from the Databases for Redis cache and takes a lot less
time to execute in the following screen capture:
Figure 2. Team Directory team list and cache information
The cached data is set to expire within 60 seconds. So if you return to one of the teams after 60 seconds, the data is again retrieved from the
database and not the cache.
e
. 
Use the 
Clear Cache
 button to remove all cached data from Databases for Redis if necessary.
About the Code
The application is a simple Node.js application. It uses three main packages:
@ibm-cloud/cloudant
 to connect to IBM Cloudant and read/write data.
redis
 to connect to the Databases for Redis instance and read/write data.
Express
 to enable a simple web server that allows users to interact with the data.
The following sections describe the two main files.
server.js
This 
server.js
 file runs the web server and communicates with IBM Cloudant and Databases for Redis. When the front end submits a team
selection to the 
team
 route (see 
index.html
), 
the 
app.route
 function first checks the cache to see whether it has the data already. If it does, then
it returns that. Otherwise, it makes a query to IBM Cloudant to retrieve team data, store it in the cache, and return it 
to the front end.
 Note: 
In a real cloud-based application, the application server and the Databases for Redis instance would be close to each other (in
the same data center) so latency between the two would be only a few milliseconds. In this example, extra network 
hops exist between
your locally hosted application server and the cloud-hosted Databases for Redis cache so latency gains aren't as good as in production.
Cloudant
   
185The read operation uses an IBM Cloudant design document and a MapReduce view to select documents. This selection is beyond the scope of this
tutorial, but you can read more about 
views and design documents
 
in the documentation.
This script also contains some code that uploads test data (contained in the 
directorydata.json
 file) to the database the first time it runs.
index.html
The index.html page is the only page of the application that is using the 
Vue.js framework
. When it loads, it shows you the available teams.
When you select a team, it makes an HTTP POST request with your choice to the 
/team
 route of the application (see 
redis.js
). A successful return
from the application contains all the 
data for the team members. We are displaying only their names and town for simplicity.
Summary
Today, we combined two IBM Cloud services to optimize cost and user experience: IBM Cloudant as a document store and query engine and
Databases for Redis as a content cache. Cached documents can be retrieved more quickly and more cheaply, 
but the tradeoff is that your application
might be showing old data to your users for a time.
 Important: 
If you followed this tutorial, you must deprovision your resources to stop incurring charges. You can deprovision from the
terraform
 directory on your terminal by typing the following command, 
terraform destroy --auto-approve
.
Cloudant
   
186How documents work
Overview
Documents are 
JSON objects
. Documents are also containers for your data, and are the basis of the IBM® Cloudant® for IBM Cloud® database.
IBM Cloudant uses an 
eventually consistent
 model for data. If you use the eventually consistent model, it's possible, under some conditions, to
retrieve older document content. 
For example, older content is retrieved when your application writes or updates a document that is followed
immediately by a read of the same document.
In other words, your application would see the document content as it was before the write or update occurred. For more information about this
model, see the topic on 
Consistency
.
Document fields
All documents must have two fields:
A unique 
_id
 field. The 
_id
 field is detailed in the next section.
A 
_rev
 field. The 
_rev
 field is a revision identifier, and is 
essential to the IBM Cloudant replication protocol
.
In addition to these two mandatory fields, documents can generally contain any other content that can be described by using JSON, subject to some
caveats detailed in the following sections.
Document IDs
The format of a document ID differs depending on whether a database is partitioned or not. When a database is partitioned, the partition key for each
document is defined as part of the document ID as detailed in the next section.
IDs in partitioned databases
When you use a partitioned database, the document ID specifies both the partition key and the document key. These keys are specified by splitting
the document ID into two parts that are separated by a colon:
$ 
$PARTITION_KEY
:
$DOCUMENT_KEY
The 
$PARTITION_KEY
 might be the same between documents. The 
$DOCUMENT_KEY
 must be unique within each partition. That is, overall the entire
document ID must be unique within a database. A document key might contain 
further colon characters.
IDs in non-partitioned databases
For non-partitioned databases, the 
_id
 field is either created by you, or generated automatically as a 
UUID
 by IBM Cloudant.
As with partitioned databases, the document ID must be unique within a database.
Field name restrictions
Field names that begin with the underscore character (
_
) are reserved in IBM Cloudant. This rule means that you can't normally have your own field
names that begin with an underscore. For example, the field 
example
 
would be accepted, but the field 
_example
 would result in a
doc_validation
 error message.
See an example of a JSON document that attempts to create a field with an underscore prefix:
{
 
"_top_level_field_name"
:
 
"some data"
}
See an error message that is returned when you attempt to create a field with an underscore prefix:
 Tip: 
If you're using an 
IBM Cloudant service on IBM Cloud®
, documents are limited to a maximum size of 1 MB. Exceeding this limit causes a
413
 error
.
 Tip: 
If you choose to specify the document 
_id
 field, it must be limited to no more than 7168 characters (7k).
Cloudant
   
187{
 
"error"
:
 
"doc_validation"
,
 
"reason"
:
 
"Bad special document member: _top_level_field_name"
}
However, if the field name is for an object that is nested within the document, you can use an underscore prefix for the field name.
See an example of a JSON document that attempts to create a field with an underscore prefix, nested within an object:
{
 
"another_top_level_field_name"
:
 
"some data"
,
 
"another_field"
:
 
{
  
"_lower_level_field_name"
:
 
"some more data"
 
}
}
See an example success message (abbreviated) returned when a nested field with an underscore prefix is created:
{
 
"ok"
:
 
true
,
 
"id"
:
 
"2"
,
 
"rev"
:
 
"1-9ce...8d4"
}
Quorum - writing and reading data
In a distributed system, it's possible that a request might take some time to complete. A "quorum" mechanism is used to help determine when a
request, such as a write or read, completes successfully.
For more information about quorum settings and their implications on dedicated IBM Cloudant systems, contact IBM Cloudant support.
Time to live
Time to live
 (TTL) is a property of data, where after a relative amount of time, or at an absolute time, the data is considered expired. The data itself
might be deleted or moved to an alternative (archive) location.
IBM Cloudant does not support Time to Live functions. The reason is that IBM Cloudant documents are only "soft" deleted, not deleted. The soft
deletion involves replacing the original document with a 
smaller record
. 
This small record or "tombstone" is required for replication purposes. It
helps ensure that the correct revision to use can be identified during replication.
If the TTL capability was available in IBM Cloudant, the resulting potential increase in short-lived documents and soft deletion records would mean
that the database size might grow in an unbounded fashion.
Creating a document
The steps that are shown here demonstrate how to create a document.
a
. 
Send a 
POST
 request with the document's JSON content to create a document.
b
. 
Run the following command: 
https://$ACCOUNT.cloudant.com/$DATABASE
.
Creating a document by using HTTP
The following steps show you how to create a document by using HTTP.
a
. 
Send a 
PUT
 request with the document's JSON content by using HTTP to create a document.
b
. 
Run the following command:
PUT
 
/$DATABASE/$DOC_ID
 
HTTP/1.1
Content-Type
: 
application/json
Examples of how to create a document
See an example of creating an IBM Cloudant document for this JSON in a nonpartitioned database:
Cloudant
   
188{
   
"type"
:
 
"event"
,
   
"userid"
:
 
"abc123"
,
   
"eventType"
:
 
"addedToBasket"
,
   
"productId"
:
 
"1000042"
,
   
"date"
:
 
"2019-01-28T10:44:22.000Z"
}
See an example of creating a document:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X PUT 
"
$SERVICE_URL
/events/0007241142412418284"
 -H 
"Content-Type:
 
application/json"
 --data 
'{ "type": "event", "userid": "abc123", "eventType": "addedToBasket", "productId": "1000042",
 
"date": "2019-01-28T10:44:22.000Z }'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Document;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PutDocumentOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Document
 
eventDoc
 
=
 
new
 
Document
();
eventDoc.put(
"type"
, 
"event"
);
eventDoc.put(
"userid"
, 
"abc123"
);
eventDoc.put(
"eventType"
, 
"addedToBasket"
);
eventDoc.put(
"productId"
, 
"1000042"
);
eventDoc.put(
"date"
, 
"2019-01-28T10:44:22.000Z"
);
PutDocumentOptions
 
documentOptions
 
=
    
new
 
PutDocumentOptions
.Builder()
        .db(
"events"
)
        .docId(
"0007241142412418284"
)
        .document(eventDoc)
        .build();
DocumentResult
 
response
 
=
    service.putDocument(documentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 eventDoc = {
  
type
: 
'event'
,
  
userid
: 
'abc123'
,
  
eventType
: 
'addedToBasket'
,
  
productId
: 
'1000042'
,
  
date
: 
'2019-01-28T10:44:22.000Z'
};
service.
putDocument
({
  
db
: 
'events'
,
 Tip: 
You can customize creating a document for the programming language that you want to use by selecting the language in the code
examples.
Cloudant
   
189  
docId
: 
'0007241142412418284'
,
  
document
: eventDoc
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 Document, CloudantV1
service = CloudantV1.new_instance()
event_doc = Document(
  
type
=
'event'
,
  userid=
'abc123'
,
  eventType=
'addedToBasket'
,
  productId=
'1000042'
,
  date=
'2019-01-28T10:44:22.000Z'
)
response = service.put_document(
  db=
'events'
,
  doc_id=
'0007241142412418284'
,
  document=event_doc
).get_result()
print
(response)
Go
eventDoc := cloudantv1.Document{}
eventDoc.SetProperty(
"type"
, 
"event"
)
eventDoc.SetProperty(
"userid"
, 
"abc123"
)
eventDoc.SetProperty(
"eventType"
, 
"addedToBasket"
)
eventDoc.SetProperty(
"productId"
, 
"1000042"
)
eventDoc.SetProperty(
"date"
, 
"2019-01-28T10:44:22.000Z"
)
putDocumentOptions := service.NewPutDocumentOptions(
  
"events"
,
  
"0007241142412418284"
,
)
putDocumentOptions.SetDocument(&eventDoc)
documentResult, response, err := service.PutDocument(putDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The response is a JSON document that contains the ID of the created document, the revision string, and 
"ok": true
.
If you didn't provide an 
_id
 field, IBM Cloudant generates one automatically as a 
UUID
.
A failure to create the document results in a response that contains a description of the error.
Cloudant
   
190See an example response after successfully creating a document:
{
  
"id"
:
 
"exampleid"
,
  
"ok"
:
 
true
,
  
"rev"
:
 
"2-056f5f44046ecafc08a2bc2b9c229e20"
}
Reading a document
The steps shown here demonstrate how to read a document:
a
. 
Send a 
GET
 request to retrieve a document.
b
. 
Run the following command: 
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID
.
Recall that for a partitioned database the 
$DOCUMENT_ID
 is formed of a partition key part and a document key part.
If you don't know the 
_id
 for a particular document, you can 
query the database
 for all documents.
See an example of retrieving a document by using HTTP:
GET
 
/$DATABASE/$DOCUMENT_ID
 
HTTP/1.1
See an example of retrieving a document:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/products/small-appliances:1000042"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Document;
import
 com.ibm.cloud.cloudant.v1.model.GetDocumentOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetDocumentOptions
 
documentOptions
 
=
    
new
 
GetDocumentOptions
.Builder()
        .db(
"products"
)
        .docId(
"small-appliances:1000042"
)
        .build();
Document
 
response
 
=
    service.getDocument(documentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
 Tip: 
If the write 
quorum
 can't be met during an attempt to create a document, a 
202
 response
 is returned.
 Note: 
Due to the distributed, eventually consistent nature of IBM Cloudant, reads might return stale data. In particular, data written recently,
even by the same client, might not be returned from a read request immediately following the write request. 
To work around this behavior, a
client can cache the state of data locally. Caching also helps to keep request counts down, increase application performance, and decrease
load on the database cluster. This behavior also applies to other read 
requests such as to MapReduce and search indexes.
 Tip: 
You can customize this section for the programming language that you want to use by selecting the language in the code examples.
Cloudant
   
191service.
getDocument
({
  
db
: 
'products'
,
  
docId
: 
'small-appliances:1000042'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_document(
  db=
'products'
,
  doc_id=
'small-appliances:1000042'
).get_result()
print
(response)
Go
getDocumentOptions := service.NewGetDocumentOptions(
  
"products"
,
  
"small-appliances:1000042"
,
)
document, response, err := service.GetDocument(getDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(document, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The response contains the document that you requested, or a description of the error if the document can't be retrieved.
See an example response of retrieving a document:
{
  
"_id"
:
 
"exampleid"
,
  
"brand"
:
 
"Foo"
,
  
"colours"
:
 
[
    
"red"
,
    
"green"
,
    
"black"
,
    
"blue"
  
]
,
  
"description"
:
 
"Slim Colourful Design Electronic Cooking Appliance for ..."
,
  
"image"
:
 
"assets/img/0gmsnghhew.jpg"
,
  
"keywords"
:
 
[
    
"Foo"
,
    
"Scales"
,
    
"Weight"
,
    
"Digital"
,
Cloudant
   
192    
"Kitchen"
  
]
,
  
"name"
:
 
"Digital Kitchen Scales"
,
  
"price"
:
 
14.99
,
  
"productid"
:
 
"1000042"
,
  
"taxonomy"
:
 
[
    
"Home"
,
    
"Kitchen"
,
    
"Small Appliances"
  
]
,
  
"type"
:
 
"product"
}
Query parameters
You can add some query parameters to the URL, for example 
/mydatabase/doc?attachments=true&conflicts=true
.
All parameters are optional.
Table 1. Query parameters
Name
Type
Description
Default
attachments
Boolean
Includes attachments bodies in response.
False
att_encoding_info
Boolean
Includes encoding information in attachment stubs if the particular attachment is
compressed.
False
atts_since
Array of revision
strings
Includes attachments only since specified revisions. Doesn't include attachments for
specified revisions.
[]
conflicts
Boolean
Includes information about conflicts in documents.
False
deleted_conflicts
Boolean
Includes information about deleted conflicted revisions.
False
latest
Boolean
Forces retrieval of the most recent "leaf" revision, no matter what revision was
requested.
False
local_seq
Boolean
Includes last update sequence number for the document.
False
meta
Boolean
Same as specifying the 
conflicts
, 
deleted_conflicts
, and 
open_revs
 query
parameters.
False
open_revs
Array or 
all
Retrieves documents of specified leaf revisions. Additionally, it accepts the value 
all
to return all leaf revisions.
[]
rev
String
Retrieves document of specified revision.
revs
Boolean
Includes list of all known document revisions.
False
revs_info
Boolean
Includes detailed information for all known document revisions.
False
Read many
To fetch more than one document at a time, 
query the database
 by using the 
include_docs
 option.
Updating a document
To update a document, send a 
PUT
 or 
POST
 request with the updated JSON content and the latest 
_rev
 value to
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID
. You can also use this 
PUT
 
method to create a document, in which case you don't
need to supply the most recent 
_rev
 value.
Cloudant
   
193Recall that for a partitioned database the 
$DOCUMENT_ID
 is formed from a partition key part and a document key part.
If you fail to provide the most recent 
_rev
 when you attempt to update an existing document, IBM Cloudant responds with a 
409 error
. This error
prevents 
you from overwriting data that were changed by other processes. If the write 
quorum
 can't be met, a 
202
 response
 is returned.
Any document update can lead to a conflict, especially when you replicate updated documents. For more information about avoiding and resolving
conflicts, see the 
Document versioning and MVCC guide
.
See an example of updating a document by using HTTP:
POST
 
/$DATABASE
 
HTTP/1.1
See examples of updating a document:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/products"
 -H 
"Content-Type: application/json"
 --data
 
'{ "_id": "small-appliances:1000042", "_rev": "1-967a00dff5e02add41819138abb3284d", "type": "product", "productid":
 
"1000042", "brand": "Salter", "name": "Digital Kitchen Scales", "description": "Slim Colourful Design Electronic Cooking
 
Appliance for Home / Kitchen, Weigh up to 5kg + Aquatronic for Liquids ml + fl. oz. 15Yr Guarantee - Green", "price: 14.99,
 
"image": "assets/img/0gmsnghhew.jpg" }'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Document;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PostDocumentOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Document
 
productsDocument
 
=
 
new
 
Document
();
productsDocument.setId(
"small-appliances:1000042"
);
productsDocument.setRev(
"1-967a00dff5e02add41819138abb3284d"
);
productsDocument.put(
"type"
, 
"product"
);
productsDocument.put(
"productid"
, 
"1000042"
);
productsDocument.put(
"brand"
, 
"Salter"
);
productsDocument.put(
"name"
, 
"Digital Kitchen Scales"
);
productsDocument.put(
"description"
, 
"Slim Colourful Design Electronic"
    + 
"Cooking Appliance for Home/Kitchen, Weigh up to 5kg + Aquatronic"
    + 
"for Liquids ml + fl. oz. 15Yr Guarantee - Green"
);
productsDocument.put(
"price"
, 
14.99
);
productsDocument.put(
"image"
, 
"assets/img/0gmsnghhew.jpg"
);
PostDocumentOptions
 
documentOptions
 
=
    
new
 
PostDocumentOptions
.Builder()
        .db(
"products"
)
        .document(productsDocument)
        .build();
DocumentResult
 
response
 
=
    service.postDocument(documentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 productsDoc = {
  
_id
: 
'small-appliances:1000042'
,
  
_rev
: 
'1-967a00dff5e02add41819138abb3284d'
 Tip: 
You can customize this topic for the programming language that you want to use by selecting the language in the code examples.
Cloudant
   
194  
type
: 
'product'
,
  
productid
: 
'1000042'
,
  
brand
: 
'Salter'
,
  
name
: 
'Digital Kitchen Scales'
,
  
description
: 
'Slim Colourful Design Electronic Cooking Appliance for Home / Kitchen, Weigh up to 5kg + Aquatronic for
 
Liquids ml + fl. oz. 15Yr Guarantee - Green'
,
  
price
: 
14.99
,
  
image
: 
'assets/img/0gmsnghhew.jpg'
};
service.
postDocument
({
  
db
: 
'products'
,
  
document
: productsDoc
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 Document, CloudantV1
service = CloudantV1.new_instance()
products_doc = Document(
  
id
=
"small-appliances:1000042"
,
  rev=
"1-967a00dff5e02add41819138abb3284d"
  
type
=
"product"
,
  productid=
"1000042"
,
  brand=
"Salter"
,
  name=
"Digital Kitchen Scales"
,
  description=
"Slim Colourful Design Electronic Cooking Appliance for Home / Kitchen, Weigh up to 5kg + Aquatronic for
 
Liquids ml + fl. oz. 15Yr Guarantee - Green"
,
  price=
14.99
,
  image=
"assets/img/0gmsnghhew.jpg"
)
response = service.post_document(db=
'products'
, document=products_doc).get_result()
print
(response)
Go
productsDoc := cloudantv1.Document{
  ID: core.StringPtr(
"small-appliances:1000042"
),
}
productsDoc.Rev = 
"1-967a00dff5e02add41819138abb3284d"
productsDoc.SetProperty(
"type"
, 
"product"
)
productsDoc.SetProperty(
"productid"
, 
"1000042"
)
productsDoc.SetProperty(
"brand"
, 
"Salter"
)
productsDoc.SetProperty(
"name"
, 
"Digital Kitchen Scales"
)
productsDoc.SetProperty(
"description"
, 
"Slim Colourful Design Electronic Cooking Appliance for Home / Kitchen, Weigh up to
 
5kg + Aquatronic for Liquids ml + fl. oz. 15Yr Guarantee - Green"
)
productsDoc.SetProperty(
"price"
, 
14.99
)
productsDoc.SetProperty(
"image"
, 
"assets/img/0gmsnghhew.jpg"
)
postDocumentOptions := service.NewPostDocumentOptions(
  
"products"
,
)
postDocumentOptions.SetDocument(&productsDoc)
documentResult, response, err := service.PostDocument(postDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Cloudant
   
195Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See an example of JSON data that contains an updated document:
{
   
"id"
:
 
"exampleid"
,
   
"ok"
:
 
true
,
   
"rev"
:
 
"2-056f5f44046ecafc08a2bc2b9c229e20"
}
Recall that for a partitioned database the 
$DOCUMENT_ID
 is formed from a partition key part and a document key part.
The response contains the ID and the new revision of the document, or an error message if the update failed.
See an example response after a successful update:
{
  
"id"
:
 
"exampleid"
,
  
"ok"
:
 
true
,
  
"rev"
:
 
"2-056f5f44046ecafc08a2bc2b9c229e20"
}
Deleting a document
The steps shown here demonstrate how to delete a document.
a
. 
Send a 
DELETE
 request with the document's most recent 
_rev
 in the query string.
b
. 
Run the following command: 
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID
. The response contains the ID and the new
revision of the document, or an error message if the delete failed.
IBM Cloudant doesn't completely delete the specified document. Instead, it leaves a 
tombstone
 with basic information about the document. The
tombstone is required so that the delete action can be replicated to 
other copies of the database. Since the tombstones stay in the database
indefinitely, creating new documents and deleting them increases the disk space usage of a database. They might also increase the query time for
the primary index, which 
is used to look up documents by their ID.
The following steps show you how to delete a request by using HTTP.
a
. 
Send a 
DELETE
 request with the document's most recent 
_rev
 in the query string by using HTTP.
b
. 
Run the following command: 
DELETE /$DATABASE/$DOCUMENT_ID?rev=$REV HTTP/1.1
.
The following code examples show you how to delete a document by using the command line.
Curl
# make sure $JSON contains the correct `_rev` value!
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X DELETE 
"
$SERVICE_URL
/events/0007241142412418284?rev=2-
9a0d1cd9f40472509e9aac6461837367"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
 Note: 
If you fail to provide the most recent 
_rev
, IBM Cloudant responds with a 
409 error
. This error prevents you overwriting data that
were changed by 
other clients. If the write 
quorum
 can't be met, a 
202
 response
 is returned.
Cloudant
   
196import
 com.ibm.cloud.cloudant.v1.model.DeleteDocumentOptions;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteDocumentOptions
 
documentOptions
 
=
    
new
 
DeleteDocumentOptions
.Builder()
        .db(
"events"
)
        .docId(
"0007241142412418284"
)
        .rev(
"2-9a0d1cd9f40472509e9aac6461837367"
)
        .build();
DocumentResult
 
response
 
=
    service.deleteDocument(documentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
deleteDocument
({
 
db
: 
'events'
,
 
docId
: 
'0007241142412418284'
,
 
rev
: 
'2-9a0d1cd9f40472509e9aac6461837367'
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_document(
 db=
'events'
,
 doc_id=
'0007241142412418284'
,
 rev=
'2-9a0d1cd9f40472509e9aac6461837367'
).get_result()
print
(response)
Go
deleteDocumentOptions := service.NewDeleteDocumentOptions(
 
"events"
,
 
"0007241142412418284"
,
)
deleteDocumentOptions.SetRev(
"2-9a0d1cd9f40472509e9aac6461837367"
)
documentResult, response, err := service.DeleteDocument(deleteDocumentOptions)
if
 err != 
nil
 {
 
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
Cloudant
   
197   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See an example response after a successful deletion request.
{
  
"id"
:
 
"exampleid"
,
  
"ok"
:
 
true
,
  
"rev"
:
 
"2-056f5f44046ecafc08a2bc2b9c229e20"
}
"Tombstone" documents
Tombstone documents are small documents that are kept in place within a database when the original document is deleted. Their purpose is to
allow the deletion to be replicated.
When the replication completes, the tombstones are no longer required. Automatic compaction helps ensure that only the minimal amount of data is
kept and transferred during replication. Nevertheless, tombstone documents aren't automatically removed.
Over time, as documents are created and deleted, the number of tombstone documents increases. Each tombstone is small, but gradually they add
to database disk space usage, and to the query time for the primary index. To reduce these effects, you 
might want to remove the tombstones.
Simple removal of "tombstone" documents
To remove tombstones manually, do the following steps:
a
. 
Create a database to hold the required documents.
The new database is intended to hold all documents except the tombstone documents.
a
. 
Set up a 
filtered replication
 to replicate documents from the original database to the new database.
Configure the filter so that documents with the "
_deleted
" attribute aren't replicated.
a
. 
When replication is complete, switch your application logic to use the new database.
b
. 
Verify that your applications work correctly with the new database.
When you're satisfied that everything is working correctly, you might want to delete the old database.
See an example filter to exclude deleted documents during a replication:
{
 
"_id"
:
 
"_design/filters"
,
 
"filters"
:
 
{
  
"deleted_filter"
:
 
"function(doc, req) { return !doc._deleted; };"
 
}
}
Advanced removal of tombstone documents
The 
simple removal technique
 works well, if documents aren't being updated in the source database while the replication takes place.
If updates are made during replication, it's possible that a complete document is replicated to the target database as normal, and is also deleted
from the source database, leaving a tombstone. The problem is that the tombstone is not replicated 
across to the target database because the
tombstone is excluded by the filter. Therefore, the document that was deleted from the source database is not deleted from the target database,
causing an inconsistency.
A solution is to do more advanced removal of tombstones by using a 
validate_doc_update
 function
.
A 
validate_doc_update
 function is stored in a design document. The function is run every time that a document is updated in the database. The
function can be used to prevent invalid or unauthorized document updates.
 Tip: 
In general, try to design and implement your applications to do the minimum necessary amount of deletion.
Cloudant
   
198The function works by using the following parameters:
The new version of the document.
The current version of the document in the database.
A user context, which provides details about the user that supplied the updated document.
The function inspects the request to determine whether the update is allowed to proceed. If the update is acceptable, the function returns. If the
update is not acceptable, a suitable error object is returned. In particular, if the user is not 
authorized to make the update, an 
unauthorized
 error
object is returned, along with an explanatory error message. Similarly, the requested update might not be allowed for some reason, such as when
some mandatory fields are absent 
from the new document. In that case, a 
forbidden
 error object is returned, again with an explanatory error
message.
For tombstone removal, a suitable 
validate_doc_update
 function would work as follows:
a
. 
If the update is to apply a change to an existing document (
oldDoc
) within the target database, the function allows the change by returning.
The reason is that the update affected a document that was copied to the target database during the replication, but then changed in the source
database during the replication. It's possible that the change was a 
DELETE
, resulting 
in a tombstone record in the target database. The tombstone
record is removed by a subsequent replication process at some point in the future. 2. The target database does not have a copy of the current
document, and the document to be updated 
has the 
_deleted
 property (indicating that it's a tombstone). Therefore, the updated document must
be a tombstone and was encountered before, so the update to the target database must be rejected.
See an example JavaScript 
validate_doc_update
 function to reject deleted documents not already present in the target database:
function
(
newDoc, oldDoc, userCtx
) {
 
// any update to an existing doc is OK
 
if
(oldDoc) {
  
return
;
 }
 
// reject tombstones for docs we don’t know about
 
if
(newDoc[
"_deleted"
]) {
  
throw
({forbidden : 
"Deleted document rejected"
});
 }
 
return
; 
// Not strictly necessary, but clearer.
}
To use a 
validate_doc_update
 function to remove tombstone documents:
a
. 
Stop replication from the source to the target database.
b
. 
If appropriate, delete the target database, then create a new target database.
c
. 
Add a suitable 
validate_doc_update
 function, similar to the example provided.
d
. 
Add it to a design document in the target database.
e
. 
Restart replication between the source and the (new) target database.
f
. 
When replication is complete, switch your application logic to use the new database.
g
. 
Verify that your applications work correctly with the new database.
When you're satisfied that everything is working correctly, you might want to delete the old database.
Here is another variation for using the 
validate_doc_update
 function to remove tombstone documents if possible.
a
. 
Add some metadata to the tombstone documents, for example, to record the deletion date.
b
. 
Use the function to inspect the metadata and allow deletion documents through if they must be applied to the target database.
This check helps ensure correct replication of the deletion.
Performance implications of tombstone removal
Tombstones are used for more consistent deletion of documents from databases. This purpose is especially important for mobile devices: without
tombstone documents, a deletion might not replicate correctly to a mobile device, with the result 
that documents might never be deleted from the
device.
If you re-create a database, for example, a new target for a replication. Any clients that use the target database as a server must work through all the
changes again because the database sequence numbers are likely to be different.
Cloudant
   
199Bulk operations
Use the bulk document API to create and update multiple documents at the same time within a single request. The basic operation is similar to
creating or updating a single document, except that you batch the document structure and information.
When you create new documents, the document ID is optional. For updating existing documents, you must provide the document ID, revision
information, and new document values.
Bulk request structure
For both inserts and updates, the basic structure of the JSON document in the request contains the following fields:
Table 1. Basic bulk request structure
Field
Description
Type
Optional
docs
List of document objects
Array of objects
No
Each 
docs
 array object has the following structure:
Table 2. Structure of the docs array object
Field
Description
Type
Optional
_id
Document ID
String
Optional only for new documents. Otherwise, it's mandatory.
_rev
Document revision
String
Mandatory for updates and deletes, not used for new
documents.
_deleted
Determines whether the document must be
deleted.
Boolean
(Optional) The default value is 
false
.
Recall that for a partitioned database the 
_id
 field is formed from a partition key part and a document key part.
See an example of using HTTP to create, update, or delete multiple documents:
POST
 
/$DATABASE/_bulk_docs
 
HTTP/1.1
Content-Type
: 
application/json
See an example of using the command line to create, update, or delete multiple documents:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/events/_bulk_docs"
 -H 
"Content-Type:
 
application/json"
 --data 
'{ "docs": [ { "_id": "0007241142412418284", "type": "event", "userid": "abc123", "eventType":
 
"addedToBasket", "productId": "1000042", "date": "2019-01-28T10:44:22.000Z" }, { "_id": "0008001142412418285", "type":
 
"event", "userid": "def456", "eventType": "addedToBasket", "productId": "1000043", "date": "2019-01-28T12:30:00.000Z" } ],
 
"new_edits": true }'
 Tip: 
If you're using a 
validate_doc_update
 function, avoid replicating that function to clients. This rule is to prevent the possibility of
unwanted side effects that result from having the function present on the client.
 Note: 
IBM Cloudant sync
 libraries don't replicate design documents, so replication of 
validate_doc_update
 functions is not normally a
problem for IBM Cloudant. 
However, other clients might replicate the design documents or 
validate_doc_update
 functions, potentially
resulting in unwanted side effects.
 Tip: 
A special case of bulk operations is the 
_bulk_get
 endpoint.
 Note: 
It is best not to use the 
new_edits
 field. By default, if conflicts exist, document updates fail and return an error to the client. However,
this option applies document revisions without checking for conflicts, so it is easy to 
accidentally end up with many conflicts.
Cloudant
   
200Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.BulkDocs;
import
 com.ibm.cloud.cloudant.v1.model.Document;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PostBulkDocsOptions;
import
 java.util.Arrays;
import
 java.util.List;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Document
 
eventDoc1
 
=
 
new
 
Document
();
eventDoc1.setId(
"0007241142412418284"
);
eventDoc1.put(
"type"
, 
"event"
);
eventDoc1.put(
"userid"
, 
"abc123"
);
eventDoc1.put(
"eventType"
, 
"addedToBasket"
);
eventDoc1.put(
"productId"
, 
"1000042"
);
eventDoc1.put(
"date"
, 
"2019-01-28T10:44:22.000Z"
);
Document
 
eventDoc2
 
=
 
new
 
Document
();
eventDoc2.setId(
"0007241142412418285"
);
eventDoc2.put(
"type"
, 
"event"
);
eventDoc2.put(
"userid"
, 
"abc234"
);
eventDoc2.put(
"eventType"
, 
"addedToBasket"
);
eventDoc2.put(
"productId"
, 
"1000050"
);
eventDoc2.put(
"date"
, 
"2019-01-28T10:44:22.000Z"
);
BulkDocs
 
bulkDocs
 
=
 
new
 
BulkDocs
.Builder()
    .docs(Arrays.asList(eventDoc1, eventDoc2))
    .build();
PostBulkDocsOptions
 
bulkDocsOptions
 
=
 
new
 
PostBulkDocsOptions
.Builder()
    .db(
"events"
)
    .bulkDocs(bulkDocs)
    .build();
List<DocumentResult> response =
    service.postBulkDocs(bulkDocsOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 eventDoc1 = {
   
_id
: 
'0007241142412418284'
,
   
type
: 
'event'
,
   
userid
: 
'abc123'
,
   
eventType
:
'addedToBasket'
,
   
productId
: 
'1000042'
,
   
date
: 
'2019-01-28T10:44:22.000Z'
}
const
 eventDoc2 = {
   
_id
: 
'0007241142412418285'
,
   
type
: 
'event'
,
   
userid
: 
'abc234'
,
   
eventType
: 
'addedToBasket'
,
   
productId
: 
'1000050'
,
   
date
: 
'2019-01-25T20:00:00.000Z'
}
const
 bulkDocs = {  
docs
: [eventDoc1, eventDoc2] }
Cloudant
   
201service.
postBulkDocs
({
   
db
: 
'events'
,
   
bulkDocs
: bulkDocs
}).
then
(
response
 =>
 {
   
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 Document, CloudantV1, BulkDocs
service = CloudantV1.new_instance()
event_doc_1 = Document(
   
id
=
"0007241142412418284"
,
   
type
=
"event"
,
   userid=
"abc123"
,
   eventType=
"addedToBasket"
,
   productId=
"1000042"
,
   date=
"2019-01-28T10:44:22.000Z"
)
event_doc_2 = Document(
   
id
=
"0007241142412418285"
,
   
type
=
"event"
,
   userid=
"abc234"
,
   eventType=
"addedToBasket"
,
   productId=
"1000050"
,
   date=
"2019-01-25T20:00:00.000Z"
)
bulk_docs = BulkDocs(docs=[event_doc_1, event_doc_2])
response = service.post_bulk_docs(
   db=
'events'
,
   bulk_docs=bulk_docs
).get_result()
print
(response)
Go
eventDoc1 := cloudantv1.Document{
   ID: core.StringPtr(
"0007241142412418284"
),
}
eventDoc1.SetProperty(
"type"
, 
"event"
)
eventDoc1.SetProperty(
"userid"
, 
"abc123"
)
eventDoc1.SetProperty(
"eventType"
, 
"addedToBasket"
)
eventDoc1.SetProperty(
"productId"
, 
"1000042"
)
eventDoc1.SetProperty(
"date"
, 
"2019-01-28T10:44:22.000Z"
)
eventDoc2 := cloudantv1.Document{
   ID: core.StringPtr(
"0007241142412418285"
),
}
eventDoc2.SetProperty(
"type"
, 
"event"
)
eventDoc2.SetProperty(
"userid"
, 
"abc234"
)
eventDoc2.SetProperty(
"eventType"
, 
"addedToBasket"
)
eventDoc2.SetProperty(
"productId"
, 
"1000050"
)
eventDoc2.SetProperty(
"date"
, 
"2019-01-25T20:00:00.000Z"
)
postBulkDocsOptions := service.NewPostBulkDocsOptions(
   
"events"
,
)
bulkDocs, err := service.NewBulkDocs(
   []cloudantv1.Document{
    eventDoc1,
    eventDoc2,
   },
)
if
 err != 
nil
 {
   
panic
(err)
Cloudant
   
202}
postBulkDocsOptions.SetBulkDocs(bulkDocs)
documentResult, response, err := service.PostBulkDocs(postBulkDocsOptions)
if
 err != 
nil
 {
   
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See an example JSON describing the update, creation, and deletion of three documents in one bulk request:
[
  
{
    
"id"
:
 
"0007241142412418284"
,
    
"ok"
:
 
true
,
    
"rev"
:
 
"1-5005d65514fe9e90f8eccf174af5dd64"
  
}
,
  
{
    
"id"
:
 
"0008001142412418285"
,
    
"ok"
:
 
true
,
    
"rev"
:
 
"1-2d7810b054babeda4812b3924428d6d6"
  
}
]
Bulk request responses
The HTTP status code that is received in response indicates whether the request was fully or partially successful. In the response body itself, you get
an array with detailed information for each document in the request.
Table 3. HTTP status codes
Code
Description
201
The request did succeed, but this success doesn't imply all documents were updated. Inspect the response body to determine the
status of each requested change, and 
address any problems
.
202
For at least one document, the write 
quorum
 wasn't met.
See an example response from a bulk request:
[
    
{
    
"ok"
:
true
,
    
"id"
:
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
    
"rev"
:
"1-54dd23d6a630d0d75c2c5d4ef894454e"
    
}
,
    
{
    
"ok"
:
true
,
    
"id"
:
"5a049246-179f-42ad-87ac-8f080426c17c"
,
    
"rev"
:
"1-0cde94a828df5cdc0943a10f3f36e7e5"
Cloudant
   
203    
}
,
    
{
    
"ok"
:
true
,
    
"id"
:
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
    
"rev"
:
"1-a2b6e5dac4e0447e7049c8c540b309d6"
    
}
]
Inserting documents in bulk
To insert documents in bulk into a database, you need to supply a JSON structure with the array of documents that you want to add to the database.
You can either include a document ID for each document, or allow the document ID to be automatically 
generated.
See an example JSON for a bulk insert of three documents:
{
 
"docs"
:
 
[
   
{
    
"name"
:
 
"Nicholas"
,
    
"age"
:
 
45
,
    
"gender"
:
 
"male"
,
    
"_id"
:
 
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
    
"_attachments"
:
 
{
    
}
   
}
,
   
{
    
"name"
:
 
"Taylor"
,
    
"age"
:
 
50
,
    
"gender"
:
 
"male"
,
    
"_id"
:
 
"5a049246-179f-42ad-87ac-8f080426c17c"
,
    
"_attachments"
:
 
{
    
}
   
}
,
   
{
    
"name"
:
 
"Owen"
,
    
"age"
:
 
51
,
    
"gender"
:
 
"male"
,
    
"_id"
:
 
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
    
"_attachments"
:
 
{
    
}
   
}
 
]
}
The return code from a successful bulk insertion is 
201
. The content of the returned structure indicates success or other information messages on 
a
per-document basis.
See an example response header after successful bulk insert of three documents:
201 Created
Cache-Control
: 
must-revalidate
Content-Length
: 
269
Content-Type
: 
application/json
Date
: 
Mon, 04 Mar 2013 14:06:20 GMT
server
: 
CouchDB/1.0.2 (Erlang OTP/R14B)
x-couch-request-id
: 
e8ff64d5
The returned JSON contains a list of the documents that were created, including their revision and ID values.
The content and structure of the returned JSON depends on the transaction semantics that are used for the bulk update. For more information, see
Bulk documents transaction semantics
.
Conflicts and validation errors that occur when you update documents in bulk must be handled separately. For more information, see 
Bulk document
validation and conflict errors
.
See an example response content after successful bulk insert of two documents:
Cloudant
   
204[
    
{
    
"ok"
:
 
true
,
    
"id"
:
 
"id1"
,
    
"rev"
:
 
"2-402c81fee7ae6e723ff08bb166703a50"
    
}
,
    
{
    
"id"
:
 
"id2"
,
    
"error"
:
 
"conflict"
,
    
"reason"
:
 
"Document update conflict."
    
}
]
Updating documents in bulk
The bulk document update procedure is similar to the insertion procedure, except that you must specify the document ID and current revision for
every document in the bulk update JSON string.
See an example of using HTTP to do a bulk update:
POST
 
/$DATABASE/_bulk_docs
 
HTTP/1.1
Accept
: 
application/json
See an example of using the command line to do a bulk update:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/events/_bulk_docs"
 -H 
"Content-Type:
 
application/json"
 --data 
'{ "docs": [ { "_id": "0007241142412418284", "type": "event", "userid": "abc123", "eventType":
 
"addedToBasket", "productId": "1000042", "date": "2019-01-28T10:44:22.000Z" }, { "_id": "0008001142412418285", "type":
 
"event", "userid": "def456", "eventType": "addedToBasket", "productId": "1000043", "date": "2019-01-28T12:30:00.000Z" } ],
 
"new_edits": true }'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.BulkDocs;
import
 com.ibm.cloud.cloudant.v1.model.Document;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PostBulkDocsOptions;
import
 java.util.Arrays;
import
 java.util.List;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Document
 
eventDoc1
 
=
 
new
 
Document
();
eventDoc1.setId(
"0007241142412418284"
);
eventDoc1.put(
"type"
, 
"event"
);
eventDoc1.put(
"userid"
, 
"abc123"
);
eventDoc1.put(
"eventType"
, 
"addedToBasket"
);
eventDoc1.put(
"productId"
, 
"1000042"
);
eventDoc1.put(
"date"
, 
"2019-01-28T10:44:22.000Z"
);
Document
 
eventDoc2
 
=
 
new
 
Document
();
eventDoc2.setId(
"0007241142412418285"
);
eventDoc2.put(
"type"
, 
"event"
);
eventDoc2.put(
"userid"
, 
"abc234"
);
eventDoc2.put(
"eventType"
, 
"addedToBasket"
);
eventDoc2.put(
"productId"
, 
"1000050"
);
eventDoc2.put(
"date"
, 
"2019-01-28T10:44:22.000Z"
);
BulkDocs
 
bulkDocs
 
=
 
new
 
BulkDocs
.Builder()
    .docs(Arrays.asList(eventDoc1, eventDoc2))
    .build();
PostBulkDocsOptions
 
bulkDocsOptions
 
=
 
new
 
PostBulkDocsOptions
.Builder()
    .db(
"events"
)
Cloudant
   
205    .bulkDocs(bulkDocs)
    .build();
List<DocumentResult> response =
    service.postBulkDocs(bulkDocsOptions).execute()
        .getResult();
System.out.println(response);
Python
from
 ibmcloudant.cloudant_v1 
import
 Document, CloudantV1, BulkDocs
service = CloudantV1.new_instance()
event_doc_1 = Document(
   
id
=
"0007241142412418284"
,
   
type
=
"event"
,
   userid=
"abc123"
,
   eventType=
"addedToBasket"
,
   productId=
"1000042"
,
   date=
"2019-01-28T10:44:22.000Z"
)
event_doc_2 = Document(
   
id
=
"0007241142412418285"
,
   
type
=
"event"
,
   userid=
"abc234"
,
   eventType=
"addedToBasket"
,
   productId=
"1000050"
,
   date=
"2019-01-25T20:00:00.000Z"
)
bulk_docs = BulkDocs(docs=[event_doc_1, event_doc_2])
response = service.post_bulk_docs(
   db=
'events'
,
   bulk_docs=bulk_docs
).get_result()
print
(response)
Go
eventDoc1 := cloudantv1.Document{
   ID: core.StringPtr(
"0007241142412418284"
),
}
eventDoc1.SetProperty(
"type"
, 
"event"
)
eventDoc1.SetProperty(
"userid"
, 
"abc123"
)
eventDoc1.SetProperty(
"eventType"
, 
"addedToBasket"
)
eventDoc1.SetProperty(
"productId"
, 
"1000042"
)
eventDoc1.SetProperty(
"date"
, 
"2019-01-28T10:44:22.000Z"
)
eventDoc2 := cloudantv1.Document{
   ID: core.StringPtr(
"0007241142412418285"
),
}
eventDoc2.SetProperty(
"type"
, 
"event"
)
eventDoc2.SetProperty(
"userid"
, 
"abc234"
)
eventDoc2.SetProperty(
"eventType"
, 
"addedToBasket"
)
eventDoc2.SetProperty(
"productId"
, 
"1000050"
)
eventDoc2.SetProperty(
"date"
, 
"2019-01-25T20:00:00.000Z"
)
postBulkDocsOptions := service.NewPostBulkDocsOptions(
   
"events"
,
)
bulkDocs, err := service.NewBulkDocs(
   []cloudantv1.Document{
     eventDoc1,
     eventDoc2,
    },
)
Cloudant
   
206if
 err != 
nil
 {
   
panic
(err)
}
postBulkDocsOptions.SetBulkDocs(bulkDocs)
documentResult, response, err := service.PostBulkDocs(postBulkDocsOptions)
if
 err != 
nil
 {
   
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 eventDoc1 = {
   
_id
: 
'0007241142412418284'
,
   
type
: 
'event'
,
   
userid
: 
'abc123'
,
   
eventType
:
'addedToBasket'
,
   
productId
: 
'1000042'
,
   
date
: 
'2019-01-28T10:44:22.000Z'
}
const
 eventDoc2 = {
   
_id
: 
'0007241142412418285'
,
   
type
: 
'event'
,
   
userid
: 
'abc234'
,
   
eventType
: 
'addedToBasket'
,
   
productId
: 
'1000050'
,
   
date
: 
'2019-01-25T20:00:00.000Z'
}
const
 bulkDocs = { 
docs
: [eventDoc1, eventDoc2] };
service.
postBulkDocs
({
   
db
: 
'events'
,
   
bulkDocs
: bulkDocs
}).
then
(
response
 =>
 {
   
console
.
log
(response.
result
);
});
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See an example JSON structure to request bulk update of documents:
{
 
"docs"
:
 
[
   
{
    
"name"
:
 
"Nicholas"
,
    
"age"
:
 
45
,
    
"gender"
:
 
"female"
,
Cloudant
   
207    
"_id"
:
 
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
    
"_attachments"
:
 
{
    
}
,
    
"_rev"
:
 
"1-54dd23d6a630d0d75c2c5d4ef894454e"
   
}
,
   
{
    
"name"
:
 
"Taylor"
,
    
"age"
:
 
50
,
    
"gender"
:
 
"female"
,
    
"_id"
:
 
"5a049246-179f-42ad-87ac-8f080426c17c"
,
    
"_attachments"
:
 
{
    
}
,
    
"_rev"
:
 
"1-0cde94a828df5cdc0943a10f3f36e7e5"
   
}
,
   
{
    
"name"
:
 
"Owen"
,
    
"age"
:
 
51
,
    
"gender"
:
 
"female"
,
    
"_id"
:
 
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
    
"_attachments"
:
 
{
    
}
,
    
"_rev"
:
 
"1-a2b6e5dac4e0447e7049c8c540b309d6"
   
}
 
]
}
The return JSON structure summarizes the updated documents, with the new revision and ID information.
See an example JSON structure that is returned after bulk update:
[
    
{
        
"ok"
:
true
,
        
"id"
:
"96f898f0-f6ff-4a9b-aac4-503992f31b01"
,
        
"rev"
:
"2-ff7b85665c4c297838963c80ecf481a3"
  
    
}
,
    
{
        
"ok"
:
true
,
        
"id"
:
"5a049246-179f-42ad-87ac-8f080426c17c"
,
        
"rev"
:
"2-9d5401898196997853b5ac4163857a29"
    
}
,
    
{
        
"ok"
:
true
,
        
"id"
:
"d1f61e66-7708-4da6-aa05-7cbc33b44b7e"
,
        
"rev"
:
"2-cbdef49ef3ddc127eff86350844a6108"
    
}
]
Deleting documents in bulk
To delete a document from the database, you must provide the ID and the revision of a specific document with the 
"_deleted": true
 field.
See an example JSON structure to request bulk delete of two documents:
The return JSON structure summarizes the deleted documents, with the new revision and ID information.
{
 
"docs"
:
 
[
   
{
    
"_id"
:
 
"person34567"
,
    
"_deleted"
:
 
true
,
    
"_rev"
:
 
"2-54dd23d6a630d0d75c2c5d4ef894454e"
   
}
,
   
{
    
"_id"
:
 
"person568"
,
    
"_deleted"
:
 
true
,
Cloudant
   
208    
"_rev"
:
 
"3-8a245604ee5e829d7fbd1b456aed01ac"
   
}
    
]
}
See an example JSON structure that is returned after bulk delete:
[
    
{
        
"ok"
:
 
true
,
        
"id"
:
 
"person34567"
,
        
"rev"
:
 
"3-674ccbb6ec6fe6d7ba0fb30a5eecf664"
    
}
,
    
{
        
"ok"
:
 
true
,
        
"id"
:
 
"person568"
,
        
"rev"
:
 
"4-c6067e21e97557f54d29282461843037"
    
}
]
Bulk documents transaction semantics
If your request receives a 
202
 response
, the only certainty is that some of the document tasks were processed completely. The response body
contains 
the list of documents that were successfully inserted or updated during the process.
A successful document update is indicated by the presence of a new 
_rev
 parameter for the document, indicating that a new document revision
was successfully created.
If a document update failed, then you get an 
error
 of type 
conflict
 for that document. In this case, no new revision was created. You must
submit the document update again, with the same revision tag, to retry the document 
update.
See an example bulk update response with errors:
[
 
{
   
"id"
 
:
 
"FishStew"
,
   
"error"
 
:
 
"conflict"
,
   
"reason"
 
:
 
"Document update conflict."
 
}
,
 
{
   
"id"
 
:
 
"LambStew"
,
   
"error"
 
:
 
"conflict"
,
   
"reason"
 
:
 
"Document update conflict."
 
}
,
 
{
   
"id"
 
:
 
"7f7638c86173eb440b8890839ff35433"
,
   
"error"
 
:
 
"conflict"
,
   
"reason"
 
:
 
"Document update conflict."
 
}
]
Bulk document validation and conflict errors
The JSON returned by the 
_bulk_docs
 operation consists of an array of JSON structures, one for each document in the original submission. The
returned JSON structure must be examined to ensure that all of the documents that were 
submitted in the original request were successfully added
to the database.
The structure of the returned information is shown in the following tables:
Table 4. Structure of JSON returned
Field
Description
Type
docs
List of document objects
Array of objects
Each 
docs
 array object has the following structure:
Cloudant
   
209Table 5. Structure for the docs array object
Field
Description
Type
id
Document ID
String
error
Error type
String
reason
Error string with extended reason
String
When a document (or document revision) is not correctly committed to the database because of an error, you must check the 
error
 field to
determine error type and course of action. The error is one of 
conflict
 
or 
forbidden
.
conflict
The document as submitted is in conflict. If you used the default bulk transaction mode, then the new revision wasn't created. You must resubmit the
document to the database.
Conflict resolution that uses the bulk docs interface is identical to the resolution procedures outlined in the 
Conflicts
 documentation.
forbidden
Entries with this error type indicate that the validation routine that was applied to the document during submission returned an error.
See an example JavaScript to produce 
forbidden
 error as part of a validation function:
throw
({
forbidden
: 
'invalid recipe ingredient'
});
See an example error message from a validation function:
{
 
"id"
 
:
 
"7f7638c86173eb440b8890839ff35433"
,
 
"error"
 
:
 
"forbidden"
,
 
"reason"
 
:
 
"invalid recipe ingredient"
}
The 
_bulk_get
 endpoint
You might need to access all the available information about multiple documents. The 
_bulk_get
 endpoint is similar to the 
_all_docs
 endpoint,
but returns information about the requested documents only.
Like the 
_bulk_docs
 endpoint, a JSON document that is supplied in the request includes an array that identifies all the documents of interest.
See an example of using HTTP to run the bulk 
GET
request of document information:
POST
 
/$DATABASE/_bulk_get
 
HTTP/1.1
Accept
: 
application/json
See an example of using the command line to run the bulk 
GET
request:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X POST 
"
$SERVICE_URL
/orders/_bulk_get"
 -H 
"Content-Type:
 
application/json"
 --data 
'{
  "docs": [
    {
      "id": "order00067",
      "rev": "3-917fa2381192822767f010b95b45325b"
    },
    {
      "id": "order00067"
      "rev": "4-a5be949eeb7296747cc271766e9a498b"
    }
   ],
}'
Cloudant
   
210Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.BulkGetQueryDocument;
import
 com.ibm.cloud.cloudant.v1.model.BulkGetResult;
import
 com.ibm.cloud.cloudant.v1.model.PostBulkGetOptions;
import
 java.util.ArrayList;
import
 java.util.List;
Cloudant
 
service
 
=
 Cloudant.newInstance();
String
 
docId
 
=
 
"order00067"
;
List<BulkGetQueryDocument> bulkGetDocs = 
new
 
ArrayList
<>();
bulkGetDocs.add(
    
new
 
BulkGetQueryDocument
.Builder()
        .id(docId)
        .rev(
"3-917fa2381192822767f010b95b45325b"
)
        .build());
bulkGetDocs.add(
    
new
 
BulkGetQueryDocument
.Builder()
        .id(docId)
        .rev(
"4-a5be949eeb7296747cc271766e9a498b"
)
        .build());
PostBulkGetOptions
 
bulkGetOptions
 
=
 
new
 
PostBulkGetOptions
.Builder()
    .db(
"orders"
)
    .docs(bulkGetDocs)
    .build();
BulkGetResult
 
response
 
=
    service.postBulkGet(bulkGetOptions).execute()
        .getResult();
System.out.println(response);
Python
from
 ibmcloudant.cloudant_v1 
import
 BulkGetQueryDocument, CloudantV1
service = CloudantV1.new_instance()
doc_id = 
'order00067'
bulk_get_doc_1 = BulkGetQueryDocument(
    
id
=doc_id,
    rev=
'3-917fa2381192822767f010b95b45325b'
)
bulk_get_doc_2 = BulkGetQueryDocument(
    
id
=doc_id,
    rev=
'4-a5be949eeb7296747cc271766e9a498b'
)
response = service.post_bulk_get(
    db=
'orders'
,
    docs=[bulk_get_doc_1, bulk_get_doc_2],
).get_result()
print
(response)
Go
docID := 
"order00067"
bulkGetDocs := []cloudantv1.BulkGetQueryDocument{
   {
    ID: &docID,
    Rev: core.StringPtr(
"3-917fa2381192822767f010b95b45325b"
),
   },
   {
    ID: &docID,
Cloudant
   
211    Rev: core.StringPtr(
"4-a5be949eeb7296747cc271766e9a498b"
),
   },
}
postBulkGetOptions := service.NewPostBulkGetOptions(
   
"orders"
,
   bulkGetDocs,
)
bulkGetResult, response, err := service.PostBulkGet(postBulkGetOptions)
if
 err != 
nil
 {
   
panic
(err)
}
b, _ := json.MarshalIndent(bulkGetResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
Node
const
 service = 
Cloudant
V1.
newInstance
({});
const
 docId = 
'order00067'
;
const
 bulkGetDoc1 = {
   
id
: docId,
   
rev
: 
'3-917fa2381192822767f010b95b45325b'
};
const
 bulkGetDoc2 = {
   
id
: docId,
   
rev
: 
'4-a5be949eeb7296747cc271766e9a498b'
};
const
 bulkGetDocs = [bulkGetDoc1, bulkGetDoc2];
const
 postBulkGetParams = {
   
db
: 
'orders'
,
   
docs
: bulkGetDocs,
};
service.
postBulkGet
(postBulkGetParams)
   .
then
(
response
 =>
 {
    
console
.
log
(response.
result
);
   });
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/v5/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
See an example of a JSON object that uses 
POST
 to the 
_bulk_get
 endpoint:
{
 
"docs"
:
 
[
   
{
    
"id"
:
 
"doc1"
   
}
,
   
{
    
"id"
:
 
"doc3"
   
}
 
]
}
Cloudant
   
212See an example JSON structure that is returned after bulk get:
{
                                                         
 
"results"
:
 
[
                                                         
   
{
                                                         
    
"id"
:
 
"doc01"
,
    
"docs"
:
 
[
     
{
      
"ok"
:
 
{
       
"_id"
:
 
"doc01"
,
       
"_rev"
:
 
"1-f3751e2db1d92e13b0baa6bdeb874c8c"
,
       
"simplekey"
:
 
"somedata"
      
}
     
}
     
]
   
}
,
   
{
    
"id"
:
 
"doc03"
,
    
"docs"
:
 
[
     
{
      
"ok"
:
 
{
       
"_id"
:
 
"doc03"
,
       
"_rev"
:
 
"2-d4fc04ef748edf305a8c0ed347f269c4"
,
       
"simplekey"
:
 
"somemoredata"
      
}
     
}
    
]
   
}
 
]
}
How design documents work
IBM® Cloudant® for IBM Cloud® reads specific fields and values of design documents as functions. Design documents are used to 
build indexes
 and
validate updates
.
Each design document defines either 
partitioned
 or 
global
 indexes, which are controlled by the 
options.partitioned
 field. A 
partitioned
 index
allows only queries over a single data partition in a partitioned 
database. A 
global
 index allows querying over all data within a database, at a cost of
latency and throughput over a partitioned index.
Creating or updating a design document
Method
PUT /$DATABASE/_design/$DDOC
Request
JSON of the design document information.
Response
JSON status.
Roles permitted
_admin
To create a design document, upload it to the specified database.
In these examples, 
$VARIABLES
 might refer to standard or design documents. To distinguish between them, standard documents have an 
_id
indicated by 
$DOCUMENT_ID
, while design documents have an 
_id
 indicated 
by 
$DDOC
.
A design document's ID never includes a partition key regardless of the database's partitioning type. The partition key isn't included because the
indexes that are included within a design document apply to all partitions in a partitioned database.
 Note: 
If a design document is updated, IBM Cloudant deletes the indexes from the previous version, and re-creates the index from scratch. If
Cloudant
   
213A design document's structure includes the following parts:
_id
Design document ID. This ID is 
always
 prefixed 
_design
 and 
never
 includes a partition key, regardless of database partitioning type.
_rev
Design document revision.
Options
Contains options for this design document.
$ 
Partitioned (optional, boolean)
:  Determines whether this design document describes partitioned or global indexes. For more information, see [The
 
`options.partitioned` field](#the-options-partitioned-field).
Views (optional)
An object that describes MapReduce views.
$ 
  `Viewname`
 :  (One for each view) - View Definition.
      Map
        :  Map Function for the view.
Reduce (optional)
Reduce Function for the view.
Indexes (optional)
An object that describes search indexes.
Index name
(One for each index) - Index definition.
Analyzer
Object that describes the analyzer to be used or an object with the following fields:
Name
Name of the analyzer. Valid values are 
standard
, 
email
, 
keyword
, 
simple
, 
whitespace
, 
classic
, and 
perfield
.
Stopwords (optional)
An array of stop words. Stop words are words that must not be indexed. If this array is specified, it overrides the default list of stop words.
The default list of stop words depends on the analyzer. The standard analyzer includes the 
following list of stop words: 
a
, 
an
, 
and
,
are
, 
as
, 
at
, 
be
, 
but
, 
by
, 
for
, 
if
, 
in
, 
into
, 
is
, 
it
, 
no
, 
not
, 
of
, 
on
, 
or
, 
such
, 
that
, 
the
, 
their
, 
then
,
there
, 
these
, 
they
, 
this
, 
to
, 
was
, 
will
, and 
with
.
Default (for the per field analyzer)
Default language to use if no language is specified for the field.
you need to change a design document for a larger database, have a look at the 
Design document management guide
.
Cloudant
   
214Fields (for the per field analyzer)
An object that specifies which language to use to analyze each field of the index. Field names in the object correspond to field
names in the index, that is, the first parameter of the index function. The values of the fields are the 
languages to be used, for
example 
english
.
Index
Function that handles the indexing.
Filters (optional, disallowed when 
partitioned
 is 
true
)
Filter functions.
Function name (one for each function)
Function definition.
Validate_doc_update (optional, disallowed when 
partitioned
 is 
true
)
Update validation function.
The 
options.partitioned
 field
This field sets whether the created index is a partitioned or global index.
This field includes the following values:
Table 1. Values for the options.partitioned field
Value
Description
Notes
true
Create the index as partitioned.
Can be used only in a partitioned database.
false
Create the index as global.
Can be used in any database.
The default follows the 
partitioned
 setting for the database:
Table 2. Partition settings
Database is partitioned?
Default 
partitioned
 value
Allowed values
Yes
true
true
, 
false
No
false
false
Copying a design document
You can copy the latest version of a design document to a new document by specifying the base document and target document. The copy is
requested by using the 
COPY
 request method.
The following example requests that IBM Cloudant copy the design document 
allusers
 to the new design document 
copyOfAllusers
, and
produces a response that includes the ID and revision of the new document.
 Tip: 
COPY
 is a nonstandard HTTP command.
Cloudant
   
215See the following example command to copy a design document by using HTTP:
COPY
 
$SERVICE_URL/$DATABASE/_design/$DDOC
 
HTTP/1.1
Content-Type
: 
application/json
Destination
: 
_design/$COPY_OF_DDOC
See the following example command to copy a design document:
$ 
curl 
"
$SERVICE_URL
/users/_design/allusers"
 \
 -X COPY \
 -H 
"Content-Type: application/json"
 \
 -H 
"Destination: _design/copyOfAllusers"
See the following example response to the copy request:
{
  
"ok"
:
 
true
,
  
"id"
:
 
"_design/copyOfAllusers"
,
  
"rev"
:
 
"1-9c65296036141e575d32ba9c034dd3ee"
}
The structure of the copy command
Method
COPY /$DATABASE/_design/$DDOC
Request
None.
Response
JSON describing the new document and revision.
Roles permitted
_design
Query Arguments
Argument
rev
Description
Revision to copy from.
Optional
Yes.
Type
String.
 Note: 
Copying a design document doesn't automatically reconstruct the view indexes. Like other views, these views are re-created the first
time that you access the new view.
 Note: 
The IBM Cloudant SDKs currently do not support the HTTP COPY method.
Cloudant
   
216HTTP Headers
Header
Destination
Description
Destination document (and optional revision)
Optional
No.
The source design document is specified on the request line, while the 
Destination
 HTTP Header of the request specifies the target document.
Copying from a specific revision
To copy from a specific version, add the 
rev
 argument to the query string.
The new design document is created by using the specified revision of the source document.
See the following example command to copy a specific revision of the design document by using HTTP:
COPY
 
$SERVICE_URL/$DATABASE/_design/$DDOC?rev=$REV
 
HTTP/1.1
Content-Type
: 
application/json
Destination
: 
_design/$COPY_OF_DDOC
See the following example command to copy a specific revision of the design document by using the command line:
curl 
"
$SERVICE_URL
/users/_design/allusers?rev=1-e23b9e942c19e9fb10ff1fde2e50e0f5"
 \
 -X COPY \
 -H 
"Content-Type: application/json"
 \
 -H 
"Destination: _design/copyOfAllusers"
Copying to an existing design document
To overwrite or copy to an existing document, specify the current revision string for the target document by using the 
rev
 parameter to the
Destination
 HTTP Header string.
See the following example command to overwrite an existing copy of the design document by using HTTP:
COPY $SERVICE_URL/$DATABASE/_design/$DDOC
Content-Type
: 
application/json
Destination
: 
_design/$COPY_OF_DDOC?rev=$REV
See the following example command to overwrite an existing copy of the design document by using the command line:
curl 
"
$SERVICE_URL
/users/_design/allusers"
 \
 -X COPY \
 -H 
"Content-Type: application/json"
 \
 -H 
"Destination: _design/copyOfAllusers?rev=1-9c65296036141e575d32ba9c034dd3ee"
The return value is the ID and new revision of the copied document.
See the following example response to overwrite an existing copy of the design document:
{
  
"id"
 
:
 
"_design/copyOfAllusers"
,
  
"rev"
 
:
 
"2-55b6a1b251902a2c249b667dab1c6692"
}
Cloudant
   
217Deleting a design document
You can delete an existing design document. Deleting a design document also deletes all of the associated view indexes, and recovers the
corresponding space on disk for the indexes in question.
To delete a design document successfully, you must specify the current revision of the design document by using the 
rev
 query argument.
See the following example command to delete a design document by using HTTP:
DELETE
 
$SERVICE_URL/$DATABASE/_design/$DDOC?rev=$REV
 
HTTP/1.1
See the following examples to delete a design document:
Curl
curl 
"
$SERVICE_URL
/users/_design/allusers?rev=2-21314508552eceb0e3012429d04575da"
 -X DELETE
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_design_document(
  db=
'users'
,
  ddoc=
'allusers'
,
  rev=
'2-21314508552eceb0e3012429d04575da'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DeleteDesignDocumentOptions;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteDesignDocumentOptions
 
designDocumentOptions
 
=
    
new
 
DeleteDesignDocumentOptions
.Builder()
        .db(
"users"
)
        .ddoc(
"allusers"
)
        .rev(
"2-21314508552eceb0e3012429d04575da"
)
        .build();
DocumentResult
 
response
 
=
    service.deleteDesignDocument(designDocumentOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.deleteDesignDocument({
  db: 'users',
  ddoc: 'allusers',
  rev: '2-21314508552eceb0e3012429d04575da'
}).then(response => {
  console.log(response.result);
});
Go
Cloudant
   
218deleteDesignDocumentOptions := service.NewDeleteDesignDocumentOptions(
  
"users"
,
  
"allusers"
,
)
deleteDesignDocumentOptions.SetRev(
"2-21314508552eceb0e3012429d04575da"
)
documentResult, response, err := service.DeleteDesignDocument(deleteDesignDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
"encoding/json"
"fmt"
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example response that includes the deleted document ID and revision:
{
  
"id"
:
 
"_design/allusers"
,
  
"ok"
:
 
true
,
  
"rev"
:
 
"3-7a05370bff53186cb5d403f861aca154"
}
The structure of the delete command
Method
DELETE /db/_design/$DDOC
Request
None.
Response
JSON of deleted design document.
Roles permitted
_design
Query Arguments
Argument
rev
Description
Current revision of the document for validation.
Optional
Yes, if 
If-Match
 header exists.
Type
String.
Cloudant
   
219HTTP Headers
Header
If-Match
Description
Current revision of the document for validation.
Optional
Yes, if 
rev
 query argument exists.
Views
An important use of design documents is for creating views. For more information about creating views, see 
Views (MapReduce)
.
Indexes
All queries operate on pre-defined indexes that are defined in design documents. These indexes are defined in the following list:
Search
MapReduce
For example, to create a design document that is used for searching, you must ensure that two conditions are true:
a
. 
You defined the document as a design document when you started the 
_id
 with 
_design/
.
b
. 
You created a 
search index
 within the document where you 
updated
 the document with the appropriate field or 
created
 a new document that
includes the search index.
As soon as the search index design document exists and the index is built, you can make queries by using it.
General notes on functions in design documents
Functions in design documents are run on multiple nodes for each document, and might be run several times. To avoid inconsistencies, they need to
be 
idempotent
, meaning they need to behave identically when run multiple times or on different nodes. In particular, you must not use functions
that generate random numbers or return the current time.
Filter functions
Filter functions are design documents that filter the 
changes feed
. They work by applying tests to each of the objects included in the changes feed.
If any of the function tests fail, the object is "removed" or "filtered" from the feed. If the function returns a 
true
 result when applied to a change, the
change remains in the feed. In other words, filter functions 
"remove" or "ignore" changes that you don't want to monitor.
Filter functions require two arguments: 
doc
 and 
req
.
The 
doc
 argument represents the document that is tested for filtering.
The 
req
 argument includes more information about the request. With this argument, you can create filter functions that are more dynamic because
they're based on multiple factors such as query parameters or the user context.
 Tip: 
Design documents with 
options.partitioned
 set to 
true
 can't contain a 
filters
 field.
 Tip: 
Filter functions can also be used to modify a 
replication task
.
Cloudant
   
220For example, you could control aspects of the filter function tests by using dynamic values that are provided as part of the HTTP request. However, in
many filter function use cases, only the 
doc
 parameter is used.
See the following example design document that includes a filter function:
{
 
"_id"
:
"_design/example_design_doc"
,
 
"filters"
:
 
{
  
"example_filter"
:
 
"function (doc, req) { ... }"
 
}
}
See the following example of a filter function:
function(doc, req){
 // we need only `mail` documents
 if (doc.type != 'mail'){
  return false;
 }
 // we're interested only in `new` ones
 if (doc.status != 'new'){
  return false;
 }
 return true; // passed!
}
Changes feed filter functions
To apply a filter function to the changes feed, include the 
filter
 parameter in the 
_changes
 query, providing the name of the filter to use.
See the following example of a filter function that is applied to a 
_changes
 query by using HTTP:
POST
 
$SERVICE_URL/$DATABASE/_changes?filter=$DDOC/$FILTER_FUNCTION
 
HTTP/1.1
See the following examples of a filter function applied to a 
_changes
 query:
Curl
curl -X POST 
"
$SERVICE_URL
/orders/_changes?filter=example_design_doc/example_filter"
 -H 
"Content-Type: application/json"
 -d
 
'{}'
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'orders'
,
  
filter
=
'example_design_doc/example_filter'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"orders"
)
    .filter(
"example_design_doc/example_filter"
)
    .build();
Cloudant
   
221ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.postChanges({
  db: 'orders',
  filter: 'example_design_doc/example_filter'
}).then(response => {
  console.log(response.result);
});
Go
postChangesOptions := service.NewPostChangesOptions(
  
"$DATABASE"
,
)
postChangesOptions.SetFilter(
"example_design_doc/example_filter"
)
changesResult, response, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
"encoding/json"
"fmt"
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
Filter function 
req
 argument
The 
req
 argument gives you access to aspects of the HTTP request by using the 
query
 property.
See the following example of supplying a 
req
 argument by using HTTP:
GET
 
$SERVICE_URL/$DATABASE/_changes?filter=$DDOC/$FILTER_FUNCTION&status=new
 
HTTP/1.1
See the following example of supplying a 
req
 argument:
Curl
curl 
"
$SERVICE_URL
/
$DATABASE
/_changes?filter=
$DDOC
/
$FILTER_FUNCTION
&status=new"
See the following example filter by using a supplied 
req
 argument:
function(doc, req){
 // we need only `mail` documents
 if (doc.type != 'mail'){
  return false;
 Important: 
The IBM Cloudant SDKs currently do not support 
status
 option for 
_changes
 request.
Cloudant
   
222 }
 // we're interested only in `new` ones
 if (doc.status != req.query.status){
  return false;
 }
 return true; // passed!
}
Predefined filter functions
A number of predefined filter functions are available:
_design
Accepts only changes to design documents.
_doc_ids
Accepts only changes for documents whose ID is specified in the 
doc_ids
 parameter or supplied JSON document.
_selector
Accepts only changes for documents that match a specified selector that is defined by using the same 
selector syntax
 as described in the
Request section, which is 
used for 
_find
.
_view
With this function, you can use an existing 
map function
 as the filter.
The 
_design
 filter
The 
_design
 filter accepts changes only for design documents within the requested database.
The filter doesn't require any arguments.
Changes are listed for 
all
 the design documents within the database.
See the following example application of the 
_design
 filter by using HTTP:
POST
 
/$DATABASE/_changes?filter=_design
 
HTTP/1.1
See the following example applications of the 
_design
 filter:
Curl
curl -X POST 
"
$SERVICE_URL
/orders/_changes?filter=_design"
 -H 
"Content-Type: application/json"
 -d 
'{}'
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'orders'
,
  
filter
=
'_design'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Cloudant
   
223PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"orders"
)
    .filter(
"_design"
)
    .build();
ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.postChanges({
  db: 'orders',
  filter: '_design'
}).then(response => {
  console.log(response.result);
});
Go
postChangesOptions := service.NewPostChangesOptions(
  
"$DATABASE"
,
)
postChangesOptions.SetFilter(
"_design"
)
changesResult, response, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
"encoding/json"
"fmt"
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example response (abbreviated) after you apply the 
_design
 filter:
{
  ...
  
"results"
:
[
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"10-304...4b2"
        
}
      
]
,
      
"id"
:
"_design/ingredients"
,
      
"seq"
:
"8-g1A...gEo"
    
}
,
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"123-6f7...817"
        
}
Cloudant
   
224      
]
,
      
"deleted"
:
true
,
      
"id"
:
"_design/cookbook"
,
      
"seq"
:
"9-g1A...4BL"
    
}
,
    ...
  
]
}
The 
_doc_ids
 filter
The 
_doc-ids
 filter accepts only changes for documents with specified IDs. The IDs are specified in a 
doc_ids
 parameter, or within a JSON
document supplied as part of the original request.
See the following example application of the 
_doc_ids
 filter by using HTTP:
POST
 
$SERVICE_URL/$DATABASE/_changes?filter=_doc_ids
 
HTTP/1.1
See the following example applications of the 
_doc_ids
 filter:
Curl
curl -X POST 
"
$SERVICE_URL
/orders/_changes?filter=_doc_ids"
 -H 
"Content-Type: application/json"
 -d 
'{"doc_ids":
 
["ExampleID"]}'
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'orders'
,
  
filter
=
'_doc_ids'
,
  doc_ids=[
'ExampleID'
]
).get_result()
print
(response)
Java
import
 java.util.Arrays;
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"orders"
)
    .filter(
"_doc_ids"
)
    .docIds(Arrays.asList(
"ExampleID"
))
    .build();
ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.postChanges({
Cloudant
   
225  db: 'orders',
  filter: '_doc_ids',
  docIds: ['ExampleID']
}).then(response => {
  console.log(response.result);
});
Go
postChangesOptions := service.NewPostChangesOptions(
  
"$DATABASE"
,
)
postChangesOptions.SetFilter(
"_doc_ids"
)
postChangesOptions.SetDocIds([]
string
{
"ExampleID"
})
changesResult, response, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
"encoding/json"
"fmt"
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example JSON document that lists document IDs to match during filtering:
{
  
"doc_ids"
:
 
[
    
"ExampleID"
  
]
}
See the following example response (abbreviated) after you filter by 
_docs_ids
:
{
  
"last_seq"
:
"5-g1A...o5i"
,
  
"pending"
:
0
,
  
"results"
:
[
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"13-bcb...29e"
        
}
      
]
,
      
"id"
:
"ExampleID"
,
      
"seq"
:
"5-g1A...HaA"
    
}
  
]
}
The 
_selector
 filter
The 
_selector
 filter accepts only changes for documents that match a specified selector, which is defined by using the same 
selector syntax
 that is
used for 
_find
.
For more examples that show use of this filter, see the information on 
selector syntax
.
See the following example application of the 
_selector
 filter by using HTTP:
Cloudant
   
226POST
 
$SERVICE_URL/$DATABASE/_changes?filter=_selector
 
HTTP/1.1
See the following example applications of the 
_selector
 filter:
Curl
curl -X POST 
"
$SERVICE_URL
/orders/_changes?filter=_selector"
 -H 
"Content-Type: application/json"
 -d 
'{"selector": {"_id": {
 
"$regex": "^_design/"}}}'
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'orders'
,
  
filter
=
'_selector'
,
  selector={
'_id'
: { 
'$regex'
: 
'^_design/'
}}
).get_result()
print
(response)
Java
import
 java.util.HashMap;
import
 java.util.Map;
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = 
new
 
HashMap
<String, Object>();
selector.put(
"_id"
, 
new
 
HashMap
<>().put(
"$regex"
, 
"^_design/"
));
PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"orders"
)
    .filter(
"_selector"
)
    .selector(selector)
    .build();
ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.postChanges({
    db: 'animaldb',
    filter: '_selector',
    selector: {"_id": { "$regex": "^_design/"}},
  }).then(response => {
    console.log(response.result);
  });
Go
postChangesOptions := service.NewPostChangesOptions(
  
"$DATABASE"
,
Cloudant
   
227)
postChangesOptions.SetFilter(
"_selector"
)
postChangesOptions.SetSelector(
map
[
string
]
interface
{}{
  
"_id"
: 
map
[
string
]
string
{ 
"$regex"
: 
"^_design/"
}})
changesResult, response, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
"encoding/json"
"fmt"
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example JSON document that includes the selector expression to use during filtering:
{
  
"selector"
:
{
    
"_id"
:
{
      
"$regex"
:
"^_design/"
    
}
  
}
}
See the following example response (abbreviated) after you filter by using a selector:
{
  
"last_seq"
:
"11-g1A...OaA"
,
  
"pending"
:
0
,
  
"results"
:
[
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"10-304...4b2"
        
}
      
]
,
      
"id"
:
"_design/ingredients"
,
      
"seq"
:
"8-g1A...gEo"
    
}
,
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"123-6f7...817"
        
}
      
]
,
      
"deleted"
:
true
,
      
"id"
:
"_design/cookbook"
,
      
"seq"
:
"9-g1A...4BL"
    
}
,
    
{
      
"changes"
:
[
        
{
          
"rev"
:
"6-5b8...8f3"
        
}
      
]
,
      
"deleted"
:
true
,
      
"id"
:
"_design/meta"
,
      
"seq"
:
"11-g1A...Hbg"
    
}
  
]
Cloudant
   
228}
The 
_view
 filter
Using the 
_view
 filter, you can use an existing 
map function
 as the filter.
The map function might emit output as the result of processing a specific document. When this situation occurs, the filter considers the document
that is allowed and includes it in the list of documents that you changed.
See the following example application of the 
_view
 filter by using HTTP:
POST
 
$SERVICE_URL/$DATABASE/_changes?filter=_view&view=$DDOC/$VIEW_NAME
 
HTTP/1.1
See the following example applications of the 
_view
 filter:
Curl
curl -X POST 
"
$SERVICE_URL
/animaldb/_changes?filter=_view&view=views101/latin_name"
 -H 
"Content-Type: application/json"
 -d
 
'{}'
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_changes(
  db=
'animaldb'
,
  
filter
=
'_view'
,
  view=
'views101/latin_name'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ChangesResult;
import
 com.ibm.cloud.cloudant.v1.model.PostChangesOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostChangesOptions
 
changesOptions
 
=
 
new
 
PostChangesOptions
.Builder()
    .db(
"animaldb"
)
    .filter(
"_vew"
)
    .view(
"views101/latin_name"
)
    .build();
ChangesResult
 
response
 
=
    service.postChanges(changesOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.postChanges({
  db: 'animaldb',
  filter: '_view',
  view: 'views101/latin_name'
}).then(response => {
  console.log(response.result);
});
Cloudant
   
229Go
postChangesOptions := service.NewPostChangesOptions(
  
"animaldb"
,
)
postChangesOptions.SetFilter(
"_view"
)
postChangesOptions.SetView(
"views101/latin_name"
)
changesResult, _, err := service.PostChanges(postChangesOptions)
if
 err != 
nil
 {
fmt.Println(err)
}
b, _ := json.MarshalIndent(changesResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
See the following example response (abbreviated) after you filter by using a map function:
{
  
"last_seq"
:
 
"5-g1A...o5i"
,
  
"results"
:
 
[
    
{
      
"changes"
:
 
[
        
{
          
"rev"
:
 
"13-bcb...29e"
        
}
      
]
,
      
"id"
:
 
"ExampleID"
,
      
"seq"
:
  
"5-g1A...HaA"
    
}
  
]
}
Update validators
Update validators determine whether a document must be written to disk when insertions and updates are attempted. They don't require a query
because they implicitly run during this process. If a change is rejected, the update validator responds 
with a custom error.
Update validators require four arguments:
Table 3. Arguments for the update validator
Argument
Purpose
newDoc
The version of the document passed in the request.
oldDoc
The version of the document currently in the database, or 
null
 if none exists.
secObj
The 
security object
 for the database.
userCtx
Context regarding the currently authenticated user, such as 
name
 and 
roles
.
See the following example design document with an update validator:
{
 
"_id"
:
 
"_design/validator_example"
,
 
"validate_doc_update"
:
 
"function(newDoc, oldDoc, userCtx, secObj) { ... }"
}
 Tip: 
Design documents with 
options.partitioned
 set to 
true
 can't contain a 
validate_doc_update
 field.
 Tip: 
Update validators don't apply when a design document is updated by an admin user. This practice ensures that admins can never
accidentally lock themselves out.
Cloudant
   
230See the following example of an update validator:
function(newDoc, oldDoc, userCtx, secObj) {
 if (newDoc.address === undefined) {
  throw({forbidden: 'Document must have an address.'});
 }
}
See the following example response from an update validator:
{
 
"error"
:
 
"forbidden"
,
 
"reason"
:
 
"Document must have an address."
}
Retrieving information about a design document
Two endpoints provide you with more information about design documents: 
_info
 and 
_search_info
.
The 
_info
 endpoint
The 
_info
 endpoint returns information about a specific design document, including the view index, view index size, and status of the design
document and associated view index information.
Method
GET /db/_design/$DDOC/_info
Request
None
Response
JSON that contains the design document information.
Roles permitted
_reader
See the following example of retrieving information about the 
recipesdd
 design document from within the 
recipes
 database by using HTTP:
GET
 
/recipes/_design/recipesdd/_info
 
HTTP/1.1
See the following examples of retrieving information about the 
recipesdd
 design document from within the 
recipes
 database:
Curl
curl 
"
$SERVICE_URL
/recipes/_design/recipesdd/_info"
Go
getDesignDocumentInformationOptions := service.NewGetDesignDocumentInformationOptions(
  
"recipes"
,
  
"recipesdd"
,
)
designDocumentInformation, response, err := service.GetDesignDocumentInformation(getDesignDocumentInformationOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(designDocumentInformation, 
""
, 
"  "
)
fmt.Println(
string
(b))
Python
Cloudant
   
231from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_design_document_information(
  db=
'recipes'
,
  ddoc=
'recipesdd'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DesignDocumentInformation;
import
 com.ibm.cloud.cloudant.v1.model.GetDesignDocumentInformationOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetDesignDocumentInformationOptions
 
informationOptions
 
=
    
new
 
GetDesignDocumentInformationOptions
.Builder()
        .db(
"recipes"
)
        .ddoc(
"recipesdd"
)
        .build();
DesignDocumentInformation
 
response
 
=
    service.getDesignDocumentInformation(informationOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.getDesignDocumentInformation({
  db: 'recipes',
  ddoc: 'recipesdd'
}).then(response => {
  console.log(response.result);
});
The JSON response includes the following individual fields:
name
Name or ID of design document.
view_index
View Index
compact_running
Indicates whether a compaction routine runs on the view.
disk_size
Size in bytes of the view as stored on disk.
language
Language that is used for defining views.
purge_seq
The purge sequence that was processed.
signature
Cloudant
   
232MD5 signature of the views for the design document.
update_seq
The update sequence of the corresponding database that was indexed.
updater_running
Indicates whether the view is being updated.
waiting_clients
Number of clients that are waiting on views from this design document.
waiting_commit
Indicates whether the underlying database has outstanding commits that need to process.
See the following example response in JSON format:
{
 
"name"
 
:
 
"recipesdd"
,
 
"view_index"
:
 
{
  
"compact_running"
:
 
false
,
  
"updater_running"
:
 
false
,
  
"language"
:
 
"javascript"
,
  
"purge_seq"
:
 
10
,
  
"waiting_commit"
:
 
false
,
  
"waiting_clients"
:
 
0
,
  
"signature"
:
 
"fc65594ee76087a3b8c726caf5b40687"
,
  
"update_seq"
:
 
375031
,
  
"disk_size"
:
 
16491
 
}
}
The 
_search_info
 endpoint
The 
_search_info
 endpoint returns information about a specified search that is defined within a specific design document.
Method
GET /db/_design/$DDOC/_search_info/yourSearch
Request
None
Response
JSON that contains information about the specified search.
Roles permitted*
_reader
See the following example of getting information about the 
description
 search, which is defined within the 
app
 design document that is stored in
the 
foundbite
 database, by using HTTP:
GET
 
/foundbite/_design/app/_search_info/description
 
HTTP/1.1
See the following examples of getting information about the 
description
 search index, which is defined within the 
app
 design document that is
stored in the 
foundbite
 database:
Curl
curl 
"
$SERVICE_URL
/foundbite/_design/app/_search_info/description"
Python
Cloudant
   
233from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_search_info(
  db=
'foundbite'
,
  ddoc=
'app'
,
  index=
'description'
).get_result()
print
(response)
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.GetSearchInfoOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchInfoResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetSearchInfoOptions
 
infoOptions
 
=
    
new
 
GetSearchInfoOptions
.Builder()
        .db(
"foundbite"
)
        .ddoc(
"app"
)
        .index(
"description"
)
        .build();
SearchInfoResult
 
response
 
=
    service.getSearchInfo(infoOptions).execute()
        .getResult();
System.out.println(response);
Node
const { CloudantV1 } = require('@ibm-cloud/cloudant');
const service = CloudantV1.newInstance({});
service.getSearchInfo({
  db: 'foundbite',
  ddoc: 'app',
  index: 'description'
}).then(response => {
  console.log(response.result);
});
Go
getSearchInfoOptions := service.NewGetSearchInfoOptions(
  
"foundbite"
,
  
"app"
,
  
"description"
,
)
searchInfoResult, response, err := service.GetSearchInfo(getSearchInfoOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(searchInfoResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The JSON structure includes the following individual fields:
name
Name or ID of the Search within the design document.
Cloudant
   
234Name or ID of the Search within the design document.
search_index
The Search Index
pending_seq
The sequence number of changes in the database that reached the Lucene index, both in memory and on disk.
doc_del_count
Number of deleted documents in the index.
doc_count
Number of documents in the index.
disk_size
The size of the index on disk, in bytes.
committed_seq
The sequence number of changes in the database that were committed to the Lucene index on disk.
See the following example response in JSON format:
{
  
"name"
:
"_design/app/description"
,
  
"search_index"
:
{
    
"pending_seq"
:
63
,
    
"doc_del_count"
:
3
,
    
"doc_count"
:
10
,
    
"disk_size"
:
9244
,
    
"committed_seq"
:
63
  
}
}
Design document management
The scalable JSON data store for IBM Cloudant has several querying mechanisms, all of which generate indices that are created and maintained
separately from the core data.
Article contributed by Glynn Bird, Developer Advocate at IBM Cloudant, 
glynn@cloudant.com
.
Indexing isn't performed immediately when a document is saved. Instead, indexing is scheduled to happen later, providing a faster, non-blocking
write throughput.
MapReduce views are indexes into the data set with key value pairs that are stored in a BTree for efficient retrieval by key or range of keys.
Search Indexes are constructed by using Apache Lucene to allow free-text search, faceting, and complex ad hoc queries.
IBM® Cloudant® for IBM Cloud®'s 
search indexes
 and 
MapReduce views
 are configured by adding design documents to a 
database. Design
documents are JSON documents that include the instructions about how the view or index is to be built. Let's take a simple example. Assume that
you have a simple collection of data documents, similar to the following example.
See an example of a simple data document:
{
    
"_id"
:
 
"23966717-5A6F-E581-AF79-BB55D6BBB613"
,
    
"_rev"
:
 
"1-96daf2e7c7c0c277d0a63c49b57919bc"
,
    
"doc_name"
:
 
"Markdown Reference"
,
    
"body"
:
 
"Lorem Ipsum"
,
    
"ts"
:
 
1422358827
}
Each data document includes a name, a body, and a timestamp. You create a 
MapReduce view
 to sort your documents by timestamp.
You can sort your documents by timestamp by creating a Map function.
Cloudant
   
235See an example map function that returns a document's timestamp field, if present:
function
(
doc
) {
    
if
 (doc.
ts
) {
        
emit
( doc.
ts
, 
null
);
    }
}
The function emits the document's timestamp so that you can use it as the key to the index. Since we're not interested in the value in the index,
null
 is emitted. The effect is to provide a time-ordered index into the document set.
We're going to call this view 
by_ts
 and put it into a design document that is called 
fetch
.
See an example design document that defines a view by using a map function:
{
    
"_id"
:
 
"_design/fetch"
,
    
"views"
:
 
{
      
"by_ts"
:
 
{
        
"map"
:
 
"function(doc) {
          if (doc.ts) {
            emit( doc.ts, null);
          }
        }"
      
}
    
}
,
    
"language"
:
 
"javascript"
}
The result is that the map code is turned into a JSON-compatible string, and included in a design document.
Once the design document is saved, IBM Cloudant triggers server-side processes to build the 
fetch/by_ts
 view. It creates this view by iterating
over every document in the database, and sending each one to the JavaScript map function. 
The function returns the emitted 
key-value
 pair. As
the iteration continues, each 
key-value
 pair is stored in a B-Tree index. After the index is built for the first time, subsequent reindexing is
performed only against 
new and updated documents. Deleted documents are de-indexed. This time-saving process is known as incremental
MapReduce, as shown in the following diagram:
Figure 1. Illustration of Incremental MapReduce
It's worth remembering the following points:
The construction of an index happens asynchronously. IBM Cloudant confirms that the design document was saved. To check on the progress
of the construction of the index, you must poll IBM Cloudant's 
_active_tasks
 
endpoint.
The more data that you have, the longer it takes before the index is ready.
While the initial index build is in progress, any queries made against the index are blocked.
Querying a view triggers the 'mapping' of any documents that aren't incrementally indexed. This practice ensures that you get an up-to-date
view of the data. See the following 
stale
 parameter
 discussion 
for exceptions to this rule.
Multiple views in the same design document
If you define several views in the same design document, then they're built efficiently at the same time. Each document is read only once, and passed
Cloudant
   
236through each view's Map function. If you use this approach, keep in mind that modifying a design 
document invalidates all of the existing MapReduce
views that are defined in the document. This process invalidates MapReduce views even if some of the views stay unaltered.
If MapReduce views must be altered independently of each other, place their definitions in separate design documents.
Figure 2. Design document version change
Managing changes to a design document
Imagine at some point in the future you decide to change the design of the view. Now, instead of returning the actual timestamp result, we're only
interested in the count of how many documents match the criteria. To achieve this count, the map 
function stays the same, but you now use a
reduce
 of 
_count
.
See an example design document that uses a reduce function:
{
    
"_id"
:
 
"_design/fetch"
,
    
"_rev"
:
 
"2-a2324c9e74a76d2a16179c56f5315dba"
,
    
"views"
:
 
{
        
"by_ts"
:
 
{
            
"map"
:
 
"function(doc) {
                if (doc.ts) {
                  emit( doc.ts, null);
                }
            }
        }"
,
        
"reduce"
:
 
"_count"
    
}
,
    
"language"
:
 
"javascript"
}
When this design document is saved, IBM Cloudant completely invalidates the old index and begins building the new index from scratch, iterating
over every document in turn. As with the original build, the time that it takes depends on how many 
documents are in the database. The build also
blocks incoming queries on that view until it's complete.
But there's a problem...
If you have an application that is accessing this view in real time, then you might experience a deployment dilemma:
Version 1 of the code, which relied on the original design document, might no longer work because the old view is invalidated.
Version 2 of the code uses the new design document. This version can't be released immediately because the new view isn't finished building
yet. Remember the build process takes longer if the database includes many documents.
A more subtle problem that affects the code is that versions 1 and 2 expect different result data from the view: Version 1 expects a list of
 Note: 
This behavior doesn't apply to Lucene search indexes. They can be altered within the same design document without invalidating
other unchanged indexes in the same document.
Cloudant
   
237matching documents, while version 2 expects a 'reduced' count of results.
Coordinating changes to design documents
You can deal with this change control problem in two ways.
Versioned design documents
One solution is to use versioned design document names:
The code is initially written to use a view called 
_design/fetchv1
.
When you release a new version, you create a new view that is called 
_design/fetchv2
, and query the view to ensure that it builds.
IBM Cloudant polls 
_active_tasks
 until the work of building the new index is complete.
Now, you're ready to release the code that depends on the second view.
Delete 
_design/fetchv1
 when we're sure it's no longer needed.
Using versioned design documents is a simple way to manage change control in your design documents, but you must remember to remove the
older versions later.
Move and switch
 design documents
Another approach relies on the fact that IBM Cloudant recognizes when it has two identical design documents, and doesn't waste time and resources
to rebuild views that it already has. In other words, if you take your design document 
_design/fetch
 
and create an exact duplicate
_design/fetch_OLD
, then both endpoints would work interchangeably without triggering any reindexing.
To switch to the new view, follow these steps:
a
. 
Create a duplicate copy of the design document that you want to change, for example by adding 
_OLD
 to its name: 
_design/fetch_OLD
.
b
. 
Put the new or "incoming" design document into the database by using a name with the suffix 
_NEW
: 
_design/fetch_NEW
.
c
. 
Query the 
fetch_NEW
 view to ensure that it starts to build.
d
. 
Poll the 
_active_tasks
 endpoint and wait until the index is finished building.
e
. 
Put a duplicate copy of the new design document into 
_design/fetch
.
f
. 
Delete design document 
_design/fetch_NEW
.
g
. 
Delete design document 
_design/fetch_OLD
.
Move and switch
 tooling
The command-line, Node.js, 
couchmigrate
 script automates the 
Move and switch
 procedure. It can be installed by using the following
command:
npm install -g couchmigrate
To use the 
couchmigrate
 script, first define the URL of the CouchDB/IBM Cloudant instance by setting an environment variable called 
COUCH_URL
.
Run the following command to define the URL for the IBM Cloudant instance:
export
 COUCH_URL=https://127.0.0.1:5984
The URL must start with 
https://
 and can include authentication credentials. Run the following command to define the URL of the IBM Cloudant
instance with authentication credentials:
export
 COUCH_URL=
"https://
$ACCOUNT
:
$PASSWORD
@
$HOST
.cloudant.com"
If you assume that you have a design document in JSON format, which is stored in a file, you can then run the migrate command.
In this example, 
db
 specifies the name of the database to change, and 
dd
 specifies the path to the design document file. Run the 
couchmigrate
command:
$ 
couchmigrate --db mydb --dd /path/to/my/dd.json
The script coordinates the 
Move and switch
 procedure, waiting until the view is built before it returns. If the incoming design document is the same
as the incumbent one, then the script returns almost immediately.
Cloudant
   
238The source code for the script is available here: 
couchmigrate
.
The '
stale
' parameter
If an index is complete, but new records are added into the database, then the index is scheduled to be updated in the background. The state of the
database is shown in the following diagram:
Figure 3. Index scheduled for update
When querying the view, you have the following choices.
The default behavior is to ensure that the index is up to date, with the latest documents in the database, before it returns the answer. When
you query the view, IBM Cloudant first indexes the 250 new documents, and then returns the answer.
An alternative is adding the 
stale=ok
 parameter to the API call. This parameter means, 
return me the data that is already indexed.
I don't care about the latest updates.
 In other words, when you query the view with 
stale=ok
, IBM Cloudant returns the answer
immediately, without any additional reindexing.
A second alternative is to add the 
stale=update_after
 parameter to the API call. This parameter means, 
return me the data that is
already indexed, 
and then reindex any new documents.
 In other words, when you query 
the view with 
stale=update_after
, IBM
Cloudant returns the answer immediately, and then schedules a background task to index the new data.
Adding 
stale=ok
 or 
stale=update_after
 can be a good way of getting answers more quickly from a view, but at the expense of freshness.
The default behavior distributes load evenly across nodes in the IBM Cloudant cluster. If you use the alternative 
stale=ok
 or 
stale=update_after
options, these options might favor a subset of cluster nodes in order 
to return consistent results from across the eventually consistent set. The
stale
 parameter isn't a perfect solution for all use cases. However, it can provide timely responses on fast-changing data sets if your application is
happy to accept stale results. If your data's change rate is small, adding 
stale=ok
 or 
stale=update_after
 doesn't bring a performance benefit,
and might unevenly distribute the load on larger clusters.
Avoid 
stale=ok
 or 
stale=update_after
 whenever possible because the default behavior provides the freshest data, and distributes data within
the cluster. You can make a client app aware that a large data processing task 
is in progress (during a regular bulk data update, for example) by
switching to 
stale=ok
 temporarily during these times. The app can revert to the default behavior afterward.
Grouping related documents together in IBM Cloudant
Traditionally, e-commerce systems are built with relational databases. These databases typically use a number of tables joined to record sales,
customer details, purchased products, and delivery tracking information.
Relational databases offer high consistency, which means that application developers can build their applications to a database's strengths. This
practice includes joins between collections, enumerations to record the state of an object, and database 
transactions to guarantee atomic
operations.
IBM® Cloudant® for IBM Cloud® favors availability over consistency. It's a high-availability, fault-tolerant, distributed database that is eventually
consistent. A distributed database means the customer's shopping service is always available 
and scalable enough to cope with many users who
 Note: 
The 
stale
 option is still available, but the more useful options 
stable
 and 
update
 are available and must be used instead. For
more information, see 
Accessing a stale view
.
Cloudant
   
239make purchases at the same time. With that in mind, your application can leverage IBM Cloudant's strengths and not treat it like a relational
database.
This discussion outlines some of the factors that are involved in building an e-commerce system that takes advantage of IBM Cloudant's strengths.
IBM Cloudant uses concepts that are applicable to many other domains, such as:
Using multiple documents to represent the state of a purchase, rather than frequently updating a single document.
Storing copies of related objects in order instead of joining to another collection.
Creating views to collate documents by 
order_id
 to reflect the current state of a purchase.
For example, you might create a 
purchase
 document that includes details such as the items ordered, customer information, cost, and delivery
information.
See the following example document that describes a purchase:
{
    
"_id"
:
 
"023f7a21dbe8a4177a2816e4ad1ea27e"
,
    
"type"
:
 
"purchase"
,
    
"order_id"
:
 
"320afa89017426b994162ab004ce3383"
,
    
"basket"
:
 
[
        
{
            
"product_id"
:
 
"A56"
,
            
"title"
:
 
"Adele - 25"
,
            
"category"
:
 
"Audio CD"
,
            
"price"
:
 
8.33
,
            
"tax"
:
 
0.2
,
            
"quantity"
:
 
2
        
}
,
        
{
            
"product_id"
:
 
"B32"
,
            
"title"
:
 
"The Lady In The Van - Alan Bennett"
,
            
"category"
:
 
"Paperback book"
,
            
"price"
:
 
3.49
,
            
"tax"
:
 
0
,
            
"quantity"
:
 
2
        
}
    
]
,
    
"account_id"
:
 
"985522332"
,
    
"delivery"
:
 
{
        
"option"
:
 
"Next Day"
,
        
"price"
:
 
2.99
,
        
"address"
:
 
{
            
"street"
:
 
"17 Front Street"
,
            
"town"
:
 
"Middlemarch"
,
            
"postcode"
:
 
"W1A 1AA"
        
}
    
}
,
    
"pretax"
 
:
 
20.15
,
    
"tax"
 
:
 
3.32
,
    
"total"
:
 
26.46
}
This document provides enough data for a purchase record to render a summary of an order on a web page, or an email, without fetching more
records. Notice key details about the order. In particular, see the following details:
The basket contains reference IDs (
product_id
) to a database of products stored elsewhere.
The basket duplicates some of the product data in this record, enough to record the state of the items purchased at the point of sale.
The document doesn't contain fields that mark the status of the order. More documents would be added later to record payments and delivery.
The database automatically generates a document 
_id
 when it inserts the document into the database.
A unique identifier (
order_id
) is supplied with each purchase record to reference the order later.
When the customer places an order, typically at the point when they enter the check out phase on the website, a purchase order record is created
similar to the previous example.
Generating your own unique identifiers (UUIDs)
In a relational database, sequential "auto incrementing" numbers are often used. While in distributed databases, data is spread around a cluster of
Cloudant
   
240servers, and longer UUIDs are used to ensure that documents are stored with their unique 
ID.
To create a unique identifier for use in your application, such as an 
order_id
, call the 
GET _uuids
 endpoint
 on the IBM Cloudant API. The
database 
generates an identifier for you. The same endpoint can be used to generate multiple IDs by adding a 
count
 parameter, for example,
/_uuids?count=10
.
Recording payments
When the customer successfully pays for their items, more records are added to the database to record the order.
Example of a payment record
{
    
"_id"
:
 
"bf70c30ea5d8c3cd088fef98ad678e9e"
,
    
"type"
:
 
"payment"
,
    
"account_id"
:
 
"985522332"
,
    
"order_id"
:
 
"320afa89017426b994162ab004ce3383"
,
    
"value"
:
 
6.46
,
    
"method"
:
 
"credit card"
,
    
"payment_reference"
:
 
"AB9977G244FF2F667"
}
...
{
    
"_id"
:
 
"12c0ea6cd3d2c6e3b1d34442aea6a2d9"
,
    
"type"
:
 
"payment"
,
    
"account_id"
:
 
"985522332"
,
    
"order_id"
:
 
"320afa89017426b994162ab004ce3383"
,
    
"value"
:
 
20.00
,
    
"method"
:
 
"voucher"
,
    
"payment_reference"
:
 
"Q88775662377224"
}
In the previous example, the customer paid by supplying a credit card and redeeming a pre-paid voucher. The total of the two payments added up to
the amount of the order. Each payment was written to IBM Cloudant as a separate document.
You could see the status of an order by creating a view of everything you know about an 
order_id
. The view would enable a ledger that contains the
following information:
Purchase totals as positive numbers.
Payments against the account as negative numbers.
A map function might be used to identify the required values.
Example map function to find purchase total and payment values
function
 (
doc
) {
    
if
 (doc.
type
 === 
'purchase'
) {
        
emit
(doc.
order_id
, doc.
total
);
    } 
else
 {
        
if
 (doc.
type
 === 
'payment'
) {
            
emit
(doc.
order_id
, -doc.
value
);
        }
    }
}
Use the built-in 
_sum
 reducer
 to produce output as a ledger of payment events.
Example of using the built-in 
_sum
 reducer, which is queried with 
?reduce=false
{
    
"total_rows"
:
3
,
"offset"
:
0
,
"rows"
:
[
        
{
            
"id"
:
"320afa89017426b994162ab004ce3383"
,
            
"key"
:
"985522332"
,
            
"value"
:
26.46
        
}
,
Cloudant
   
241        
{
            
"id"
:
"320afa89017426b994162ab004ce3383"
,
            
"key"
:
"985522332"
,
            
"value"
:
-20
        
}
,
        
{
            
"id"
:
"320afa89017426b994162ab004ce3383"
,
            
"key"
:
"985522332"
,
            
"value"
:
-6.46
        
}
    
]
}
Alternatively, you could produce totals that are grouped by 
order_id
.
Example of totals grouped by 
order_id
, with 
?group_level=1
{
    
"rows"
:
[
        
{
            
"key"
:
"320afa89017426b994162ab004ce3383"
,
            
"value"
:
0
        
}
    
]
}
Since the view in the previous example returns 0 for the order value, the result indicates that the order is fully paid. The reason is that the positive
purchase order total cancels the negative payment amounts. Recording events as separate 
documents, for example, one for the order and one for
each payment, is good practice in IBM Cloudant. This practice avoids the possibility of creating conflicts when multiple processes modify the same
document simultaneously.
Adding more documents
You might add other, separate documents to the database to record the following state changes as the order is provisioned and dispatched:
Dispatch notifications
Delivery receipts
Refund records
As the data arrives, IBM Cloudant writes to each document separately. Therefore, it's not necessary to modify the core purchase document.
Advantages of storing purchase orders in IBM Cloudant
Using IBM Cloudant to store purchase order information allows an ordering system to be highly available and scalable. With an ordering system like
this one, you can deal with large volumes of data and high rates of concurrent access. By modeling 
the data in separate documents that are only
written once, you can ensure that documents never become conflicted, such as during concurrent access to the same document by separate
processes.
Furthermore, documents can contain copies of data that exists in other collections to represent - rather than rely on - joining data with a foreign key.
For example, IBM Cloudant records the state of a basket at the time of purchase. This record 
allows an order's state to be fetched by a single call to
an IBM Cloudant view that groups documents related by 
order_id
.
How to use attachments
Another way to store data is to use attachments. Attachments are Binary Large OBject (
BLOB
) files that are included within documents.
The BLOB is stored in the 
_attachments
 component of the document. The BLOB holds data that includes the following information:
The attachment name
The type of the attachment
The actual content
 Important: 
It's a good idea to keep attachments small in size and number because attachments can impact performance.
Cloudant
   
242Examples of BLOBs would be images and multimedia.
The content type corresponds to a 
MIME type
. For example, if you want to attach a 
.jpg
 image file to a document, 
you specify the attachment
MIME type as 
image/jpeg
.
Create or update
To create a new attachment at the same time as creating a new document, include the attachment as an 
inline
 component of the JSON content.
To create a new attachment on an existing document, or to update an attachment on a document, make a PUT request with the document's most
recent 
_rev
 to 
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
. 
The attachment's 
content type
 must be specified by
using the 
Content-Type
 header. The 
$ATTACHMENT
 
value is the name by which the attachment is associated with the document.
See the following example for creating or updating an attachment by using HTTP:
PUT
 
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT?rev=$REV
 
HTTP/1.1
Content-Type
: 
$$ATTACHMENT_MIME_TYPE
See the following example for creating or updating an attachment:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X PUT 
"
$SERVICE_URL
/products/small-appliances:100001/product_details.txt"
 
-H 
"Content-Type: text/plain"
 --data 
'This appliance includes...'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PutAttachmentOptions;
import
 java.io.ByteArrayInputStream;
import
 java.io.InputStream;
import
 java.nio.charset.StandardCharsets;
Cloudant
 
service
 
=
 Cloudant.newInstance();
String
 
detailedDescription
 
=
 
"This appliance includes..."
;
InputStream
 
detailedDescriptionStream
 
=
    
new
 
ByteArrayInputStream
(detailedDescription
        .getBytes(StandardCharsets.UTF_8));
PutAttachmentOptions
 
attachmentOptions
 
=
    
new
 
PutAttachmentOptions
.Builder()
        .db(
"products"
)
        .docId(
"small-appliances:100001"
)
        .attachmentName(
"product_details.txt"
)
        .attachment(detailedDescriptionStream)
        .contentType(
"text/plain"
)
        .build();
DocumentResult
 
response
 
=
    service.putAttachment(attachmentOptions).execute()
        .getResult();
System.out.println(response);
 Note: 
If you include the attachment as an 
inline
 component of the overall JSON, the attachment content is represented by using BASE64
form.
 Important: 
Attachments aren't permitted on documents in 
_replicator
 or 
_users
 
databases.
 Tip: 
You can create more than one attachment for a document by ensuring that the 
$ATTACHMENT
 value for each attachment is unique within
the document.
Cloudant
   
243Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 stream = 
new
 
Readable
();
stream.
push
(
'This appliance includes...'
);
stream.
push
(
null
);
service.
putAttachment
({
  
db
: 
'products'
,
  
docId
: 
'small-appliances:100001'
,
  
attachmentName
: 
'product_details.txt'
,
  
attachment
: stream,
  
contentType
: 
'text/plain'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
detailed_description = 
"This appliance includes..."
response = service.put_attachment(
  db=
'products'
,
  doc_id=
'small-appliances:100001'
,
  attachment_name=
'product_details.txt'
,
  attachment=detailed_description,
  content_type=
'text/plain'
).get_result()
print
(response)
Go
putAttachmentOptions := service.NewPutAttachmentOptions(
  
"products"
,
  
"small-appliances:100001"
,
  
"product_details.txt"
,
  ioutil.NopCloser(
    bytes.NewReader([]
byte
(
"This appliance includes..."
)),
  ),
  
"text/plain"
,
)
documentResult, response, err := service.PutAttachment(putAttachmentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"io/ioutil"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
Cloudant
   
244All Go examples require the 
service
 object to be initialized. For more information, see the API documentation 
Authentication section
 
for
examples.
The response includes the document ID and the new document revision.
See the following example response with the document ID and new revision:
{
 
"id"
 
:
 
"FishStew"
,
 
"ok"
 
:
 
true
,
 
"rev"
 
:
 
"9-247bb19a41bfd9bfdaf5ee6e2e05be74"
}
Read
To retrieve an attachment, make a 
GET
 request to 
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
. The body of the
response is the raw content of the attachment.
See the following example of reading an attachment by using HTTP:
GET
 
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
 
HTTP/1.1
See the following example of reading an attachment:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/products/small-appliances:100001/product_details.txt"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.GetAttachmentOptions;
import
 java.io.BufferedReader;
import
 java.io.InputStream;
import
 java.io.InputStreamReader;
import
 java.util.stream.Collectors;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetAttachmentOptions
 
attachmentOptions
 
=
    
new
 
GetAttachmentOptions
.Builder()
        .db(
"products"
)
        .docId(
"small-appliances:100001"
)
        .attachmentName(
"product_details.txt"
)
        .build();
InputStream
 
streamResult
 
=
    service.getAttachment(attachmentOptions).execute()
        .getResult();
String
 
response
 
=
    
new
 
BufferedReader
(
new
 
InputStreamReader
(streamResult))
        .lines().collect(Collectors.joining(
"\n"
));
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
 Tip: 
Attachments don't have their own revisions. Instead, when you update or create an attachment, the revision of the document it's
attached to changes.
Cloudant
   
245service.
getAttachment
({
  
db
: 
'products'
,
  
docId
: 
'small-appliances:100001'
,
  
attachmentName
: 
'product_details.txt'
}).
then
(
response
 =>
 {
  
let
 attachment = response.
result
 
as
 
Readable
;
  attachment.
pipe
(process.
stdout
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response_attachment = service.get_attachment(
  db=
'products'
,
  doc_id=
'small-appliances:100001'
,
  attachment_name=
'product_details.txt'
).get_result().content
print
(response_attachment)
Go
getAttachmentOptions := service.NewGetAttachmentOptions(
  
"products"
,
  
"small-appliances:100001"
,
  
"product_details.txt"
,
)
result, response, err := service.GetAttachment(getAttachmentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
data, _ := ioutil.ReadAll(result)
fmt.Println(
"\n"
, 
string
(data))
The previous Go example requires the following import block:
Go
import
 (
   
"fmt"
   
"io/ioutil"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Delete an attachment
To delete an attachment, make a 
DELETE
 request with the document's most recent 
_rev
 to
https://$ACCOUNT.cloudant.com/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
. If you don't supply the most recent 
_rev
, 
the response is a 
409
error
.
See the following example of deleting an attachment by using HTTP:
DELETE
 
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT?rev=$REV
 
HTTP/1.1
See the following example of deleting an attachment:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X DELETE 
"
$SERVICE_URL
/products/small-
Cloudant
   
246appliances:100001/product_details.txt?rev=4-1a0d1cd6f40472509e9aac646183736a"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DeleteAttachmentOptions;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteAttachmentOptions
 
attachmentOptions
 
=
    
new
 
DeleteAttachmentOptions
.Builder()
        .db(
"products"
)
        .docId(
"small-appliances:100001"
)
        .attachmentName(
"product_details.txt"
)
        .rev(
"4-1a0d1cd6f40472509e9aac646183736a"
)
        .build();
DocumentResult
 
response
 
=
    service.deleteAttachment(attachmentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
deleteAttachment
({
  
db
: 
'products'
,
  
docId
: 
'small-appliances:100001'
,
  
attachmentName
: 
'product_details.txt'
,
  
rev
: 
'4-1a0d1cd6f40472509e9aac646183736a'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_attachment(
  db=
'products'
,
  doc_id=
'small-appliances:100001'
,
  attachment_name=
'product_details.txt'
,
  rev=
'4-1a0d1cd6f40472509e9aac646183736a'
).get_result()
print
(response)
Go
deleteAttachmentOptions := service.NewDeleteAttachmentOptions(
  
"products"
,
  
"small-appliances:100001"
,
  
"product_details.txt"
,
)
deleteAttachmentOptions.SetRev(
"4-1a0d1cd6f40472509e9aac646183736a"
)
documentResult, response, err := service.DeleteAttachment(deleteAttachmentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
Cloudant
   
247b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
If the deletion is successful, the response includes 
"ok": true
, and the ID and new revision of the document.
See the following example response after a successful delete of an attachment:
{
 
"ok"
:
 
true
,
 
"id"
:
 
"DocID"
,
 
"rev"
:
 
"3-aedfb06537c1d77a087eb295571f7fc9"
}
Inline
Inline attachments are attachments that are included as part of the JSON content. The content must be provided by using 
BASE64
 representation,
as shown in the 
example.
A full list of media types is available in the 
media types
 article.
See the following example JSON document that includes an inline attachment of a jpeg image:
{
 
"_id"
:
"document_with_attachment"
,
 
"_attachments"
:
 
{
  
"name_of_attachment"
:
 
{
   
"content_type"
:
"image/jpeg"
,
   
"data"
:
 
"iVBORw0KGgoAA... ...AASUVORK5CYII="
  
}
 
}
}
Performance considerations
While document attachments are useful, they do have implications for application performance. In particular, having too many attachments can have
an adverse performance impact during replication.
For example, if your application requires storage for multiple images as attachments or includes large images, you must use an alternative 
BLOB
storage mechanism to store the images. You might then use IBM Cloudant to keep the image metadata, such as URLs to the BLOB store.
You might find it helpful to do performance testing for your specific application to determine which approach works best for your circumstances.
Cloudant
   
248Monitoring your instance
Monitoring an IBM Cloudant cluster
A key part of ensuring best performance, or troubleshooting any problems, is monitoring the affected system.
You want to be able to answer the question:
In what way has the system behavior changed as a result of any configuration or application modifications?
To answer the question, you need data. The data comes from monitoring the system. Monitoring the system while it replicates can be performed by
using the 
_active_tasks
 endpoint, which is described in more detail in the 
Active tasks
 
documentation.
For more detailed system information, use the cluster monitoring API.
Monitoring metrics overview
When you monitor the cluster, you can obtain data about how it is performing. Details such as the number of HTTP requests processed per second, or
how many documents are processed per second, can all be obtained through the monitoring API. The 
API can be invoked only by an administrative
user, and is applied to a specific monitoring endpoint.
For example, if you wanted to monitor the number of documents processed by a map function each second, you would direct the request to the
map_doc
 endpoint.
For more information, see a full list of the available 
endpoints
.
The data is returned in JSON format by default. You can specify a 
raw
 format if you prefer.
Syntax of the monitoring request
All requests to the monitoring API have the following form:
curl -u 
$ADMIN_USER
 
"https://
$ADMIN_USER
.cloudant.com/_api/v2/monitoring/
$END_POINT
?cluster=
$CLUSTER
[&format=(json|raw)]"
The fields are described in the following table:
Table 1. Monitoring API request fields
Field
Meaning
ADMIN_USER
The account name. The account must have administrative privileges.
CLUSTER
The cluster that you are interested in.
DURATION
Specifies the duration of the preferred time series query. Select from one of the following time intervals: 
["5min", "30min",
"1h", "12h", "24h", "1d", "3d", "7d", "1w", "1m", "3m", "6m", "12m", "1y"]
. 
DURATION
 must be paired with either
the 
START
 or 
END
 request.
END
UTC timestamp in ISO-8601 or UTC epoch second, which specifies the end of a time series query. The timestamp can't have a
query where 
START
 and 
END
 are the same, or where 
END
 is before 
START
, 
or where 
START
 is after 
END
.
END_POINT
The 
aspect
 of the cluster you want to monitor.
START
UTC timestamp in ISO-8601 or integer seconds where epoch format specifies the starting point of a time series query that is
mutually exclusive with 
END
.
Several of the fields have default values:
Field
Default value
 Important: 
The monitoring API is only available to IBM® Cloudant® for IBM Cloud® Enterprise customers with dedicated clusters and not to
IBM Cloud® Public customers.
Cloudant
   
249Table 2. Default values for monitoring API request fields
DURATION
5 minutes
END
No default value
START
The current time
Results format
By default, the monitoring results are returned in 
JSON
 format
. If you prefer, you can choose to receive the results in 
raw
 format
.
The results include a text string that identifies the metric that is stored on the server that provides the API capability, for example:
sumSeries(net.cloudant.mycustomer001.db*.df.srv.used)
The results include cluster-level data.
With 
format=json
 (default)
Unless you specify otherwise, the metric data that is returned is in JSON format. Each value that is returned consists of 
[datapoint, timestamp]
values.
See an example monitoring request for disk use data returned in 
JSON
 format:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/disk_use?cluster=myclustername&format=json"
See an example result after you request disk use data in 
JSON
 format:
[
 
{
  
"target"
:
 
"sumSeries(net.cloudant.mycustomer001.db*.df.srv.used)"
,
  
"datapoints"
:
 
[
   
[
523562172416.0
,
 
1391019360
]
,
   
[
524413976576.0
,
 
1391019420
]
,
   
[
519036682240.0
,
 
1391019480
]
,
   
[
518762102784.0
,
 
1391019540
]
,
   
[
523719393280.0
,
 
1391019600
]
  
]
 
}
,
 
{
  
"target"
:
 
"sumSeries(net.cloudant.mycustomer001.db*.df.srv.free)"
,
  
"datapoints"
:
 
[
   
[
6488926978048.0
,
 
1391019360
]
,
   
[
6487768301568.0
,
 
1391019420
]
,
   
[
6493145661440.0
,
 
1391019480
]
,
   
[
6493420257280.0
,
 
1391019540
]
,
   
[
4330660167680.0
,
 
1391019600
]
  
]
 
}
]
With 
format=raw
The 
raw
 format data contains a series of text strings, identifying the name of the metric and associated values.
The text string (for example 
sumSeries(net.cloudant.mycustomer001.db*.df.srv.used)
) is the name of the metric. The next two numbers are
the start and end times, expressed as UTC epoch seconds. The final number is the step size 
in seconds.
The numbers after the 
|
 character contain the metric data that is obtained from your chosen endpoint. For example, requesting metric data from
 Note: 
IBM Cloudant stores the queried data at the following resolutions: 10 seconds for the past 24 hours; 1 minute for the past 7 days; and
1 hour for the past 2 years. As a result, and to ensure that IBM Cloudant always stores the higher resolution 
interval length, deltas on the
boundary of these resolutions are trimmed by one interval's length.
Cloudant
   
250the disk use endpoint returns the output from a 
df
 command, with the disk 
use expressed as bytes stored.
See an example monitoring request for disk use data returned in 
raw
 format:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/disk_use?cluster=myclustername&format=raw"
See an example result after you request disk use data in 
raw
 format:
sumSeries(net.cloudant.mycustomer001.db*.df.srv.used),1391019780,1391020080,60|344708448256.0,345318227968.0,346120126464.0,
346716471296.0,175483256832.0
sumSeries(net.cloudant.mycustomer001.db*.df.srv.free),1391019780,1391020080,60|6.49070326579e+12,6.4896982057e+12,6.48884414
054e+12,6.48801589658e+12,4.32277107507e+12
Monitoring endpoints
To list all of the currently supported monitoring endpoints, make a request to the 
monitoring
 endpoint.
The following table lists the supported monitoring endpoints that are provided by the API:
Table 3. Monitoring API endpoints
Endpoint
Description
connections
The status of multiple load balancer connections.
disk_use
The disk use, as measured by a 
df
 command.
kv_emits
The number of 
key:value
 emits per second.
map_doc
The number of documents processed by a map function, per second.
network
The octets that are received and transmitted.
rate/status_code
The rate of requests, which are grouped by status code.
rate/verb
The rate of requests, which are grouped by HTTP verb.
rps
The number of reads per second.
wps
The number of writes per second.
See an example showing how to obtain a list of the currently supported monitoring endpoints:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring"
See an example response that lists the available monitoring endpoints:
{
    
"targets"
:
 
[
        
"node_disk_free_srv"
,
        
"rps"
,
        
"kv_emits"
,
        
"smoosh_channels/slack_dbs"
,
        
"smoosh_channels/upgrade_dbs"
,
        
"smoosh_channels/ratio_dbs"
,
        
"smoosh_channels/ratio_views"
,
        
"smoosh_channels/slack_views"
,
        
"smoosh_channels/upgrade_views"
,
        
"uptime"
,
        
"map_doc"
,
        
"wps"
,
        
"node_peak_cpu"
,
        
"rate/status_code"
,
        
"rate/verb"
,
Cloudant
   
251        
"disk_use"
,
        
"node_mean_cpu"
,
        
"memory"
,
        
"os_proc_count"
,
        
"run_queue"
,
        
"node_disk_use_srv"
,
        
"process_count"
,
        
"response_time"
    
]
}
Examples of monitoring requests
connections
See an example of a 
connections
 monitoring request:
$ 
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/connections?
cluster=myclustername&node=myloadbalancername&format=json"
The response includes a data series for the following connection states:
$ 
{
  
"end"
:
 
1512989500
,
  
"start"
:
 
1512989170
,
  
"target_responses"
:
 
[
     
{
       
"datapoints"
:
 
[
            
[
              
0
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections CLOSED"
      
}
,
      
{
 
        
"datapoints"
:
 
[
            
[
              
19
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections CLOSE_WAIT"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
2
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections CLOSING"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
280
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections ESTABLISHED"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
7
,
              
1512989170
            
]
        
]
,
Cloudant
   
252        
"target"
:
 
"myclustername.myloadbalancername Connections FIN_WAIT1"
      
}
,
      
{
 
        
"datapoints"
:
 
[
            
[
              
0
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections FIN_WAIT2"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
0
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections LAST_ACK"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
4
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections LISTEN"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
1
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections SYN_RECV"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
0
,
              
1512989170
            
]
        
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections SYN_SENT"
      
}
,
      
{
        
"datapoints"
:
 
[
            
[
              
28
,
              
1512989170
              
]
            
]
,
        
"target"
:
 
"myclustername.myloadbalancername Connections TIME_WAIT"
      
}
   
]
}
You must explicitly specify the load balancer in the request.
disk_use
See an example of a 
disk_use
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/disk_use?cluster=myclustername&format=json"
See example results (abbreviated) from a 
disk_use
 monitoring request:
Cloudant
   
253{
 
"start"
:
 
1435935759
,
 
"end"
:
 
1435936059
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername Used disk space (bytes)"
,
   
"datapoints"
:
 
[
    
[
     
6855438336.0
,
     
1435935780
    
]
,
    
[
     
null
,
     
1435935795
    
]
,
    
[
     
null
,
     
1435935810
    
]
,
    ...
    
[
     
null
,
     
1435936065
    
]
   
]
  
}
,
  
{
   
"target"
:
 
"myclustername Free disk space (bytes)"
,
   
"datapoints"
:
 
[
    
[
     
7141069422592.0
,
     
1435935780
    
]
,
    
[
     
null
,
     
1435935795
    
]
,
    
[
     
null
,
     
1435935810
    
]
,
    ...
    
[
     
null
,
     
1435936065
    
]
   
]
  
}
 
]
}
kv_emits
See an example of a 
kv_emits
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/kv_emits?cluster=myclustername&format=json"
See example results (abbreviated) from a 
kv_emits
 monitoring request:
{
 
"start"
:
 
1436194248
,
 
"end"
:
 
1436194548
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername Key:value pairs emitted per second from map functions"
,
   
"datapoints"
:
 
[
    
[
     
0.0
,
     
1436194230
Cloudant
   
254    
]
,
    
[
     
0.0
,
     
1436194245
    
]
,
    
[
     
0.8000000000001819
,
     
1436194260
    
]
,
    ...
    
[
     
null
,
     
1436194515
    
]
   
]
  
}
 
]
}
map_doc
See an example of a 
map_doc
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/map_doc?cluster=myclustername&format=json"
See example results (abbreviated) from a 
map_doc
 monitoring request:
{
 
"start"
:
 
1436194475
,
 
"end"
:
 
1436194775
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername Documents per second through map functions"
,
   
"datapoints"
:
 
[
    
[
     
0.0
,
     
1436194480
    
]
,
    
[
     
0.5
,
     
1436194495
    
]
,
    
[
     
0.4000000000005457
,
     
1436194510
    
]
,
    ...
    
[
     
0.0
,
     
1436194765
    
]
   
]
  
}
 
]
}
network
$ 
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/network?cluster=myclustername&node=myloadbalancername&format=json"
$ 
{
  
"end"
:
 
1512989748
,
  
"start"
:
 
1512989450
,
  
"target_responses"
:
 
[
      
{
        
"datapoints"
:
 
[
          
[
           
20247725.5
,
Cloudant
   
255           
1512989450
          
]
        
]
,
        
"target"
:
 
"myclustername Octets tx Per Second"
      
}
,
      
{
         
"datapoints"
:
 
[
             
[
               
17697329.3046875
,
               
1512989450
             
]
         
]
,
         
"target"
:
 
"myclustername Octets rx Per Second"
 
       
}
    
]
}
You must explicitly specify the load balancer in the request.
rate/status_code
See an example of a 
rate/status_code
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/rate/status_code?cluster=myclustername&format=json"
See example results (abbreviated) from a 
rate/status_code
 monitoring request:
{
 
"start"
:
 
1436194902
,
 
"end"
:
 
1436195202
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername 2xx"
,
   
"datapoints"
:
 
[
    
[
     
null
,
     
1436194910
    
]
,
    
[
     
36.0
,
     
1436194920
    
]
,
    ...
    
[
     
0.0
,
     
1436195200
    
]
   
]
  
}
,
  
{
   
"target"
:
 
"myclustername 3xx"
,
   
"datapoints"
:
 
[
    
[
     
null
,
     
1436194910
    
]
,
    
[
     
0.0
,
     
1436194920
    
]
,
    ...
    
[
     
null
,
     
1436195200
    
]
   
]
  
}
,
  
{
   
"target"
:
 
"myclustername 4xx"
,
Cloudant
   
256   
"datapoints"
:
 
[
    
[
     
null
,
     
1436194910
    
]
,
    
[
     
0.0
,
     
1436194920
    
]
,
    ...
    
[
     
0.0
,
     
1436195200
    
]
   
]
  
}
,
  
{
   
"target"
:
 
"myclustername 5xx"
,
   
"datapoints"
:
 
[
    
[
     
null
,
     
1436194910
    
]
,
    
[
     
0.0
,
     
1436194920
    
]
,
    ...
    
[
     
null
,
     
1436195200
    
]
   
]
  
}
 
]
}
rate/verb
See an example of a 
rate/verb
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/rate/verb?cluster=myclustername&format=json"
See example results (abbreviated) from a 
rate/verb
 monitoring request:
{
 
"start"
:
 
1436195497
,
    
"end"
:
 
1436195797
,
 
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername GET"
,
 
   
"datapoints"
:
 
[
    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
36.0
,
 
     
1436195510
    
]
,
 
    ...
    
[
     
49.5
,
 
     
1436195790
    
]
   
]
  
}
,
 
  
{
   
"target"
:
 
"myclustername POST"
,
 
   
"datapoints"
:
 
[
Cloudant
   
257    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
0.0
,
 
     
1436195510
    
]
,
 
    ...
    
[
     
0.0
,
 
     
1436195790
    
]
   
]
  
}
,
 
  
{
   
"target"
:
 
"myclustername PUT"
,
 
   
"datapoints"
:
 
[
    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
0.0
,
 
     
1436195510
    
]
,
 
    ...
    
[
     
0.0
,
 
     
1436195790
    
]
   
]
  
}
,
 
  
{
   
"target"
:
 
"myclustername DELETE"
,
 
   
"datapoints"
:
 
[
    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
0.0
,
 
     
1436195510
    
]
,
 
    ...
    
[
     
0.0
,
 
     
1436195790
    
]
   
]
  
}
,
 
  
{
   
"target"
:
 
"myclustername COPY"
,
 
   
"datapoints"
:
 
[
    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
0.0
,
 
     
1436195510
    
]
,
 
    ...
    
[
     
0.0
,
 
     
1436195790
    
]
   
]
  
}
,
 
  
{
   
"target"
:
 
"myclustername HEAD"
,
 
Cloudant
   
258   
"datapoints"
:
 
[
    
[
     
null
,
 
     
1436195500
    
]
,
 
    
[
     
0.0
,
     
1436195510
    
]
,
 
    ...
    
[
     
0.0
,
 
     
1436195790
    
]
   
]
  
}
 
]
}
response_time
See an example of a 
response_time
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/response_time?cluster=myclustername&format=json"
See example results (abbreviated) from a 
response_time
 monitoring request:
{
  
"start"
:
 
1523984559
,
  
"end"
:
 
1523984859
,
  
"target_responses"
:
 
[
    
{
      
"datapoints"
:
 
[
        
[
          
118.1668472290039
,
          
1523984540
        
]
,
        
[
          
90.57628631591797
,
          
1523984550
        
]
,
        
[
          
142.6778106689453
,
          
1523984560
        
]
,
        
[
          
118.42487335205078
,
          
1523984570
        
]
,
        
[
          
120.38044738769531
,
          
1523984580
        
]
,
        
[
          
103.94148254394531
,
          
1523984590
        
]
,
        
[
          
126.64134979248047
,
          
1523984600
        
]
,
        
[
          
113.03324127197266
,
          
1523984610
        
]
,
        
[
          
136.9058074951172
,
          
1523984620
        
]
,
        
[
Cloudant
   
259          
148.68711853027344
,
          
1523984630
        
]
,
        
[
          
121.22771453857422
,
          
1523984640
        
]
,
        
[
          
142.86459350585938
,
          
1523984650
        
]
,
        
[
          
103.75953674316406
,
          
1523984660
        
]
,
        
[
          
139.1707763671875
,
          
1523984670
        
]
,
        
[
          
118.29866027832031
,
          
1523984680
        
]
,
        
[
          
126.3541259765625
,
          
1523984690
        
]
,
        
[
          
115.5962905883789
,
          
1523984700
        
]
,
        
[
          
106.68751525878906
,
          
1523984710
        
]
,
        
[
          
144.12387084960938
,
          
1523984720
        
]
,
        
[
          
103.8598861694336
,
          
1523984730
        
]
,
        
[
          
136.84429931640625
,
          
1523984740
        
]
,
        
[
          
110.58084106445312
,
          
1523984750
        
]
,
        
[
          
94.69702911376953
,
          
1523984760
        
]
,
        
[
          
126.85747528076172
,
          
1523984770
        
]
,
        
[
          
100.8759994506836
,
          
1523984780
        
]
,
        
[
          
145.0876922607422
,
          
1523984790
        
]
,
        
[
          
100.77622985839844
,
          
1523984800
        
]
,
Cloudant
   
260        
[
          
null
,
          
1523984810
        
]
,
        
[
          
null
,
          
1523984820
        
]
,
        
[
          
null
,
          
1523984830
        
]
      
]
,
      
"target"
:
 
"myclustername Response Time (ms)"
    
}
  
]
}
rps
See an example of an 
rps
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/rps?cluster=myclustername&format=json"
See example results (abbreviated) from an 
rps
 monitoring request:
{
 
"start"
:
 
1436195908
,
 
"end"
:
 
1436196208
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername Document Reads Per Second"
,
   
"datapoints"
:
 
[
    
[
     
0.20000000001164153
,
     
1436195910
    
]
,
    
[
     
0.10000000000582077
,
     
1436195925
    
]
,
    ...
    
[
     
null
,
     
1436196195
    
]
   
]
  
}
 
]
}
wps
See an example of a 
wps
 monitoring request:
curl 
"https://
$ACCOUNT
.cloudant.com/_api/v2/monitoring/wps?cluster=myclustername&format=json"
See example results (abbreviated) from a 
wps
 monitoring request:
{
 
"start"
:
 
1436195999
,
 
"end"
:
 
1436196299
,
 
"target_responses"
:
 
[
  
{
   
"target"
:
 
"myclustername Document Writes Per Second"
,
   
"datapoints"
:
 
[
    
[
     
1.2999999999992724
,
Cloudant
   
261     
1436196000
    
]
,
    
[
     
0.5
,
     
1436196015
    
]
,
    ...
    
[
     
null
,
     
1436196285
    
]
   
]
  
}
 
]
}
Capacity
IBM Cloudant lets you: view the current and target provisioned throughput capacity setting, set the target provisioned throughput capacity setting,
and view the current consumption of provisioned throughput capacity used.
For more information, see 
provisioned throughput capacity
 about how IBM Cloudant allocates and uses capacity, and how to view and change the
capacity 
in the UI.
View the current and target provisioned throughput capacity setting
Use a GET to the 
/_api/v2/user/capacity/throughput
 endpoint to see what amount of provisioned throughput capacity is allocated to the IBM
Cloudant instance and what is the target provisioned throughput capacity. When you change 
the target capacity, the current capacity asynchronously
changes to meet the target capacity. The size of the capacity change and the amount of data that is stored in the IBM Cloudant instance determines
the time that it takes before the current 
and target capacities match. The capacity change is complete when the current and target capacity is the
same.
Method
GET
Path
/_api/v2/user/capacity/throughput
Response
Both the current and target capacity setting. Each includes the number of capacity blocks and total reads/sec, writes/sec, and global
queries/sec of throughput capacity.
See the following example request to retrieve the current and target capacity by using HTTP:
GET /_api/v2/user/capacity/throughput
See the following example request to retrieve the current and target capacity:
Curl
curl 
"
$SERVICE_URL
/_api/v2/user/capacity/throughput"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.CapacityThroughputInformation;
 Note: 
The Capacity API requires either IBM Cloudant legacy auth admin role or IAM Manager role to access the API endpoints. The following
curl examples omit the authentication aspect for simplicity. See the 
authentication overview
 
section for more details on using both types of
authentication.
Cloudant
   
262Cloudant
 
service
 
=
 Cloudant.newInstance();
CapacityThroughputInformation
 
response
 
=
service.getCapacityThroughputInformation().execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getCapacityThroughputInformation
().
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_capacity_throughput_information().get_result()
print
(response)
Go
getCapacityThroughputInformationOptions := service.NewGetCapacityThroughputInformationOptions()
capacityThroughputInformation, response, err :=
 
service.GetCapacityThroughputInformation(getCapacityThroughputInformationOptions)
if
 err != 
nil
 {
panic
(err)
}
b, _ := json.MarshalIndent(capacityThroughputInformation, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
The returned structure includes the following fields:
current
Details the current capacity that is allocated and shows both the number of capacity blocks and breakdown of throughput request classes.
target
Details the target capacity that is allocated and shows both the number of capacity blocks and breakdown of throughput request classes.
blocks
Number of provisioned throughput capacity blocks, where a block is 100 reads/sec, 50 writes/sec, and 5 global queries/sec.
throughput
Breakdown of the specific number of reads/sec, writes/sec, and global queries/sec.
Cloudant
   
263See the following example JSON response with the current and target capacity:
{
  
"current"
:
 
{
    
"throughput"
:
 
{
      
"read"
:
 
500
,
      
"write"
:
 
250
,
      
"blocks"
:
 
5
,
      
"query"
:
 
25
    
}
  
}
,
  
"target"
:
 
{
    
"throughput"
:
 
{
      
"read"
:
 
1000
,
      
"write"
:
 
500
,
      
"blocks"
:
 
10
,
      
"query"
:
 
50
    
}
  
}
}
Set the target provisioned throughput capacity setting
Use a PUT to the 
/_api/v2/user/capacity/throughput
 endpoint to set the target provisioned throughput capacity for an IBM Cloudant instance.
When you change the target capacity, the current capacity asynchronously changes to meet 
the target capacity.
Method
PUT
Path
/_api/v2/user/capacity/throughput
Response
Both the current and target capacity setting, including the number of capacity blocks and total reads/sec, writes/sec, and global queries/sec.
See the following example request to set the target capacity by using HTTP:
PUT $SERVICE_URL/_api/v2/user/capacity/throughput
Content-Type
: 
application/json
See the following example JSON object to set target capacity:
{
  
"blocks"
: 
$NUMBER_OF_BLOCKS
}
Here a block consists of 100 reads/sec, 50 writes/sec, and 5 global queries/sec of provisioned throughput capacity. The 
$NUMBER_OF_BLOCKS
 field
must be an integer in the range of 1 to 100. 
Larger capacity sizes can be obtained by contacting IBM Cloudant support.
See the following example request to set the target capacity:
Curl
curl -X PUT 
"
$SERVICE_URL
/_api/v2/user/capacity/throughput"
 -H 
"Content-Type: application/json"
 --data 
'{"blocks": 1}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.CapacityThroughputInformation;
import
 com.ibm.cloud.cloudant.v1.model.PutCapacityThroughputConfigurationOptions;
Cloudant
   
264Cloudant
 
service
 
=
 Cloudant.newInstance();
PutCapacityThroughputConfigurationOptions
 
options
 
=
    
new
 
PutCapacityThroughputConfigurationOptions
.Builder()
        .blocks(
1
)
        .build();
CapacityThroughputInformation
 
response
 
=
service.putCapacityThroughputConfiguration(options).execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
putCapacityThroughputConfiguration
({
  
blocks
: 
1
,
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.put_capacity_throughput_configuration(
  blocks=
1
).get_result()
print
(response)
Go
putCapacityThroughputConfigurationOptions := service.NewPutCapacityThroughputConfigurationOptions(
  
1
,
)
capacityThroughputConfiguration, response, err :=
 
service.PutCapacityThroughputConfiguration(putCapacityThroughputConfigurationOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(capacityThroughputConfiguration, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
The returned structure includes the following fields:
current
Details the current capacity that is allocated and shows both the number of capacity blocks and breakdown of throughput requests classes.
target
Cloudant
   
265Details the target capacity set and shows both the number of capacity blocks and the breakdown of throughput requests classes.
blocks
Number of provisioned throughput capacity blocks, where block is 100 reads/sec, 50 writes/sec, and 5 global queries/sec.
throughput
A breakdown of the specific number of reads/sec, writes/sec, and global queries/sec.
See the following example JSON response with the target capacity set:
{
  
"current"
:
 
{
    
"throughput"
:
 
{
      
"read"
:
 
500
,
      
"write"
:
 
250
,
      
"blocks"
:
 
5
,
      
"query"
:
 
25
    
}
  
}
,
  
"target"
:
 
{
    
"throughput"
:
 
{
      
"read"
:
 
1000
,
      
"write"
:
 
500
,
      
"blocks"
:
 
10
,
      
"query"
:
 
50
    
}
  
}
}
View the current consumption of provisioned throughput capacity used
Use a GET method to the 
/_api/v2/user/current/throughput
 endpoint to see the current consumption of provisioned throughput capacity for an
IBM Cloudant instance. The current consumption shows the quantities of reads, writes, and 
global queries conducted against the instance for a given
second. When you use this endpoint, it is a best practice to aggregate this data continuously over time to get a more comprehensive view of a IBM
Cloudant instance's throughput consumption 
patterns.
Method
GET
Path
/_api/v2/user/current/throughput
Response
The current consumption of provisioned throughput capacity used, broken down by the number of reads, writes, and global queries.
See the following example request to retrieve the current consumption of capacity by using HTTP:
GET $SERVICE_URL/_api/v2/user/current/throughput
See the following example request to retrieve the current consumption of capacity:
Curl
curl 
"
$SERVICE_URL
/_api/v2/user/current/throughput"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.CurrentThroughputInformation;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Cloudant
   
266CurrentThroughputInformation
 
response
 
=
service.getCurrentThroughputInformation().execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getCurrentThroughputInformation
().
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_current_throughput_information().get_result()
print
(response)
Go
getCurrentThroughputInformationOptions := service.NewGetCurrentThroughputInformationOptions()
currentThroughputInformation, response, err :=
 
service.GetCurrentThroughputInformation(getCurrentThroughputInformationOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(currentThroughputInformation, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
The returned structure includes the following fields:
throughput
 - Breakdown of the current number of reads, writes, and global queries used.
See the following example JSON response of the current consumption of capacity:
{
  
"throughput"
:
 
{
    
"read"
:
 
133
,
    
"write"
:
 
42
,
    
"query"
:
 
13
  
}
}
Active tasks
The 
/_active_tasks
 endpoint provides a list of the tasks that are running on the server, which is helpful for 
monitoring
 
the performance of your
system.
Cloudant
   
267You can retrieve a list of active tasks, including compaction, replication, and indexing tasks. For more examples on using the 
/_active_tasks
endpoint, see the 
Managing tasks
 
guide.
Retrieving a list of active tasks
Method
GET
Path
/_active_tasks
Response
List of running tasks, including the task type, name, status, and process ID.
Roles permitted
_admin
You can get a list of active tasks by using the 
/_active_tasks
 URL. The result is a JSON array of the currently running tasks, with each task
described with a single object.
See the example request to retrieve a list of active tasks by using HTTP commands:
GET
 
/_active_tasks
 
HTTP/1.1
See the example request to retrieve a list of active tasks by using the command line:
curl 
"https://
$ACCOUNT
.cloudant.com/_active_tasks"
 \
 -u 
$ACCOUNT
The returned structure includes the following fields for each task:
Table 1. Fields in the returned structure
Name
Description
database
The database and shard on which the operation occurs.
pid
Erlang Process ID
started_on
Time when the task was started. The value is an integer that includes the UNIX™ time UTC.
total_changes
Total number of documents to be processed by the task. The exact meaning depends on the type of the task.
type
Operation Type
updated_on
Time that the task status was updated. The field updates every few seconds. Returns the most recent update.
In the 
type
 field, the possible values include:
database_compaction
view_compaction
replication
indexer
search_indexer
The meaning of other fields in the JSON response depends on the type of the task.
See the example JSON response array that includes details of currently running tasks:
[
Cloudant
   
268 
{
  
"user"
:
 
null
,
  
"updated_on"
:
 
1363274088
,
  
"type"
:
 
"replication"
,
  
"target"
:
 
"https://repl:*****@tsm.cloudant.com/user-3dglstqg8aq0uunzimv4uiimy/"
,
  
"docs_read"
:
 
0
,
  
"doc_write_failures"
:
 
0
,
  
"doc_id"
:
 
"tsm-admin__to__user-3dglstqg8aq0uunzimv4uiimy"
,
  
"continuous"
:
 
true
,
  
"checkpointed_source_seq"
:
 
"403-
g1AAAADfeJzLYWBgYMlgTmGQS0lKzi9KdUhJMjTRyyrNSS3QS87JL01JzCvRy0styQGqY0pkSLL___9_VmIymg5TXDqSHIBkUj1YUxyaJkNcmvJYgCRDA5AC6tuf
lZhGrPsgGg9ANAJtzMkCAPFSStc"
,
  
"changes_pending"
:
 
134
,
  
"pid"
:
 
"<0.1781.4101>"
,
  
"node"
:
 
"dbcore@db11.julep.cloudant.net"
,
  
"docs_written"
:
 
0
,
  
"missing_revisions_found"
:
 
0
,
  
"replication_id"
:
 
"d0cdbfee50a80fd43e83a9f62ea650ad+continuous"
,
  
"revisions_checked"
:
 
0
,
  
"source"
:
 
"https://repl:*****@tsm.cloudant.com/tsm-admin/"
,
  
"source_seq"
:
 
"537-
g1AAAADfeJzLYWBgYMlgTmGQS0lKzi9KdUhJMjTUyyrNSS3QS87JL01JzCvRy0styQGqY0pkSLL___9_VmI9mg4jXDqSHIBkUj1WTTityWMBkgwNQAqob39WYhex
tkE0HoBoBNo4MQsAFuVLVQ"
,
  
"started_on"
:
 
1363274083
 
}
,
 
{
  
"user"
:
 
"acceptly"
,
  
"updated_on"
:
 
1363273779
,
  
"type"
:
 
"indexer"
,
  
"node"
:
 
"dbcore@db11.julep.cloudant.net"
,
  
"pid"
:
 
"<0.20723.4070>"
,
  
"changes_done"
:
 
189
,
  
"database"
:
 
"shards/00000000-3fffffff/acceptly/acceptly_my_chances_logs_live.1321035717"
,
  
"design_document"
:
 
"_design/MyChancesLogCohortReport"
,
  
"started_on"
:
 
1363273094
,
  
"total_changes"
:
 
26389
 
}
,
 
{
  
"user"
:
 
"username"
,
  
"updated_on"
:
 
1371118433
,
  
"type"
:
 
"search_indexer"
,
  
"total_changes"
:
 
5466
,
  
"node"
:
 
"dbcore@db7.meritage.cloudant.net"
,
  
"pid"
:
 
"<0.29569.7037>"
,
  
"changes_done"
:
 
4611
,
  
"database"
:
 
"shards/40000000-7fffffff/username/database_name"
,
  
"design_document"
:
 
"_design/lucene"
,
  
"index"
:
 
"search1"
,
  
"started_on"
:
 
1371118426
 
}
,
 
{
  
"view"
:
 
1
,
  
"user"
:
 
"acceptly"
,
  
"updated_on"
:
 
1363273504
,
  
"type"
:
 
"view_compaction"
,
  
"total_changes"
:
 
26095
,
  
"node"
:
 
"dbcore@db11.julep.cloudant.net"
,
  
"pid"
:
 
"<0.21218.4070>"
,
  
"changes_done"
:
 
20000
,
  
"database"
:
 
"shards/80000000-bfffffff/acceptly/acceptly_my_chances_logs_live.1321035717"
,
  
"design_document"
:
 
"_design/MyChancesLogCohortReport"
,
  
"phase"
:
 
"view"
,
  
"started_on"
:
 
1363273094
 
}
,
 
{
  
"updated_on"
:
 
1363274040
,
  
"node"
:
 
"dbcore@db11.julep.cloudant.net"
,
  
"pid"
:
 
"<0.29256.4053>"
,
  
"changes_done"
:
 
272195
,
  
"database"
:
 
"shards/00000000-3fffffff/heroku/app3245179/id_f21a08b7005e_logs.1346083461"
,
  
"started_on"
:
 
1363272496
,
Cloudant
   
269  
"total_changes"
:
 
272195
,
  
"type"
:
 
"database_compaction"
 
}
]
Specific response fields for compaction tasks
Table 2. Response fields for compaction tasks
Name
Description
changes_done
Number of documents compacted.
phase
Reports the stage of compaction.
total_changes
Number of documents in the database.
In the 
phase
 field, the value indicates the stage that was reached by compaction:
ids
Document compaction is in progress.
views
View compaction is in progress.
Specific response fields for replication tasks
Table 3. Response fields for replication tasks
Name
Description
changes_pending
Number of documents that need to be changed in the target database, expressed as an integer.
continuous
Boolean value that indicates whether the replication is continuous.
docs_read
Number of documents that are read from the source database, expressed as an integer.
replication_id
Unique identifier string of the replication that can be used to cancel the task.
revisions_checked
Number of document revisions that were checked to verify whether they're already in the target database.
source
An obfuscated URL string that indicates the database from which the task is replicating.
target
An obfuscated URL string that indicates the database to which the task is replicating.
user
User who started the replication, expressed as a string, or 
null
 if the replication was not initiated by a user.
Specific response fields for indexing tasks
Table 4. Response fields for indexing tasks
Name
Description
changes_done
Number of document revisions that are processed by this task. A document can have one or more revisions.
design_document
The design document that includes the view or index function or functions.
total_changes
The number of unindexed changes to process. This count includes deleted documents, although these documents are
automatically skipped by the indexer.
Cloudant
   
270Managing tasks
Creating new indexes over lots of data or replicating a large database can take quite a while.
How can you determine whether your tasks are progressing or completed? The 
_active_tasks
 endpoint
 provides information about all ongoing
tasks. However, if you 
start numerous tasks, some of them might be scheduled to run later and don't show up under 
_active_tasks
 until they start.
See the following examples of SDK and curl code:
Curl
curl 
"
$SERVICE_URL
/_active_tasks"
 
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ActiveTask;
Cloudant
 
service
 
=
 Cloudant.newInstance();
List<ActiveTask> response =
    service.getActiveTasks().execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getActiveTasks
().
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_active_tasks().get_result()
print
(response)
Go
getActiveTasksOptions := service.NewGetActiveTasksOptions()
activeTask, response, err := service.GetActiveTasks(getActiveTasksOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(activeTask, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
    
"encoding/json"
    
"fmt"
    
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
Cloudant
   
271All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Now, you learn how to use the 
_active_tasks
 endpoint to monitor long-running tasks. The 
curl
 command is used to access the endpoint. The
jq
 command line JSON processor is used to process the JSON response.
This task-focused tutorial covers only what is essential to accomplish this task. For more information, see the 
Using IBM® Cloudant® for IBM Cloud®
for a complete guide to the available 
options.
curl
 and 
jq
 basics
To get all active tasks and format the output nicely, call your account by using 
curl
, and pipe the output to 
jq
.
With 
jq
, you filter a list of documents by their field values. This filter makes it easier to get all replication documents, or the details of just one
particular view indexing task. The API reference has more information about 
the options.
See an example of obtaining and formatting a list of active tasks:
curl 
"
$SERVICE_URL
/_active_tasks"
 | jq
Monitoring view builds and search indexes
View indexes are rebuilt when a design document is updated. An update to any one of the views causes all the views in the document to be rebuilt.
Search indexes are rebuilt only when their corresponding index function is changed. For each search index that is built and for each design document
with views that are changed, a new task is created for each replica and each shard in a cluster.
For example, if 24 shards with three replicas each exist, and you update two search indexes, then 24 x 3 x 2 = 144 tasks run.
To find all the view indexing tasks, pipe the 
curl
 output to 
jq
, and let it filter the documents in the array by their type field. A corresponding
command works for search indexing tasks.
In each case, the results of searching for a list of indexing tasks is a list of JSON objects: one for each of the active tasks found.
See an example of finding all view indexing tasks by filtering for the 
indexer
 type:
curl -s 
"
$SERVICE_URL
/_active_tasks"
 | jq 
'.[] | select(.type=="indexer")'
See an example of finding all search indexing tasks by filtering for the 
search_indexer
 type:
curl -s 
"
$SERVICE_URL
/_active_tasks"
 | jq 
'.[] | select(.type=="search_indexer")'
See example results after you search for view indexing tasks:
{
    
"total_changes"
:
 
6435
,
    
"started_on"
:
 
1371118332
,
    
"user"
:
 
"username"
,
    
"updated_on"
:
 
1371118334
,
    
"type"
:
 
"indexer"
,
    
"node"
:
 
"dbcore@db6.meritage.cloudant.net"
,
    
"pid"
:
 
"<0.16366.6103>"
,
    
"changes_done"
:
 
364
,
    
"database"
:
 
"shards/40000000-7fffffff/username/database"
,
    
"design_document"
:
 
"_design/ngrams"
}
Estimating the time to complete a task
To estimate the time needed until the indexing task is complete, monitor the number of 
changes_done
 and compare this value to 
total_changes
.
For example, if 
changes_done
 advances by 250 per second, and 
total_changes
 is 1,000,000, the task is expected to take 1,000,000 / 250 =
4,000 seconds, or about 66 minutes,to complete.
Estimates of the time to complete an indexing task can't be 100% correct. The actual time to complete the task depends on the following factors:
The time that it takes to process each document. For instance, a view might check the type of document first, and emit new index entries for
Cloudant
   
272only one type.
The size of the documents.
The current workload on the cluster.
You must assume that these factors might combine to produce considerable inaccuracy in your estimate.
See the example of extracting the 
changes_done
 field by using 
jq
:
curl ... | jq 
'.[] | select(.type=="search_indexer") | .changes_done'
Monitoring replication
To find all replication tasks, pipe the 
curl
 output to 
jq
, and filter the documents in the array by their type field.
Make it easier to select the information about a replication process from the list of active tasks by following these steps:
a
. 
Start the replication process by creating a document in the 
_replicator
 database.
b
. 
Set its 
_id
 field to a known value.
See an example of finding all replication tasks, by filtering for the 
replication
 type:
curl -s 
"
$SERVICE_URL
/_active_tasks"
 | jq 
'.[] | select(.type=="replication")'
See an example of finding a specific replication task, by filtering for a known document identity:
curl ... | jq 
'.[] | select(.doc_id=="ID")'
See an example of finding a specific replication task, by filtering for a known 
replication_id
:
curl ... | jq 
'.[] | select(.replication_id=="ID")'
See an example result after you search for a replication task:
{
    
"started_on"
:
 
1371094220
,
    
"source_seq"
:
 
"62960-sakdjflksdfjsdlkafjalskdfjlsakfjlasdkjksald"
,
    
"source"
:
 
""
,
    
"revisions_checked"
:
 
12
,
    
"continuous"
:
 
true
,
    
"doc_id"
:
 
null
,
    
"doc_write_failures"
:
 
0
,
    
"docs_read"
:
 
12
,
    
"target"
:
 
""
,
    
"type"
:
 
"replication"
,
    
"updated_on"
:
 
1371118477
,
    
"user"
:
 
"username"
,
    
"checkpointed_source_seq"
:
 
"61764-dskfjalsfjsalkfjssadjfhasdfkjhsdkfhsdkf"
,
    
"changes_pending"
:
 
1196
,
    
"pid"
:
 
"<0.9955.4120>"
,
    
"node"
:
 
"dbcore@db7.meritage.cloudant.net"
,
    
"docs_written"
:
 
12
,
    
"missing_revisions_found"
:
 
12
,
    
"replication_id"
:
 
"asfksdlfkjsadkfjsdalkfjas+continuous+create_target"
}
Troubleshooting stuck tasks
Is a task stuck?
For a one-off, non-continuous replication, where the source database isn't updated significantly during the replication, the 
changes_pending
 value
shows how many documents remain to be processed. Therefore, the 
changes_pending
 
value is good indicator of when the replication is likely to be
finished.
For a continuous replication, you're more interested in how the number of documents processed changes over time, and whether the
changes_pending
 value increases. If 
changes_pending
 increases, but 
revisions_checked
 
stays constant for a while, the replication is probably
Cloudant
   
273stalled. If 
changes_pending
 increases, and 
revisions_checked
 also increases, these increases might indicate that the replication can't keep up
with the volume 
of data added to, or updated in, the database.
What to do about a stuck task?
To resolve a stalled replication, you might have to 
cancel the replication process
 and start it again.
If that doesn't help, the replication might be stalled because the user who is accessing the source or target databases doesn't have write
permissions.
If you created the replication process by creating a document in the 
_replicator
 database, you can also check the status of the replication there.
 Note: 
Replication uses 
checkpoints
, which means that content that is already replicated and unchanged doesn't have to be replicated again
if the replication is restarted.
Cloudant
   
274Querying the database
Working with IBM Cloudant Query
IBM® Cloudant® for IBM Cloud® Query is a declarative JSON querying syntax for IBM Cloudant databases. You can use a 
json
 or 
text
 type of index
with IBM Cloudant.
In the following cases, you can specify how the index is created by making it of type 
json
:
You know exactly what data you want to look for.
You want to keep storage and processing requirements to a minimum.
But for maximum flexibility when you search for data, you typically create an index of type 
text
. Indexes of type 
text
 have a simple mechanism
for automatically indexing all the fields in the documents.
Creating an index
You can create an index with one of the following types:
"type": "json"
"type": "text"
Creating a 
type=json
 index
To create a JSON index in the database 
$DATABASE
, make a 
POST
 request to 
/$DATABASE/_index
 with a JSON object that describes the index in
the request body. The 
type
 field of the JSON object 
must be set to 
json
. A JSON index can be partitioned or global; this option is set by using the
partitioned
 field.
See the following example that uses HTTP to request an index of type 
JSON
:
POST
 
/$DATABASE/_index
 
HTTP/1.1
Content-Type
: 
application/json
See the following example of a JSON object that creates a partitioned index that is called 
foo-partitioned-index
 for the field called 
foo
:
{
    
"index"
:
 
{
        
"fields"
:
 
[
"foo"
]
    
}
,
    
"name"
 
:
 
"foo-partitioned-index"
,
    
"type"
 
:
 
"json"
,
    
"partitioned"
:
 
true
}
See the following example of a JSON object that creates a global index that is called 
bar-global-index
 for the field called 
bar
:
{
    
"index"
:
 
{
        
"fields"
:
 
[
"bar"
]
    
}
,
    
"name"
 
:
 
"bar-global-index"
,
    
"type"
 
:
 
"json"
,
    
"partitioned"
:
 
false
}
See the following example of returned JSON, confirming that the index was created:
{
    
"result"
:
 
"created"
}
 Tip: 
While more flexible, 
text
 indexes might take longer to create and require more storage resources than 
json
 indexes.
Cloudant
   
275Table 1. Request body format
Field
Description
index
fields - A JSON array of field names that uses the 
sort syntax
. Nested fields are also allowed, for example, 
person.name
.
ddoc
(optional)
Name of the design document in which the index is created. By default, each index is created in its own design document.
Indexes can be grouped into design documents for efficiency. However, a change to one index in a design document
invalidates all other indexes in the same document.
type
(optional)
Can be 
json
 or 
text
. Defaults to 
json
.
name
(optional)
Name of the index. If no name is provided, a name is generated automatically.
partitioned
(optional,
boolean)
Determines whether this index is partitioned. For more information, see 
the 
partitioned
 field
.
The 
partitioned
 field
This field sets whether the created index is a partitioned or global index.
Table 2. Partitioned field values
Value
Description
Notes
true
Create the index as partitioned.
Can be used only in a partitioned database.
false
Create the index as global.
Can be used in any database.
The default follows the 
partitioned
 setting for the database:
Table 3. Default partitioned value
Is the database partitioned?
Default 
partitioned
 value
Allowed values
Yes
true
true
, 
false
No
false
false
Table 4. Return codes
Code
Description
200
Index was created successfully or existed in the database.
400
Bad request - the request body doesn't have the specified format.
Creating a 
type=text
 index
When you create a single text index, it's a good practice to use the default values, but some useful index attributes can be modified.
A 
text
 index can be partitioned or global; this option is set by using the 
partitioned
 field.
 Important: 
It's important to reiterate that the default 
partitioned
 value is 
true
 for indexes that are created in a partitioned database.
This default value means that the index 
cannot
 be used to satisfy global queries.
 Tip: 
For Full Text Indexes (FTIs), 
type
 must be set to 
text
.
Cloudant
   
276The 
name
 and 
ddoc
 attributes are for grouping indexes into design documents. Use the attributes to refer to index groups by using a custom string
value. If no values are supplied for these fields, they're automatically 
populated with a hash value.
If you create multiple text indexes in a database, with the same 
ddoc
 value, you need to know at least the 
ddoc
 value and the 
name
 value.
Creating multiple indexes with the same 
ddoc
 value 
places them into the same design document. Generally, you must put each text index into its
own design document.
For more information, see the 
more about 
text
 indexes
.
See the following example of a JSON document that requests a partitioned index creation:
{
    
"index"
:
 
{
        
"fields"
:
 
[
            
{
                
"name"
:
 
"Movie_name"
,
                
"type"
:
 
"string"
            
}
        
]
    
}
,
    
"name"
:
 
"Movie_name-text"
,
    
"type"
:
 
"text"
,
    
"partitioned"
:
 
true
}
See the following example of JSON document that requests a global index creation:
{
    
"index"
:
 
{
        
"fields"
:
 
[
            
{
                
"name"
:
 
"Movie_name"
,
                
"type"
:
 
"string"
            
}
        
]
    
}
,
    
"name"
:
 
"Movie_name-text"
,
    
"type"
:
 
"text"
,
    
"partitioned"
:
 
false
}
See the following example of a JSON document that requests creation of a more complex partitioned index:
{
    
"type"
:
 
"text"
,
    
"name"
:
 
"my-index"
,
    
"ddoc"
:
 
"my-index-design-doc"
,
    
"index"
:
 
{
        
"default_field"
:
 
{
            
"enabled"
:
 
true
,
            
"analyzer"
:
 
"german"
        
}
,
        
"selector"
:
 
{
}
,
        
"fields"
:
 
[
            
{
"name"
:
 
"married"
,
 
"type"
:
 
"boolean"
}
,
            
{
"name"
:
 
"lastname"
,
 
"type"
:
 
"string"
}
,
            
{
"name"
:
 
"year-of-birth"
,
 
"type"
:
 
"number"
}
        
]
    
}
,
    
"partitioned"
:
 
true
}
The 
index
 field
The 
index
 field contains settings specific to text indexes.
To index all fields in all documents automatically, use the simple syntax:
"index"
:
 
{
}
Cloudant
   
277The indexing process traverses all of the fields in all the documents in the database.
In the 
example movies' demo database
, you can see an example of a text index that contains all fields and all documents in a database.
See the following example of a JSON document that requests creation of an index of all fields in all documents:
{
 
"type"
:
 
"text"
,
 
"index"
:
 
{
 
}
}
The 
default_field
 field
The 
default_field
 value specifies how the 
$text
 operator can be used with the index.
The 
default_field
 includes two keys:
Table 5. Default_field field keys
Key
Description
enabled
Enable or disable the 
default_field index
. The default value is 
true
.
The 
analyzer
 key in the 
default_field
 specifies how the index analyzes text. Later, the index can be queried by using the 
$text
 operator. For
more information, see the 
Search documentation
 
for alternative analyzers. You might choose an alternative analyzer when documents are indexed
in languages other than English, or when you have other special requirements for the analyzer, such as matching email addresses.
If the 
default_field
 isn't specified, or is supplied with an empty object, it defaults to 
true
 and the 
standard
 analyzer is used.
The 
fields
 array
The 
fields
 array includes a list of fields that must be indexed for each document. If you know an index queries only on specific fields, then this
field can be used to limit the size of the index. Each field must also specify 
a type to be indexed. The acceptable types are shown in the following list:
"boolean"
"string"
"number"
The 
index_array_lengths
 field
IBM Cloudant Query text indexes have a property that is called 
index_array_lengths
. If the property isn't explicitly set, the default value is 
true
.
If the field is set to 
true
, the index requires extra work. This work contains a scan of every document for any arrays, and creating a field to hold the
length for each array found.
You might prefer to set the 
index_array_lengths
 field to 
false
 in the following situations:
You don't need to know the length of an array.
You don't use the 
$size
 operator.
The documents in your database are complex, or not completely under your control. As a result, it's difficult to estimate the impact of the extra
processing that is needed to determine and store the array lengths.
See the following example JSON document with suggested settings to optimize performance on production systems:
{
 
"default_field"
:
 
{
  
"enabled"
:
 
false
 
}
,
 
"index_array_lengths"
:
 
false
}
 Tip: 
Take care when you index all fields in all documents for large data sets as it might be a resource-consuming activity.
 Tip: 
The 
$size
 operator requires that you set the 
index_array_lengths
 field to 
true
. Otherwise, the operator can't work.
Cloudant
   
278The 
partitioned
 field
This field determines whether the created index is a partitioned or global index.
Table 6. Partitioned field values
Value
Description
Notes
true
Create the index as partitioned.
Can be used only in a partitioned database.
false
Create the index as global.
Can be used in any database.
The default follows the 
partitioned
 setting for the database:
Table 7. Partitioned settings for the database
Is the database partitioned?
Default 
partitioned
 value
Allowed values
Yes
true
true
, 
false
No
false
false
IBM Cloudant Query Parameters
The 
$text
 operator is based on a Lucene search with a standard analyzer. The operator isn't case-sensitive, and matches on any words. However,
the 
$text
 operator doesn't support full Lucene syntax, such as wildcards, 
fuzzy matches, or proximity detection.
For more information, see the 
Search documentation
. The 
$text
 operator applies to all strings found in the document. If you place this operator in
the context of a field 
name, it's invalid.
The 
fields
 array is a list of fields that must be returned for each document. The provided field names can use dotted notation to access subfields.
See the following example JSON document that uses all available query parameters:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gt"
:
 
2010
  
}
 
}
,
 
"fields"
:
 
[
"_id"
,
 
"_rev"
,
 
"year"
,
 
"title"
]
,
 
"sort"
:
 
[
{
"year"
:
 
"asc"
}
]
,
 
"limit"
:
 
10
,
 
"skip"
:
 
0
 
}
Working with indexes
IBM® Cloudant® for IBM Cloud® endpoints can be used to create, list, update, and delete indexes in a database, and to query data by using these
indexes.
Methods
Path
Description
DELETE
/$DATABASE/_index
Delete an index.
GET
/$DATABASE/_index
List all IBM Cloudant Query indexes.
POST
/$DATABASE/_find
Find documents by using a global index.
POST
/$DATABASE/_partition/$PARTITION_KEY/_find
Find documents by using a partitioned index.
 Tip: 
The format of the 
selector
 field is as described in the 
selector syntax
, except for the 
$text
 operator.
Cloudant
   
279Table 1. Available methods and endpoints
POST
/$DATABASE/_index
Create an index.
Creating a partial index
IBM Cloudant Query supports partial indexes by using the 
partial_filter_selector
 field. For more information, see the 
CouchDB documentation
and the original example.
See the following example query:
{
  
"selector"
:
 
{
    
"status"
:
 
{
      
"$ne"
:
 
"archived"
    
}
,
    
"type"
:
 
"user"
  
}
}
Without a partial index, this query requires a full index scan to find all the documents of 
type
:
user
 that don't have a status of 
archived
. This
situation occurs because a normal index can be used to match 
contiguous rows, and the 
$ne
 operator can't guarantee that.
To improve response time, you can create an index that excludes documents with 
status: { $ne: archived }
 at index time by using the
partial_filter_selector
 field that is shown in the following example:
POST /db/_index HTTP/
1.1
Content-Type
:
 application/json
Content-Length
:
 
144
Host
:
 localhost
:
5984
{
  
"index"
:
 
{
    
"partial_filter_selector"
:
 
{
      
"status"
:
 
{
        
"$ne"
:
 
"archived"
      
}
    
}
,
    
"fields"
:
 
[
"type"
]
  
}
,
  
"ddoc"
 
:
 
"type-not-archived"
,
  
"type"
 
:
 
"json"
}
Partial indexes aren't currently used by the query planner unless specified by a 
use_index
 field, so you must modify the original query:
{
  
"selector"
:
 
{
    
"status"
:
 
{
      
"$ne"
:
 
"archived"
    
}
,
    
"type"
:
 
"user"
  
}
,
  
"use_index"
:
 
"type-not-archived"
}
Technically, you don't need to include the filter on the 
status
 field in the query selector. The partial index ensures that this value is always true.
However, if you include the filter, it makes the intent of the selector clearer. 
It also makes it easier to take advantage of future improvements to
query planning (for example, automatic selection of partial indexes).
Creating selector expressions
 Tip: 
The 
partial_filter_selector
 field replaces the 
selector
 field, previously only valid in text indexes. The 
selector
 field is still
compatible with an earlier version for text indexes only.
Cloudant
   
280In general, whenever you have an operator that takes an argument, that argument can itself be another operator with arguments of its own. This
expansion enables more complex selector expressions.
Combination or array logical operators, such as 
$regex
, can result in a full database scan when you use indexes of type JSON, resulting in poor
performance. Only equality operators, such as 
$eq
, 
$gt
, 
$gte
, 
$lt
, and 
$lte
 (but not 
$ne
), enable index lookups. To ensure that indexes are
used effectively, analyze the 
explain plan
 for each query.
Most selector expressions work exactly as you would expect for the operator. The matching algorithms that are used by the 
$regex
 operator are
currently 
based
 on the 
Perl Compatible Regular Expression (PCRE) library
. However, not all of the PCRE library is implemented. Additionally, some
parts of the 
$regex
 operator go beyond what PCRE offers. For more information 
about what is implemented, see the 
Erlang Regular Expression
information.
Sort syntax
The 
sort
 field contains a list of field name and direction pairs, expressed as a basic array. The first field name and direction pair are the topmost-
level of sort. Further pairs, if provided, specify the next level of sort.
The sort field can be any field. Use dotted notation if needed for subfields.
The direction value is 
asc
 for ascending, and 
desc
 for descending.
See the following example of simple sort syntax:
[
 
{
  
"fieldName1"
:
 
"desc"
 
}
,
 
{
  
"fieldName2"
:
 
"desc"
 
}
]
See the following example of simple sort, assuming default direction of "ascending" for both fields:
[
 
"fieldNameA"
,
 
"fieldNameB"
]
A typical requirement is to search for some content by using a selector, then to sort the results according to the specified field, in the direction
preferred.
To use sorting, an index containing the sort fields must be defined. If using 
json
 index, the fields must be specified in the same order as the sort.
If the direction is ascending, you can use a string instead of an object to specify the sort fields.
For field names in sort queries against a 
text
 index where the type of the field being sorted cannot be determined, it may be necessary for a field
type to be specified. For example:
{
 
"<fieldname>:string"
:
 
"asc"
}
Which index is used
by query?
Field type requirement
JSON index
None
 Tip: 
If you exclude the direction value, the default 
asc
 is used.
 Tip: 
Currently, IBM Cloudant Query doesn't support multiple fields with different sort orders, so the direction must either be all ascending or
all descending.
Cloudant
   
281Table 1. When to specify the field type
Text index of all
fields in all
documents
Specify the sort field in the query if the database contains documents where the sort field has one type. Also, specify
the sort field in the query if it contains documents where the sort field has a different type.
Any other text index
Specify the type of all sort fields in the query.
The sorting order is undefined when fields contain different data types. This characteristic is an important difference between text and view indexes.
Sorting behavior for fields with different data types might change in future versions.
See the following example of a simple query that uses sorting:
{
 
"selector"
:
 
{
  
"Actor_name"
:
 
"Robert De Niro"
 
}
,
 
"sort"
:
 
[
  
{
   
"Actor_name"
:
 
"asc"
  
}
,
  
{
   
"Movie_runtime"
:
 
"asc"
  
}
 
]
}
Filtering fields
It's possible to specify exactly which fields are returned for a document when you select from a database. The two advantages are shown in the
following list:
Your results are limited to only those parts of the document that are needed for your application.
A reduction in the size of the response.
The fields to be returned are specified as an array.
See the following example of selective retrieval of fields from matching documents:
{
 
"selector"
:
 
{
  
"Actor_name"
:
 
"Robert De Niro"
 
}
,
 
"fields"
:
 
[
  
"Actor_name"
,
  
"Movie_year"
,
  
"_id"
,
  
"_rev"
 
]
}
Pagination
IBM Cloudant Query supports pagination by the bookmark field. Every 
_find
 response contains a bookmark - a token that IBM Cloudant uses to
determine where to resume from when later queries are made. To get the next set of query 
results, add the bookmark that was received in the
previous response to your next request. Remember to keep the selector the same, otherwise you receive unexpected results. To paginate
backwards, you can use a previous bookmark to return the 
previous set of results.
 Tip: 
A text index of all fields in all documents is created when you use the syntax: 
"index": {}
.
 Tip: 
Only the specified filter fields are included in the response. 
_id
 or other metadata fields aren't automatically included.
 Tip: 
The presence of a bookmark doesn’t guarantee more results. You can test whether you are at the end of the result set by comparing the
number of results that are returned with the page size requested. If the results returned are less than limit, 
no more results were returned in
Cloudant
   
282Explain plans
IBM Cloudant Query chooses which index to use for responding to a query, unless you specify an index at query time.
When you specify an index to use, IBM Cloudant Query uses the following logic:
The query planner looks at the selector section, and finds the index with the closest match to operators and fields that are used in the query. If
two or more JSON type indexes match, the index with the smallest number of fields in the index 
is preferred. If two or more candidate indexes
still exist, the index with the first alphabetical name is chosen.
If a 
json
 type index 
and
 a 
text
 type index might both satisfy a selector, the 
json
 index is chosen by default.
The 
text
 type index is chosen when the following conditions are met:
A 
json
 type index 
and
 a 
text
 type index exist in the same field (for example 
fieldone
).
The selector can be satisfied only by using a 
text
 type index.
For example, assume that you have a 
text
 type index and a 
json
 type index for the field 
foo
, and you want to use a selector similar to the
following sample:
{
 
"foo"
:
 
{
  
"$in"
:
 
[
"red"
,
"blue"
,
"green"
]
 
}
}
IBM Cloudant Query uses the 
text
 type index because a 
json
 type index can't satisfy the selector.
However, you might use a different selector with the same indexes:
{
 
"foo"
:
 
{
  
"$gt"
:
 
2
 
}
}
In this example, IBM Cloudant Query uses the 
json
 type index because both types of indexes can satisfy the selector.
To identify which index is being used by a particular query, send a 
POST
 to the 
_explain
 endpoint for the database, with the query as data. The
details of the index in use are shown in the 
index
 object 
within the result.
See the following example that uses HTTP to show how to identify the index that was used to answer a query:
POST
 
/movies/_explain
 
HTTP/1.1
Host
: 
$SERVICE_URL
Content-Type
: 
application/json
{
 "selector": {
  "$text": "Pacino",
  "year": 2010
 }
}
See the following example that uses the command line to show how to identify the index that was used to answer a query:
Curl
curl 
"
$SERVICE_URL
/movies/_explain"
 \
 -X POST \
 -H 
"Content-Type: application/json"
 \
 -d 
'{
  "selector": {
   "$text": "Pacino",
   "year": 2010
  }
 }'
the result set.
Cloudant
   
283Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ExplainResult;
import
 com.ibm.cloud.cloudant.v1.model.PostExplainOptions;
import
 java.util.HashMap;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = 
new
 
HashMap
<>();
selector.put(
"$text"
, 
"Pacino"
);
selector.put(
"year"
, 
2010
);
PostExplainOptions
 
explainOptions
 
=
    
new
 
PostExplainOptions
.Builder()
        .db(
"movies"
)
        .selector(selector)
        .build();
ExplainResult
 
response
 
=
    service.postExplain(explainOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
let
 
selector
: 
Cloudant
V1.
Selector
 = {
    
'$text'
: 
'Pacino'
,
    
'year'
: 
2010
};
service.
postExplain
({
  
db
: 
'movies'
,
  
selector
: selector
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_find(
  db=
'movies'
,
  selector={
'$text'
: 
'Pacino'
, 
'year'
: 
2010
}
).get_result()
print
(response)
Go
postExplainOptions := service.NewPostExplainOptions(
    
"movies"
,
    
map
[
string
]
interface
{}{
        
"$text"
: 
"Pacino"
,
        
"year"
:  
2010
,
    },
)
explainResult, _, err := service.PostExplain(postExplainOptions)
Cloudant
   
284if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(explainResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example response that shows which index was used to answer a query:
{
 
"dbname"
:
 
"$ACCOUNT/movies"
,
 
"index"
:
 
{
  
"ddoc"
:
 
"_design/32372935e14bed00cc6db4fc9efca0f1537d34a8"
,
  
"name"
:
 
"32372935e14bed00cc6db4fc9efca0f1537d34a8"
,
  
"type"
:
 
"text"
,
  
"def"
:
 
{
   
"default_analyzer"
:
 
"keyword"
,
   
"default_field"
:
 
{
}
,
   
"selector"
:
 
{
}
,
   
"fields"
:
 
[
]
  
}
 
}
,
 
"selector"
:
 
{
  
"$and"
:
 
[
   
{
    
"$default"
:
 
{
     
"$text"
:
 
"Pacino"
    
}
   
}
,
   
{
    
"year"
:
 
{
     
"$eq"
:
 
2010
    
}
   
}
  
]
 
}
,
 
"opts"
:
 
{
  
"use_index"
:
 
[
]
,
  
"bookmark"
:
 
[
]
,
  
"limit"
:
 
10000000000
,
  
"skip"
:
 
0
,
  
"sort"
:
 
{
}
,
  
"fields"
:
 
"all_fields"
,
  
"r"
:
 
[
   
49
  
]
,
  
"conflicts"
:
 
false
 
}
,
 
"limit"
:
 
200
,
 
"skip"
:
 
0
,
 
"fields"
:
 
"all_fields"
,
 
"query"
:
 
"(($default:Pacino) AND (year_3anumber:2010))"
,
 
"sort"
:
 
"relevance"
}
To instruct a query to use a specific index, add the 
use_index
 parameter to the query.
The value of the 
use_index
 parameter takes one of the following formats:
Cloudant
   
285"use_index": "$DDOC"
"use_index": ["$DDOC","$INDEX_NAME"]
See the following example query with instructions to use a specific index:
{
 
"selector"
:
 
{
  
"$text"
:
 
"Pacino"
,
  
"year"
:
 
2010
 
}
,
 
"use_index"
:
 
"_design/32372935e14bed00cc6db4fc9efca0f1537d34a8"
}
Selector syntax
The IBM® Cloudant® for IBM Cloud® Query language is expressed as a JSON object that describes documents of interest. Within this structure, you
can apply conditional logic by using specially named fields.
The IBM Cloudant Query language has some similarities with MongoDB query documents, but these similarities arise from a commonality of purpose
and don't necessarily extend to equivalence of function or result.
Selector basics
Elementary selector syntax requires you to specify one or more fields, and the corresponding values needed for those fields. The following example
selector matches all documents that have a 
director
 field that contains the value 
Lars von Trier
.
See the following example of a simple selector:
{
 
"selector"
:
 
{
  
"director"
:
 
"Lars von Trier"
 
}
}
If you created a full text index by specifying 
"type":"text"
 when the index was created, you can use the 
$text
 operator to select matching
documents. In the following example, the full text index 
is inspected to find any document that contains the word 
Bond
.
See the following example of a simple selector for a full_text index:
{
 
"selector"
:
 
{
  
"$text"
:
 
"Bond"
 
}
}
You can create more complex selector expressions by combining operators. However, for IBM Cloudant Query indexes of type 
json
, you can't use
"combination" or "array logical" operators such as 
$regex
 
as the 
basis
 of a query. Only the equality operators such as 
$eq
, 
$gt
, 
$gte
, 
$lt
, and
$lte
 - but 
not
 
$ne
 - can be used as the basis of a more complex query. For more information about creating complex selector expressions, see
Creating selector expressions
.
Selector with two fields
In the following example, the selector matches any document with a 
name
 field that contains 
Paul
, 
and
 that also has a 
location
 field with the
value "Boston".
See the following example of a more complex selector:
{
 
"selector"
:
 
{
  
"name"
:
 
"Paul"
,
  
"location"
:
 
"Boston"
 
}
}
Cloudant
   
286Subfields
Use a more complex selector to specify the values for a field of nested objects, or subfields. For example, you might use a standard JSON structure
for specifying a field 
and
 a subfield.
See the following example of a field and subfield selector within a JSON object:
{
 
"selector"
:
 
{
  
"imdb"
:
 
{
   
"rating"
:
 
8
  
}
 
}
}
An abbreviated equivalent uses a dot notation to combine the field and subfield names into a single name.
See the following example of an equivalent field and subfield selector that uses dot notation:
{
 
"selector"
:
 
{
  
"imdb.rating"
:
 
8
 
}
}
IBM Cloudant Operators
Operators are identified by the use of a dollar sign (
$
) prefix in the name field.
The selector syntax has two core types of operators:
Combination operators
Condition operators
In general, combination operators are applied at the topmost level of selection. They're used to combine conditions, or to create combinations of
conditions, into one selector.
Every explicit operator has the form:
{
 
"$operator"
:
 
"argument"
}
A selector without an explicit operator is considered to have an implicit operator. The exact implicit operator is determined by the structure of the
selector expression.
Implicit operators
The two implicit operators are shown in the following list:
"Equality"
"And"
In a selector, any field that contains a JSON value, but that has no operators in it, is considered to be an equality condition. The implicit equality test
also applies for fields and subfields.
Any JSON object that isn't the argument to a condition operator is an implicit 
$and
 operator on each field.
See the following example selector that uses an operator to match any document, where the 
year
 field has a value greater than 2010:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gt"
:
 
2010
  
}
 
}
}
Cloudant
   
287In the following example, a matching document must have a field that is called 
director
, 
and
 the field must have a value exactly equal to 
Lars
von Trier
.
See the following example of the implicit equality operator:
{
 
"director"
:
 
"Lars von Trier"
}
You can also make the equality operator explicit, as shown in the following example.
See the following example of an explicit equality operator:
{
 
"director"
:
 
{
  
"$eq"
:
 
"Lars von Trier"
 
}
}
In the following example that uses subfields, the field 
imdb
 in a matching document 
must
 also have a subfield 
rating
, 
and
 the subfield 
must
 have
a value equal to 8.
See the following example of implicit operator that is applied to a subfield test:
{
 
"imdb"
:
 
{
  
"rating"
:
 
8
 
}
}
You can make the equality operator explicit.
See the following example of an explicit equality operator:
{
 
"selector"
:
 
{
  
"imdb"
:
 
{
   
"rating"
:
 
{
 
"$eq"
:
 
8
 
}
  
}
 
}
}
See the following example of a 
$eq
 operator that is used with full text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$eq"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"title"
 
]
}
See the following example of an 
$eq
 operator that is used with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$eq"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
Cloudant
   
288 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
In the following example, the field 
director
 must be present and contain the value 
Lars von Trier
 
and
 the field 
year
 must exist and have the
value 
2003
.
See the following example of an implicit 
$and
 operator:
{
 
"director"
:
 
"Lars von Trier"
,
 
"year"
:
 
2003
}
You can make both the 
$and
 operator and the equality operator explicit.
See the following example that uses explicit 
$and
 and 
$eq
 operators:
{
 
"$and"
:
 
[
  
{
   
"director"
:
 
{
    
"$eq"
:
 
"Lars von Trier"
   
}
  
}
,
  
{
   
"year"
:
 
{
    
"$eq"
:
 
2003
   
}
  
}
 
]
}
Explicit operators
All operators, apart from the 
$eq
 (equality) and 
$and
 (and) operators, must be stated explicitly.
Combination operators
Combination operators are used to combine selectors. Three combination operators (
$all
, 
$allMatch
, and 
$elemMatch
) help you work with
JSON arrays, in addition to the common Boolean operators found in most 
programming languages.
A combination operator takes a single argument. The argument is either another selector, or an array of selectors.
Table 1. Combination operators
Operator
Argument
Purpose
$all
Array
Matches an array value if it contains all the elements of the argument array.
$allMatch
Selector
Matches and returns all documents that contain an array field, where all the elements match all the specified
query criteria.
$and
Array
Matches if all the selectors in the array match.
$elemMatch
Selector
Matches and returns all documents that contain an array field with at least one element that matches all the
specified query criteria.
$nor
Array
Matches if none of the selectors in the array match.
$not
Selector
Matches if the selector doesn't match.
$or
Array
Matches if any of the selectors in the array match. All selectors must use the same index.
Cloudant
   
289Examples of combination operators
The 
$all
 operator
The 
$all
 operator matches an array value if it contains 
all
 the elements of the argument array.
See the following example that uses the 
$all
 operator:
{
 
"selector"
:
 
{
  
"genre"
:
 
{
   
"$all"
:
 
[
"Comedy"
,
"Short"
]
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"genre"
 
]
,
 
"limit"
:
 
10
}
The 
$allMatch
 operator
The 
$allMatch
 operator matches and returns all documents that contain an array field, where all the elements in the array field match the supplied
query criteria.
See the following example that uses the 
$allMatch
 operator:
{
    
"genre"
:
 
{
        
"$allMatch"
:
 
{
          
"$eq"
:
 
"Horror"
        
}
    
}
}
The 
$and
 operator
The 
$and
 operator matches if all the selectors in the array match.
See the following example that uses the 
$and
 operator:
{
    
"selector"
:
 
{
        
"$and"
:
 
[
            
{
                
"year"
:
 
{
                    
"$in"
:
 
[
2014
,
 
2015
]
                
}
            
}
,
            
{
                
"genre"
:
 
{
                     
"$all"
:
 
[
"Comedy"
,
"Short"
]
                 
}
            
}
        
]
    
}
,
    
"fields"
:
 
[
        
"year"
,
        
"_id"
,
        
"title"
    
]
,
    
"limit"
:
 
10
}
The 
$elemMatch
 operator
Cloudant
   
290The 
$elemMatch
 operator matches and returns all documents that contain an array field with at least one element that matches the supplied query
criteria.
See the following example that uses the 
$elemMatch
 operator:
{
 
"selector"
:
 
{
  
"genre"
:
 
{
   
"$elemMatch"
:
 
{
    
"$eq"
:
 
"Horror"
   
}
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"genre"
 
]
,
 
"limit"
:
 
10
}
The 
$nor
 operator
The 
$nor
 operator matches if the selector does 
not
 match.
See the following example that uses the 
$nor
 operator:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gte"
:
 
1900
,
   
"$lte"
:
 
1910
  
}
,
  
"$nor"
:
 
[
   
{
 
"year"
:
 
1901
 
}
,
   
{
 
"year"
:
 
1905
 
}
,
   
{
 
"year"
:
 
1907
 
}
  
]
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"year"
 
]
}
The 
$not
 operator
The 
$not
 operator matches if the selector does 
not
 resolve to a value of 
true
.
See the following example that uses the 
$not
 operator:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gte"
:
 
1900
,
   
"$lte"
:
 
1903
  
}
,
  
"$not"
:
 
{
   
"year"
:
 
1901
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"year"
 
]
}
The 
$or
 operator
The 
$or
 operator matches if any of the selectors in the array match.
Cloudant
   
291See the following example that uses the 
$or
 operator:
{
 
"selector"
:
 
{
  
"year"
:
 
1977
,
  
"$or"
:
 
[
   
{
 
"director"
:
 
"George Lucas"
 
}
,
   
{
 
"director"
:
 
"Steven Spielberg"
 
}
  
]
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"director"
,
  
"year"
 
]
}
Condition operators
Condition operators are specific to a field, and are used to evaluate the value that is stored in that field. For instance, the 
$eq
 operator matches
when the specified field contains a value that is equal to the supplied argument.
The basic equality and inequality operators common to most programming languages are supported. Some "meta" condition operators are also
available.
Some condition operators accept any valid JSON content as the argument. Other condition operators require the argument to be in a specific JSON
format.
Operator
type
Operator
Argument
Purpose
(In) equality
$lt
Any JSON
The field is less than the argument.
$lte
Any JSON
The field is less than or equal to the argument.
$eq
Any JSON
The field is equal to the argument.
$ne
Any JSON
The field isn't equal to the argument.
$gte
Any JSON
The field is greater than or equal to the argument.
$gt
Any JSON
The field is greater than the argument.
Object
$exists
Boolean
Check whether the field exists or not, no matter what its value is.
$type
String
Check the document field's type. Accepted values are 
null
, 
boolean
, 
number
, 
string
, 
array
,
and 
object
.
Array
$in
Array of
JSON
values
The document field must exist in the list provided.
$nin
Array of
JSON
values
The document field must not exist in the list provided.
$size
Integer
Special condition to match the length of an array field in a document. Non-array fields can't
match this condition.
Miscellaneous
$mod
[Divisor,
Remainder]
Divisor and Remainder are both positive or negative integers. Non-integer values result in a
404 status
. Matches documents where the expression (
field % Divisor == Remainder
) 
is
true, and only when the document field is an integer.
Cloudant
   
292Table 2. Condition operator argument requirements
$regex
String
A regular expression pattern to match against the document field. Matches only when the field
is a string value and matches the supplied regular expression.
Examples of condition operators
The 
$lt
 operator
The 
$lt
 operator matches if the specified field content is less than the argument.
See the following example that uses the 
$lt
 operator with full-text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$lt"
:
 
1900
  
}
 
}
,
 
"sort"
:
 
[
  
"year:number"
,
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"year"
,
  
"title"
 
]
}
See the following example that uses the 
$lt
 operator with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$lt"
:
 
1900
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
The 
$lte
 operator
The 
$lte
 operator matches if the specified field content is less than or equal to the argument.
See the following example that uses the 
$lte
 operator with full-text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$lte"
:
 
1900
  
}
 
}
,
 
"sort"
:
 
[
  
"year:number"
,
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"year"
,
  
"title"
 Tip: 
Regular expressions don't work with indexes, so they must not be used to filter large data sets. However, they can be used to restrict a
partial index <find/partial_indexes>
.
Cloudant
   
293 
]
}
See the following example that uses the 
$lte
 operator with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$lte"
:
 
1900
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
The 
$eq
 operator
The 
$eq
 operator matches if the specified field content is equal to the supplied argument.
See the following example that uses the 
$eq
 operator with full-text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$eq"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"title"
 
]
}
See the following example that uses the 
$eq
 operator with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$eq"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
The 
$ne
 operator
The 
$ne
 operator matches if the specified field content isn't equal to the supplied argument.
See the following example that uses the 
$ne
 operator with full-text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$ne"
:
 
1892
 Tip: 
The 
$ne
 operator can't be the basic (lowest level) element in a selector when you use an index of type 
json
.
Cloudant
   
294  
}
 
}
,
 
"fields"
:
 
[
  
"year"
 
]
,
 
"sort"
:
 
[
  
"year:number"
 
]
}
See the following example that uses the 
$ne
 operator with a primary index:
{
 
"selector"
:
 
{
 
"year"
:
 
{
   
"$ne"
:
 
1892
  
}
 
}
,
 
"fields"
:
 
[
  
"year"
 
]
,
 
"limit"
:
 
10
}
The 
$gte
 operator
The 
$gte
 operator matches if the specified field content is greater than or equal to the argument.
See the following example that uses the 
$gte
 operator with full-text indexing:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gte"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year:number"
,
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"year"
,
  
"title"
 
]
}
See the following example that uses the 
$gte
 operator with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gte"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
The 
$gt
 operator
The 
$gt
 operator matches if the specified field content is greater than the argument.
See the following example that uses the 
$gt
 operator with full-text indexing:
{
Cloudant
   
295 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gt"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year:number"
,
  
"title:string"
 
]
,
 
"fields"
:
 
[
  
"year"
,
  
"title"
 
]
}
See the following example that uses the 
$gt
 operator with a database that is indexed on the field 
year
:
{
 
"selector"
:
 
{
  
"year"
:
 
{
   
"$gt"
:
 
2001
  
}
 
}
,
 
"sort"
:
 
[
  
"year"
 
]
,
 
"fields"
:
 
[
  
"year"
 
]
}
The 
$exists
 operator
The 
$exists
 operator matches if the field exists, no matter what its value is.
See the following example that uses the 
$exists
 operator:
{
 
"selector"
:
 
{
  
"year"
:
 
2015
,
  
"title"
:
 
{
   
"$exists"
:
 
true
  
}
 
}
,
 
"fields"
:
 
[
  
"year"
,
  
"_id"
,
  
"title"
 
]
}
The 
$type
 operator
The 
$type
 operator requires that the specified document field is of the correct type.
See the following example that uses the 
$type
 operator:
{
 
"selector"
:
 
{
    
"year"
:
 
{
   
"$type"
:
 
"number"
  
}
 
}
,
 
"fields"
:
 
[
  
"year"
,
  
"_id"
,
  
"title"
 
]
}
Cloudant
   
296The 
$in
 operator
The 
$in
 operator requires that the document field 
must
 exist in the list provided.
See the following example that uses the 
$in
 operator:
{
 
"selector"
:
 
{
    
"year"
:
 
{
   
"$in"
:
 
[
2010
,
 
2015
]
  
}
 
}
,
 
"fields"
:
 
[
  
"year"
,
  
"_id"
,
  
"title"
 
]
,
 
"limit"
:
 
10
}
The 
$nin
 operator
The 
$nin
 operator requires that the document field must 
not
 exist in the list provided.
See the following example that uses the 
$nin
 operator:
{
 
"selector"
:
 
{
    
"year"
:
 
{
   
"$nin"
:
 
[
2010
,
 
2015
]
  
}
 
}
,
 
"fields"
:
 
[
  
"year"
,
  
"_id"
,
  
"title"
 
]
,
 
"limit"
:
 
10
}
The 
$size
 operator
The 
$size
 operator matches the length of an array field in a document.
See the following example that uses the 
$size
 operator:
{
 
"selector"
:
 
{
    
"genre"
:
 
{
   
"$size"
:
 
4
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"genre"
 
]
,
 
"limit"
:
 
25
}
The 
$mod
 operator
The 
$mod
 operator matches documents where the expression (
field % Divisor == Remainder
) is true, and only when the document field is an
integer. The Divisor and Remainder must be integers. They can be positive or 
negative integers. A query where the Divisor or Remainder is a non-
integer returns a 
404 status
.
 Tip: 
When you use negative integer values for the Divisor or Remainder, the IBM® Cloudant® for IBM Cloud® 
$mod
 operator uses 
truncated
division
. 
Both the 
Erlang 
rem
 modulo operator
, and the 
%
 operator in C
, behave in a similar way.
Cloudant
   
297See the following example that uses the 
$mod
 operator:
{
 
"selector"
:
 
{
          
"year"
:
 
{
   
"$mod"
:
 
[
100
,
0
]
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"year"
 
]
,
 
"limit"
:
 
50
}
The 
$regex
 operator
The 
$regex
 operator matches when the field is a string value 
and
 matches the supplied regular expression.
See the following example that uses the 
$regex
 operator:
{
 
"selector"
:
 
{
     
"cast"
:
 
{
   
"$elemMatch"
:
 
{
    
"$regex"
:
 
"^Robert"
   
}
  
}
 
}
,
 
"fields"
:
 
[
  
"title"
,
  
"cast"
 
]
,
 
"limit"
:
 
10
}
More about 
text
 indexes
The basic premise for full text indexes is that a document is "expanded" into a list of 
key:value
 pairs that are indexed by Lucene. This expansion
enables the use of Lucene's search syntax as a basis for the query capability.
This technique supports enhanced searches, but does have certain limitations. For example, it might not always be clear whether content for an
expanded document came from individual elements or an array.
The query mechanism resolves this uncertainty by preferring to return "false positive" results. In other words, if a match was found because of a
search for either an individual element, or an element from an array, then the match is 
considered a success.
Selector conversion
A standard Lucene search expression might not fully implement the wanted JSON-based IBM Cloudant query syntax. Therefore, a conversion
between the two formats takes place.
In the following example, the JSON query approximates to the English phrase, 
Match if the age expressed as a number is greater than five and less
than or equal to infinity.
 The Lucene query corresponds to that phrase, where the text 
_3a
 within the field name corresponds to the 
age:number
field, and is an example of the document content expansion that was mentioned earlier.
See the following example query to be converted:
{
 
"age"
:
 
{
  
"$gt"
:
 
5
 
}
}
 Tip: 
Like IBM® Cloudant® for IBM Cloud® Search indexes, IBM Cloudant Query indexes of 
type: text
 are limited to 200 results when
queried.
Cloudant
   
298The corresponding Lucene query
(
age_3anumber
:{
5
 
TO
 
Infinity
])
A more complex example
The following example illustrates some important points.
JSON query to be converted to Lucene
{
 
"$or"
:
 
[
  
{
   
"age"
:
 
{
    
"$gt"
:
 
5
   
}
  
}
,
  
{
   
"twitter"
:
 
{
    
"$exists"
:
true
   
}
  
}
,
  
{
   
"type"
:
 
{
    
"$in"
:
 
[
     
"starch"
,
     
"protein"
    
]
   
}
  
}
 
]
}
The first part of the JSON query is straightforward to convert to Lucene; the test determines whether the 
age
 field has a numerical value greater
than 5. The 
{
 character in the range expression means that the value 
5 isn't considered a match.
To implement the 
"twitter": {"$exists":true}
 part of the JSON query in Lucene, the first test is to determine whether a 
twitter
 field exists.
However, the field might be either an array or an object, 
so the match must succeed when the value is an array 
or
 an object.
This requirement means that the 
$fieldnames
 field must have entries that contain either 
twitter.*
 or 
twitter:*
. The 
.
 character is
represented in the query as the ASCII character sequence 
_2e
. Similarly, the 
:
 character is represented in the query as the ASCII character
sequence 
_3a
. This representation requires the use of a two clause 
OR
 query for the 
twitter
 
field, ending in 
_2e*
 and 
_3a*
. Implementing
this query as two phrases instead of a single 
twitter*
 query prevents an accidental match with a field name such as 
twitter_handle
 or similar.
The last of the three main clauses are a search for 
starch
 or 
protein
. This search is more complicated. The 
$in
 operator has some special
semantics for array values that are inherited from the way MongoDB 
behaves. In particular, the 
$in
 operator applies to the value 
or
 any of the
values that are contained in an array that is named by the field. In this example, the expression means that both 
"type":"starch"
 
and
 
"type":
["protein"]
 would match the example argument to 
$in
. Earlier, the 
type_3astring
 expression was converted to 
type:string
. The second
type_2e_5b_5d_3astring
 
phrase converts to 
type.[]:string
, which is an example of the expanded array indexing.
Corresponding Lucene query explained
The "#" comments aren't valid Lucene syntax, but help explain the query construction.
(
 # 
Search
 
for
 age > 
5
 (
age_3anumber
:{
5
 
TO
 
Infinity
])
 # 
Search
 
for
 documents that contain the twitter field
 ((
$fieldnames
:twitter_2e*) 
OR
 (
$fieldnames
:twitter_3a*))
 # 
Search
 
for
 type = starch
 (
  ((
type_3astring
:starch) 
OR
 (
type_2e_5b_5d_3astring
:starch))
  # 
Search
 
for
 type = protein
Cloudant
   
299  ((
type_3astring
:protein) 
OR
 (
type_2e_5b_5d_3astring
:protein))
 )
)
Movies demo database example
The following example uses HTTP to create a 
text
 index for your sample database.
POST
 
/my-movies/_index
 
HTTP/1.1
Host
: 
$SERVICE_URL
Content-Type
: 
application/json
{
 "index": {},
 "type": "text"
}
See the following example that uses the command line to create a 
text
 index for your sample database:
Curl
curl 
"
$SERVICE_URL
/my-movies/_index"
 \
 -X POST \
 -H 
"Content-Type: application/json"
 \
 -d 
'{"index": {}, "type": "text"}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.IndexDefinition;
import
 com.ibm.cloud.cloudant.v1.model.IndexResult;
import
 com.ibm.cloud.cloudant.v1.model.PostIndexOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
IndexDefinition
 
indexDefinition
 
=
 
new
 
IndexDefinition
.Builder()
   .build();
PostIndexOptions
 
indexOptions
 
=
 
new
 
PostIndexOptions
.Builder()
    .db(
"my-movies"
)
    .index(indexDefinition)
    .type(
"text"
)
    .build();
IndexResult
 
response
 
=
    service.postIndex(indexOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
let
 
index
: 
Cloudant
V1.
IndexDefinition
 = {}
service.
postIndex
({
  
db
: 
'my-movies'
,
  
index
: index,
  
type
: 
'text'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
Cloudant
   
300from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, IndexDefinition
service = CloudantV1.new_instance()
index = IndexDefinition()
response = service.post_index(
  db=
'my-movies'
,
  index=index,
  
type
=
'text'
).get_result()
print
(response)
Go
postIndexOptions := service.NewPostIndexOptions(
    
"my-movies"
,
    &cloudantv1.IndexDefinition{},
)
postIndexOptions.SetType(
"text"
)
indexResult, _, err := service.PostIndex(postIndexOptions)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(indexResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example response after a 
text
 index is created successfully:
{
    
"id"
:
 
"_design/bf936ad6eb87f03c2b42ae153377462844575e40"
,
    
"name"
:
 
"bf936ad6eb87f03c2b42ae153377462844575e40"
,
 
"result"
:
 
"created"
}
The most obvious difference in the results you get when you use full text indexes is the inclusion of a large 
bookmark
 field. The reason is that 
text
indexes are different from view-based indexes. For more flexibility, 
when you work with the results that are obtained from a full text query, you can
supply the 
bookmark
 value as part of the request body. Use the 
bookmark
 to specify which page of results you require.
See the following example that uses HTTP to search for a specific document within the database:
POST
 
/my-movies/_find
 
HTTP/1.1
Host
: 
$SERVICE_URL
Content-Type
: 
application/json
{
  "selector": {
    "Person_name":"Zoe Saldana"
  }
}
See the following example that uses the command line to search for a specific document within the database:
 Tip: 
The actual 
bookmark
 value is long, so the examples here have values that are truncated for reasons of clarity.
Cloudant
   
301Curl
curl -X POST -H 
"Content-Type: application/json"
 \
 
"
$SERVICE_URL
/my-movies/_find"
 \
 -d 
'{"selector": {"Person_name":"Zoe Saldana"}}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostFindOptions;
import
 java.util.Collections;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = Collections.singletonMap(
    
"Person_name"
, 
"Zoe Saldana"
);
PostFindOptions
 
findOptions
 
=
 
new
 
PostFindOptions
.Builder()
    .db(
"my-movies"
)
    .selector(selector)
    .build();
FindResult
 
response
 
=
    service.postFind(findOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
let
 
selector
: 
Cloudant
V1.
JsonObject
 = {
  
Person
_name
: 
'Zoe Saldana'
};
service.
postFind
({
  
db
: 
'my-movies'
,
  
selector
: selector,
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_find(
  db=
'my-movies'
,
  selector={
'Person_name'
: 
'Zoe Saldana'
}
).get_result()
print
(response)
Go
postFindOptions := service.NewPostFindOptions(
    
"my-movies"
,
    
map
[
string
]
interface
{}{
        
"Person_name"
: 
"Zoe Saldana"
,
    },
Cloudant
   
302)
findResult, _, err := service.PostFind(postFindOptions)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example result from the search:
{
 
"docs"
:
 
[
  
{
   
"_id"
:
 
"d9e6a7ae2363d6cfe81af75a3941110b"
,
   
"_rev"
:
 
"1-556aec0e89fa13769fbf59d651411528"
,
   
"Movie_runtime"
:
 
162
,
   
"Movie_rating"
:
 
"PG-13"
,
   
"Person_name"
:
 
"Zoe Saldana"
,
   
"Movie_genre"
:
 
"AVYS"
,
   
"Movie_name"
:
 
"Avatar"
,
   
"Movie_earnings_rank"
:
 
"1"
,
   
"Person_pob"
:
 
"New Jersey, USA"
,
   
"Movie_year"
:
 
2009
,
   
"Person_dob"
:
 
"1978-06-19"
  
}
 
]
,
 
"bookmark"
:
 
"g2wA ... Omo"
}
See the following example that uses HTTP for a slightly more complex search:
POST
 
/my-movies/_find
 
HTTP/1.1
Host
: 
$SERVICE_URL
Content-Type
: 
application/json
{
 "selector": {
  "Person_name":"Robert De Niro",
  "Movie_year": 1978
 }
}
See the following example that uses the command line for a slightly more complex search:
Curl
curl -X POST -H 
"Content-Type: application/json"
 \
 
"
$SERVICE_URL
/my-movies/_find"
 \
 -d 
'{"selector": {"Person_name":"Robert De Niro", "Movie_year": 1978}}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostFindOptions;
import
 java.util.HashMap;
Cloudant
   
303import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = 
new
 
HashMap
<>();
selector.put(
"Person_name"
, 
"Robert De Niro"
);
selector.put(
"Movie_year"
, 
1978
);
PostFindOptions
 
findOptions
 
=
 
new
 
PostFindOptions
.Builder()
    .db(
"my-movies"
)
    .selector(selector)
    .build();
FindResult
 
response
 
=
    service.postFind(findOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
let
 
selector
: 
Cloudant
V1.
JsonObject
 = {
  
Person
_name
: 
'Robert De Niro'
,
  
Movie
_year
: 
1978
};
service.
postFind
({
  
db
: 
'my-movies'
,
  
selector
: selector,
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_find(
  db=
'my-movies'
,
  selector={
'Person_name'
: 
'Robert De Niro'
, 
'Movie_year'
: 
1978
}
).get_result()
print
(response)
Go
postFindOptions := service.NewPostFindOptions(
    
"my-movies"
,
    
map
[
string
]
interface
{}{
        
"Person_name"
: 
"Robert De Niro"
,
        
"Movie_year"
: 
1978
,
    },
)
findResult, _, err := service.PostFind(postFindOptions)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Cloudant
   
304Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example result from the search:
{
 
"docs"
:
 
[
  
{
   
"_id"
:
 
"d9e6a7ae2363d6cfe81af75a392eb9f2"
,
   
"_rev"
:
 
"1-9faa75d7ea524448b1456a6c69a4391a"
,
   
"Movie_runtime"
:
 
183
,
   
"Movie_rating"
:
 
"R"
,
   
"Person_name"
:
 
"Robert De Niro"
,
   
"Movie_genre"
:
 
"DW"
,
   
"Movie_name"
:
 
"Deer Hunter, The"
,
   
"Person_pob"
:
 
"New York, New York, USA"
,
   
"Movie_year"
:
 
1978
,
   
"Person_dob"
:
 
"1943-08-17"
  
}
 
]
,
 
"bookmark"
:
 
"g2w ... c2o"
}
See the following example that uses HTTP to search within a range:
POST
 
/my-movies/_find
 
HTTP/1.1
Host
: 
$SERVICE_URL
Content-Type
: 
application/json
{
  "selector": {
    "Person_name":"Robert De Niro",
    "Movie_year": {
      "$in": [1974, 2009]
    }
  }
}
See the following example that uses the command line to search within a range:
Curl
curl -X POST -H 
"Content-Type: application/json"
 \
 
"
$SERVICE_URL
/my-movies/_find"
 \
 -d 
'{"selector": {"Person_name":"Robert De Niro", "Movie_year": { "$in": [1974, 2009]}}}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ExplainResult;
import
 com.ibm.cloud.cloudant.v1.model.PostExplainOptions;
import
 java.util.Arrays;
import
 java.util.Collections;
import
 java.util.HashMap;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = 
new
 
HashMap
<>();
selector.put(
"Person_name"
, 
"Robert De Niro"
);
selector.put(
"Movie_year"
,
    Collections.singletonMap(
"$in"
, Arrays.asList(
1978
, 
2009
)));
Cloudant
   
305PostExplainOptions
 
explainOptions
 
=
    
new
 
PostExplainOptions
.Builder()
        .db(
"my-movies"
)
        .selector(selector)
        .build();
ExplainResult
 
response
 
=
    service.postExplain(explainOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
let
 
selector
: 
Cloudant
V1.
JsonObject
 = {
  
Person
_name
: 
'Robert De Niro'
,
  
Movie
_year
: {
'$in'
: [
1978
, 
2009
]}
};
service.
postFind
({
  
db
: 
'my-movies'
,
  
selector
: selector,
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_find(
  db=
'my-movies'
,
  selector={
'Person_name'
: 
'Robert De Niro'
,
    
'Movie_year'
: {
'$in'
: (
1978
, 
2009
)}}
).get_result()
print
(response)
Go
postFindOptions := service.NewPostFindOptions(
    
"my-movies"
,
    
map
[
string
]
interface
{}{
        
"Person_name"
: 
"Robert De Niro"
,
        
"Movie_year"
: 
map
[
string
][]
interface
{}{
            
"$in"
: []
interface
{}{
1978
, 
2009
},
        },
    },
)
findResult, _, err := service.PostFind(postFindOptions)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(findResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
Cloudant
   
306import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example result from the search:
{
 
"docs"
:
 
[
  
{
   
"_id"
:
 
"d9e6a7ae2363d6cfe81af75a392eb9f2"
,
   
"_rev"
:
 
"1-9faa75d7ea524448b1456a6c69a4391a"
,
   
"Movie_runtime"
:
 
183
,
   
"Movie_rating"
:
 
"R"
,
   
"Person_name"
:
 
"Robert De Niro"
,
   
"Movie_genre"
:
 
"DW"
,
   
"Movie_name"
:
 
"Deer Hunter, The"
,
   
"Person_pob"
:
 
"New York, New York, USA"
,
   
"Movie_year"
:
 
1978
,
   
"Person_dob"
:
 
"1943-08-17"
  
}
 
]
,
 
"bookmark"
:
 
"g2w ... c2o"
}
Creating Views (MapReduce)
Views are used to obtain data stored within a database. Within views, you use reduce functions, map and reduce functions, and storing a view
definition.
Learn more about the simplest view, reduce functions, map and reduce function restrictions, and storing a view definition. Plus, see the examples
that are provided. Views are written by using JavaScript.
View concepts
Views are mechanisms for working with document content in databases. A view can selectively filter documents and speed up the search for content.
It can be used to pre-process the results before they're returned to the client.
Views are simply JavaScript functions, which are defined within the 
views
 field of a design document. When you use a view, or more accurately
when you run a query by using your view, the system applies the JavaScript function to 
every document in the database. Views can be complex. You
might choose to define a collection of JavaScript functions to create the overall view that is required.
View index partitioning type
A view index inherits the partitioning type from the 
options.partitioned
 field of the design document that contains it.
A simple view
The simplest form of view is a map function. The map function produces output data that represents an analysis (a mapping) of the documents that
are stored within the database.
For example, you might want to find out which user completed the online registration and has a verified email to contact. You might find this
information by inspecting each document, and looking for a field in the document called "email_verified" 
and getting the value of "email". If the field
is present and has the value 
true
, it means the user completed the registration, and you can contact them by email. If the field isn't present or has a
value of something 
else than 
true
, the user didn't complete the registration.
Using the 
emit
 function in a view function makes it easy to produce a list in response to running a query by using the view. The list consists of key
and value pairs, where the key helps you identify the specific document and the 
value provides just the precise detail you want. The list also includes
metadata such as the number of 
key:value
 pairs returned.
 Note: 
The document 
_id
 is automatically included in each of the 
key:value
 pair result records. The document 
_id
 is included to make it
easier for the client to work with the results.
Cloudant
   
307See an example of a simple view by using a map function:
function
(
user
) {
  
if
(user.
email_verified
 === 
true
) {
    
emit
(user.
email
, {
name
: user.
name
, 
email_verified
: user.
email_verified
, 
joined
: user.
joined
});
  }
}
See sample data for demonstrating the simple view example:
[
    
{
        
"_id"
:
"abc123"
,
        
"name"
:
 
"Bob Smith"
,
        
"email"
:
 
"bob.smith@aol.com"
,
        
"email_verified"
:
 
true
,
        
"joined"
:
 
"2019-01-24T10:42:59.000Z"
    
}
,
    
{
        
"_id"
:
"abc125"
,
        
"name"
:
 
"Amelie Smith"
,
        
"email"
:
 
"amelie.smith@aol.com"
,
        
"email_verified"
:
 
true
,
        
"joined"
:
 
"2020-04-24T10:42:59.000Z"
    
}
]
See an example response from running the simple view query:
{
  
"total_rows"
:
 
2
,
  
"offset"
:
 
0
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"abc125"
,
      
"key"
:
 
"amelie.smith@aol.com"
,
      
"value"
:
 
{
        
"name"
:
 
"Amelie Smith"
,
        
"email_verified"
:
 
true
,
        
"joined"
:
 
"2020-04-24T10:42:59.000Z"
      
}
    
}
,
    
{
      
"id"
:
 
"abc123"
,
      
"key"
:
 
"bob.smith@aol.com"
,
      
"value"
:
 
{
        
"name"
:
 
"Bob Smith"
,
        
"email_verified"
:
 
true
,
        
"joined"
:
 
"2019-01-24T10:42:59.000Z"
      
}
    
}
  
]
}
Map function examples
The definition of a view within a design document also creates an index based on the key information. The production and use of the index
significantly increases the speed of access and searching or selecting documents from the view.
The following sections describe indexing with simple and complex keys, and reduce functions.
Your indexing functions work in a memory-constrained environment where the document forms part of the memory used in the environment. Your
code's stack and document must fit within the memory. We limit documents to a maximum size of 64 MB.
Indexing a field
The following map function checks whether the object has a 
name
 field, and if so emits the value of this field. With this check, you can query against
Cloudant
   
308the value of the 
name
 field.
See an example of indexing a field:
function
(
doc
) {
  
if
 (doc.
name
) {
    
emit
(
"name"
, doc.
name
);
  }
}
An index for a one-to-many relationship
If the object passed to 
emit
 has an 
_id
 field, a view query with 
include_docs
 set to 
true
 contains the document with the specific ID.
See an example of indexing a one-to-many relationship:
function
(
doc
) {
  
if
 (doc.
friends
) {
    
for
 (friend 
in
 doc.
friends
) {
      
emit
(doc.
_id
, { 
"_id"
: friend });
    }
  }
}
Complex keys
Keys aren't limited to simple values. You can use arbitrary JSON values to influence sorting.
When the key is an array, view results can be grouped by a subsection of the key. For example, if keys have the form 
[year, month, day]
, then
results can be reduced to a single value or by year, month, or day.
For more information, see 
Using views
.
Reduce functions
No reducer
A view definition inside a design document is permitted to have no reduce attribute, indicating that no query-time aggregation is performed.
{
    
"views"
:
 
{
        
"getVerifiedEmails"
:
 
{
            
"map"
:
 
"function(user) { if(user.email_verified === true) { emit(user.email); } }"
        
}
    
}
}
The previous map function generates a secondary index suitable for selection only. The index is always ordered by the key (the emit function's first
parameter) - in this case 
user.email
. This view is ideal for fetching documents 
by a known user email or ranges of users email addresses.
Built-in reduce functions
For performance reasons, a few simple reduce functions are built in. Whenever possible, you must use one of these functions instead of writing your
own.
To use one of the built-in functions, put the name into the 
reduce
 field of the view object in your design document.
{
    
"views"
:
 
{
        
"sumPrices"
:
 
{
            
"map"
:
 
"function(user) { if(user.email_verified === true) { emit(user.name, user.email); } }"
,
            
"reduce"
:
 
"_count"
 Tip: 
Design documents with 
options.partitioned
 set to 
true
 can't contain custom JavaScript reduce functions. Only built-in reduces
are allowed.
Cloudant
   
309        
}
    
}
}
The previous MapReduce view creates an index that is keyed on the username and whose counts all active email. As the reducer is 
_count
, the view
outputs the total email count for the selection of data queried. It is suitable for 
counting the registered users.
The numeric reducers 
_stats
/
_sum
 act upon the value (the emit function's second parameter) which can be a number, array, or object. Consider
the following MapReduce definition on the 
products
 partitioned 
database:
{
    
"views"
:
 
{
        
"statsReadingsObject"
:
 
{
            
"map"
:
 
"function(product) {  emit(product.type, { price: product.price, tax: product.tax }); }"
,
            
"reduce"
:
 
"_sum"
        
}
    
}
}
The view is keyed on the type of the product, and the value is an object that contains two values: price and tax. The 
_sum
 reduce calculates totals for
each attribute of the object that it finds:
{
"rows"
:
[
    
{
"key"
:
null
,
"value"
:
{
"price"
:
144.97
,
 
"tax"
:
7.32
}
}
]
}
Or add 
?group=true
 when querying the view. The output is grouped and summed by a unique key, in this case, 
type
:
{
"rows"
:
[
    
{
"key"
:
"portable"
,
"value"
:
{
"price"
:
14.99
,
"tax"
:
1.14
}
}
,
    
{
"key"
:
"product"
,
"value"
:
{
"price"
:
129.98
,
"tax"
:
6.18
}
}
]
}
The numeric reducers also calculate multiple reductions when the value of an index is an array of numbers:
{
    
"views"
:
 
{
        
"statsReadingsArray"
:
 
{
            
"map"
:
 
"function(doc) { emit(doc.date, [doc.price, doc.tax]); }"
,
            
"reduce"
:
 
"_stats"
        
}
    
}
}
The previous definition calculates statistics on the numerical values that it finds in the array that is emitted as the index's value. The values are
returned as an array in the same order as supplied in the map function:
{
"rows"
:
[
    
{
"key"
:
"portable"
,
"value"
:
[
        
{
"sum"
:
14.99
,
"count"
:
1
,
"min"
:
14.99
,
"max"
:
14.99
,
"sumsqr"
:
224.7001
}
,
        
{
"sum"
:
1.14
,
"count"
:
1
,
"min"
:
1.14
,
"max"
:
1.14
,
"sumsqr"
:
1.2995
}
    
]
}
,
    
{
"key"
:
"product"
,
"value"
:
[
        
{
"sum"
:
129.98
,
"count"
:
2
,
"min"
:
29.99
,
"max"
:
99.99
,
"sumsqr"
:
10897.4002
}
,
        
{
"sum"
:
6.18
,
"count"
:
2
,
"min"
:
1.62
,
"max"
:
4.56
,
"sumsqr"
:
23.418
}
    
]
}
]
}
The 
_count
 reducer simply counts the number of 
key-value
 pairs that are emitted into the index.
{
"rows"
:
[
    
{
"key"
:
"product"
,
"value"
:
3
}
]
}
The 
_approx_count_distinct_reducer
 acts upon the 
key
 of the index, as opposed to the numeric reducers that act upon the index's 
value
.
Cloudant
   
310{
"rows"
:
[
    
{
"key"
:
null
,
"value"
:
2
}
]
}
Table 1. Built-in reduce functions
Function
Description
_count
Produces the row count for a specific key. The values can be any valid JSON.
_stats
Produces a JSON structure that contains the sum, the count, the min, the max, and the sum-squared values. All
values must be numeric.
_sum
Produces the sum of all values for a key. The values must be numeric.
_approx_count_distinct
Approximates the number of distinct keys in a view index by using a variant of the 
HyperLogLog
 algorithm.
Custom reduce functions
Most customers find that built-in reducers are sufficient to perform aggregations on the view 
key-value
 pairs emitted from their Map functions.
However, for unusual use-cases, a JavaScript reduce function can be supplied instead 
of the name of one of the built-in reducers.
Reduce functions are passed three arguments in the following order:
keys
values
rereduce
If a view has a custom JavaScript reduce function, it is used to produce aggregate results for that view. A reduce function is passed a set of
intermediate values and combines them to a single value. A reduce function must accept, as input, 
results emitted by its corresponding map
function, as well as results returned by the reduce function itself. The latter case is referred to as a "rereduce".
A description of the reduce functions is shown in the following example.
See the following example of a custom reduce function:
function
 (
keys, values, rereduce
) {
  
return
 
sum
(values);
}
Reduce functions must handle two cases:
a
. 
When 
rereduce
 is false:
keys
 is an array whose elements are arrays of the form 
[key, id]
, where 
key
 is a key that is emitted by the map function, and 
id
identifies the document from which the key was generated 
values
 is an array of the values that are emitted for the respective elements
in 
keys
, for example: 
reduce([ [key1,id1], [key2,id2], [key3,id3] ], [value1,value2,value3], false)
.
b
. 
When 
rereduce
 is true:
keys
 is 
null
.
values
 is an array of the values that are returned by previous calls to the reduce function, for example: 
reduce(null,
[intermediate1,intermediate2,intermediate3], true)
.
Reduce functions must return a single value, suitable for both the 
value
 field of the final view, and as a member of the 
values
 array that is passed
to the reduce function.
Often, reduce functions can be written to handle rereduce calls without any extra code, like the summation function in the earlier example. In such
cases, the 
rereduce
 argument can be ignored.
By feeding the results of 
reduce
 functions back into the 
reduce
 function, MapReduce can split up the analysis of huge data sets into discrete,
parallel tasks, which can be completed much faster.
When you use the built-in reduce function, if the input is invalid, the 
builtin_reduce_error
 error is returned. More detailed information about the
failure is provided in the 
reason
 field. The original data that caused 
the error is returned in the 
caused_by
 field.
Cloudant
   
311See an example reply:
{
    
"rows"
:
 
[
        
{
            
"key"
:
 
null
,
            
"value"
:
 
{
                
"error"
:
 
"builtin_reduce_error"
,
                
"reason"
:
 
"The _sum function requires that map values be numbers, arrays of numbers, or objects. Objects
 
can't be mixed with other data structures. Objects can be arbitrarily nested, if the values for all fields are themselves
 
numbers, arrays of numbers, or objects."
,
                
"caused_by"
:
 
[
                    
{
                        
"a"
:
 
1
                    
}
,
                    
{
                        
"a"
:
 
2
                    
}
,
                    
{
                        
"a"
:
 
3
                    
}
,
                    
{
                        
"a"
:
 
4
                    
}
                
]
            
}
        
}
    
]
}
Map and reduce function restrictions
Map and reduce function restrictions are described here.
Referential transparency
The map function must be referentially transparent. Referential transparency means that an expression can be replaced with the same value without
changing the result, in this case, a document, and a 
key-value
 pair. Because of 
referential transparency, IBM Cloudant views can be updated
incrementally and reindex only the delta since the last update.
Commutative and associative properties
In addition to referential transparency, the reduce function must also have commutative and associative properties for the input. These properties
make it possible for the MapReduce function to reduce its own output and produce the same response, 
for example:
f(Key, Values) == f(Key, [ f(Key, Values) ] )
As a result, IBM Cloudant can store intermediate results to the inner nodes of the B-tree indexes. These restrictions also make it possible for indexes
to spread across machines and reduce at query time.
Document partitioning
Due to sharding, IBM Cloudant offers no guarantees that the output of any two specific map functions passes to the same instance of a reduce call.
You must not rely on any ordering. The reduce function that you use must consider all the values 
that are passed to it and return the correct answer
irrespective of ordering. IBM Cloudant is also guaranteed to call your reduce function with 
rereduce=true
 at query time even if it didn't need to do
so when it built the index. 
It's essential that your functions work correctly in that case (
rereduce=true
 means that the keys parameter is 
null
 and
the values array is filled with results from previous reduce function calls).
Reduced value size
IBM Cloudant computes view indexes and the corresponding reduce values then caches these values inside each of the B-tree node pointers. Now,
IBM Cloudant can reuse reduced values when it updates the B-tree. You must pay attention to the amount 
of data that is returned from reduce
functions.
It's best that the size of your returned data set stays small and grows no faster than 
log(num_rows_processed)
. If you ignore this restriction, IBM
Cloudant does not automatically throw an error, but B-tree performance degrades 
dramatically. If your view works correctly with small data sets but
Cloudant
   
312quits working when more data is added, your view might violate the growth rate characteristic restriction.
Execution environment
Your indexing functions work in a memory-constrained environment where the document forms part of the memory used in the environment. Your
code's stack and document must fit within the memory. We limit documents to a maximum size of 64 MB.
No JavaScript reducers when 
options.partitioned
 is 
true
Design documents with 
options.partitioned
 set to 
true
 can't contain JavaScript reduce functions, only built-ins Erlang reducers such as
_stats
.
Storing the view definition
Each view is a JavaScript function. Views are stored in design documents. So, to store a view, IBM Cloudant simply stores the function definition
within a design document. A design document can be 
created or updated
 
just like any other document.
To store a view definition, 
PUT
 the view definition content into a 
_design
 document.
In the following example, the 
getVerifiedEmails
 view is defined as a map function, and is available within the 
views
 field of the design
document.
Use the 
PUT
 method to add a view into a design document:
PUT
 
$SERVICE_URL/$DATABASE/_design/$DDOC
 
HTTP/1.1
Content-Type
: 
application/json
The following sample adds a new 
getVerifiedEmails
 named view function to the 
allusers
 design document with view definition:
$ 
{
    
"views"
:
 
{
        
"getVerifiedEmails"
:
 
{
            
"map"
:
 
"function(user) { if(user.email_verified === true){ emit(doc.email, {name: user.name, email_verified:
 
user.email_verified, joined: user.joined}) }}  "
        
}
    
}
}
See the request examples:
Curl
curl -X PUT 
"
$SERVICE_URL
/users/_design/allusers"
 --data 
'{
  "views": {
    "getVerifiedEmails": {
      "map": "function(user) { if(user.email_verified === true){ emit(doc.email, {name: user.name, email_verified:
 
user.email_verified, joined: user.joined}) }}"
    }
  }
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DesignDocument;
import
 com.ibm.cloud.cloudant.v1.model.DesignDocumentViewsMapReduce;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PutDesignDocumentOptions;
import
 java.util.Collections;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DesignDocumentViewsMapReduce
 
emailViewMapReduce
 
=
    
new
 
DesignDocumentViewsMapReduce
.Builder()
        .map(
"function(user) { if(user.email_verified === true){ emit(doc.email,{name: user.name, email_verified:
 
user.email_verified, joined: user.joined}) }"
)
Cloudant
   
313        .build();
DesignDocument
 
designDocument
 
=
 
new
 
DesignDocument
();
designDocument.setViews(
        Collections.singletonMap(
"getVerifiedEmails"
, emailViewMapReduce));
PutDesignDocumentOptions
 
designDocumentOptions
 
=
    
new
 
PutDesignDocumentOptions
.Builder()
        .db(
"users"
)
        .designDocument(designDocument)
        .ddoc(
"allusers"
)
        .build();
DocumentResult
 
response
 
=
    service.putDesignDocument(designDocumentOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
emailViewMapReduce
: 
Cloudant
V1.
DesignDocumentViewsMapReduce
 = {
  
map
: 
'function(user) { if(user.email_verified === true){ emit(doc.email, {name: user.name, email_verified:
 
user.email_verified, joined: user.joined}) }}'
}
const
 
designDocument
: 
Cloudant
V1.
DesignDocument
 = {
  
views
: {
'getVerifiedEmails'
: emailViewMapReduce}
}
service.
putDesignDocument
({
  
db
: 
'users'
,
  
designDocument
: designDocument,
  
ddoc
: 
'allusers'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
email_view_map_reduce = DesignDocumentViewsMapReduce(
  
map
=
'function(user) { if(user.email_verified === true){ emit(doc.email, {name: user.name, email_verified:
 
user.email_verified, joined: user.joined}) }}'
)
design_document = DesignDocument(
  views={
'getVerifiedEmails'
: email_view_map_reduce}
)
response = service.put_design_document(
  db=
'users'
,
  design_document=design_document,
  ddoc=
'allusers'
).get_result()
print
(response)
Go
emailViewMapReduce, err := service.NewDesignDocumentViewsMapReduce(
  
"function(user) { if(user.email_verified === true){ emit(doc.email, {name: user.name, email_verified: user.email_verified,
 
Cloudant
   
314joined: user.joined}) }}"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
designDocument := &cloudantv1.DesignDocument{
  Views: 
map
[
string
]cloudantv1.DesignDocumentViewsMapReduce{
    
"getVerifiedEmails"
: *emailViewMapReduce,
  },
}
putDesignDocumentOptions := service.NewPutDesignDocumentOptions(
  
"users"
,
  
"allusers"
,
  designDocument,
)
documentResult, _, err := service.PutDesignDocument(putDesignDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
  
"encoding/json"
  
"fmt"
  
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Using Views
Use views to search for content within a database that matches specific criteria. The criteria are specified within the view definition.
Criteria can also be supplied as arguments when you use the view.
Querying a view
To query a view, submit a 
GET
 request with the following format:
Method
Issue a partition query by using the following command, 
GET
$SERVICE_URL/$DATABASE/_partition/$PARTITION_KEY/_design/$DDOC/_view/$VIEW_NAME
. Or issue a global query by using the following
command, 
GET $SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME
.
Request
None
Response
JSON of the documents that are returned by the view.
Roles permitted
_reader
The request runs either:
Cloudant
   
315The specified 
$VIEW_NAME
 from the specified 
$DDOC
 design document within the 
$DATABASE
 database, which is constrained to results
within the specified 
$PARTITION_KEY
 data partition.
The specified 
$VIEW_NAME
 from the specified 
$DDOC
 design document within the 
$DATABASE
 database.
The examples in this document vary between partition and global queries for illustrative purposes. Unless otherwise noted, modifying the path to
embed or remove the partition name works for any view query type.
Query and JSON Body Arguments
Global queries can use all query and JSON body arguments. Partition queries can use only the subset that is indicated in the table.
Argument
Description
Optional
Type
Default
Supported
values
Partition
query
conflicts
Specify whether to include a list of conflicted revisions
in the 
_conflicts
 property of the returned document.
Ignored if 
include_docs
 isn't set to 
true
.
Yes
Boolean
False
Yes
descending
Return the documents in 
descending by key
 order.
Yes
Boolean
False
Yes
end_key
Stop returning records when the specified key is
reached.
Yes
String or
JSON
array
Yes
end_key_docid
Stop returning records when the specified document
ID is reached.
Yes
String
Yes
group
Specify whether to group reduced results by key. Valid
only if a reduce function is defined in the view. If the
view emits keys in JSON array format, then it is
possible to reduce groups further based on the
number of array elements 
with the 
group_level
parameter.
Yes
Boolean
False
Yes
group_level
Specify a group level to be used. Only applicable if the
view uses keys that are JSON arrays. Implies group is
true
. Group level groups the reduced results by the
specified number of array elements. If unset, results
are 
grouped by the entire array key, returning a
reduced value for each complete key.
Yes
Numeric
Yes
include_docs
Include the full content of the documents in the
response.
Yes
Boolean
False
Yes
inclusive_end
Include rows with the specified 
end_key
.
Yes
Boolean
True
Yes
key
Return only documents that match the specified key.
Keys are JSON values, and must be URL encoded.
Yes
JSON
array
Yes
keys
Specify to return only documents that match any of
the specified keys. String representation of a JSON
array of keys that match the key type that is emitted
by the view function.
Yes
String or
JSON
array
Yes
limit
Limit the number of returned documents to the
specified count.
Yes
Numeric
Yes
reduce
Use the 
reduce
 function.
Yes
Boolean
True
Yes
skip
Skip this number of rows from the start.
Yes
Numeric
0
Yes
Cloudant
   
316Table 1. Subset of query and JSON body arguments available for partitioned queries
stable
Specify whether to use the same replica of the index
on each request. The default value 
false
 contacts all
replicas and returns the result from the first, fastest
responder. Setting it to 
true
, when used with
update=false
, might improve consistency at the
expense of increased latency and decreased
throughput if the selected replica is not the fastest of
the available replicas.
Note
: In general, setting this parameter to 
true
 is
discouraged and not recommended when you use
update=true
.
Yes
Boolean
False
No
stale
Note
: 
stale
 is deprecated. Use 
stable
 and
update
 instead.
Specify whether to use the results from a stale view
without triggering a rebuild of all views within the
encompassing design doc.
ok
 is equivalent to
stable=true&update=false
.
update_after
 is equivalent to
stable=true&update=lazy
.
Yes
String
False
No
start_key
Return records, starting with the specified key.
Yes
String or
JSON
array
Yes
start_key_docid
Return records, starting with the specified document
ID.
Yes
String
Yes
update
Specify whether or not the view in question must be
updated before you respond to the user.
true
 - Return results after the view is updated.
false
 - Return results without updating the
view.
lazy
 - Return the view results without waiting
for an update, but update them immediately
after the request.
Yes
String
True
Yes
See the example of using HTTP to retrieve a list of the first 10 documents that include the full content of the documents from a partition of a
database, applying a user-created view.
GET
 
$SERVICE_URL/$DATABASE/_partition/$PARTITION_KEY/_design/$DDOC/_view/$VIEW_NAME?include_docs=true&limit=10
 
HTTP/1.1
See the example of using HTTP to retrieve a list of the first 10 documents from a database, applying a user-created view.
GET
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME?limit=10
 
HTTP/1.1
See the example to retrieve a list of the first 10 documents that include the full content of them from the 
small-appliances
 partition of a database,
applying the user-created 
byApplianceProdId
 view.
Curl
 Important: 
Using 
include_docs=true
 might have 
performance implications
.
Client libraries use 
POST
 method instead of 
GET
 because they have the same behavior.
Cloudant
   
317curl -X GET 
"
$SERVICE_URL
/products/_partition/small-appliances/_design/appliances/_view/byApplianceProdId?
include_docs=true&limit=10"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostPartitionViewOptions
 
viewOptions
 
=
    
new
 
PostPartitionViewOptions
.Builder()
        .db(
"products"
)
        .ddoc(
"appliances"
)
        .includeDocs(
true
)
        .limit(
10
)
        .partitionKey(
"small-appliances"
)
        .view(
"byApplianceProdId"
)
        .build();
ViewResult
 
response
 
=
    service.postPartitionView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postPartitionView
({
  
db
: 
'products'
,
  
ddoc
: 
'appliances'
,
  
includeDocs
: 
true
,
  
limit
: 
10
,
  
partitionKey
: 
'small-appliances'
,
  
view
: 
'byApplianceProdId'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_view(
  db=
'products'
,
  ddoc=
'appliances'
,
  include_docs=
True
,
  limit=
10
,
  partition_key=
'small-appliances'
,
  view=
'byApplianceProdId'
).get_result()
print
(response)
Go
postPartitionViewOptions := service.NewPostPartitionViewOptions(
  
"products"
,
  
"small-appliances"
,
  
"appliances"
,
  
"byApplianceProdId"
,
Cloudant
   
318)
postPartitionViewOptions.SetIncludeDocs(
true
)
postPartitionViewOptions.SetLimit(
10
)
viewResult, response, err := service.PostPartitionView(postPartitionViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the example to retrieve a list of the first 10 documents from a database, applying the user-created 
getVerifiedEmails
 view.
Curl
curl -X GET 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails?limit=10"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .limit(
10
)
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
limit
: 
10
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
Client libraries use 
POST
 method instead of 
GET
 because they have the same behavior.
Cloudant
   
319});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  limit=
10
).get_result()
print
(response)
Go
postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
postViewOptions.SetLimit(
10
)
viewResult, response, err := service.PostView(postViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the following example response to the request:
{
  
"offset"
:
 
0
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"abc125"
,
      
"key"
:
 
"amelie.smith@aol.com"
,
      
"value"
:
 
[
        
"Amelie Smith"
,
        
true
,
        
"2020-04-24T10:42:59.000Z"
      
]
    
}
,
    
{
      
"id"
:
 
"abc123"
,
      
"key"
:
 
"bob.smith@aol.com"
,
      
"value"
:
 
[
        
"Bob Smith"
,
        
true
,
Cloudant
   
320        
"2019-01-24T10:42:59.000Z"
      
]
    
}
  
]
,
  
"total_rows"
:
 
2
}
Indexes
When a view is defined in a design document, a corresponding index is also created, based on the information defined within the view. Use indexes to
find documents by criteria other than their 
_id
 field. For example, you might select 
by a field, or combination of fields, or by a value that is computed
by using the contents of the document. The index is populated as soon as the design document is created. On large databases, this process might
take a while.
If one of the following events occurs, the index content is updated incrementally and automatically:
A new document is added to the database.
An existing document is deleted from the database.
An existing document in the database is updated.
View indexes are rebuilt entirely when the view definition changes, or when another view definition in the same design document changes. The
rebuild ensures that changes to the view definitions are reflected in the view indexes. To ensure that 
the rebuild happens, a 'fingerprint' of the view
definition is created whenever the design document is updated. If the fingerprint changes, then the view indexes are rebuilt.
If the database was updated recently, the results might be delayed when the view is accessed. The delay is affected by the number of changes to the
database, and whether the view index isn't current because the database content was modified.
It isn't possible to eliminate these delays. For newly created databases, you might reduce the delays by creating the view definition in the design
document in your database before you insert or update documents. Creating the view definition 
in the design document causes incremental updates
to the index when the documents are inserted.
If speed of response is more important than having up-to-date data, an alternative is to allow users to access an old version of the view index. To
allow access to an old version of the view index, use the 
update
 query string parameter 
when you make a view query.
See the following examples:
$ 
{
  
"_id"
:
 
"_design/lookup"
,
  
"autoupdate"
:
 
false
,
  
"views"
:
 
{
    
"view"
:
 
{
      
"map"
:
 
"function(doc)..."
    
}
  
}
}
$ 
{
  
"_id"
:
 
"_design/lookup"
,
  
"autoupdate"
:
 
{
"views"
:
 
false
}
,
  
"views"
:
 
{
    
"view"
:
 
{
      
"map"
:
 
"function(doc)..."
    
}
  
}
}
 Tip: 
View index rebuilds occur when you change any one view from all the views that are defined in the design document. For example, if you
have a design document with three views, and you update the design document, all three view indexes within 
the design document are
rebuilt. If you want to change a design document for a larger database, have a look at the 
Design document management guide
.
 Important: 
If you want to save old index versions without incurring indexing processor usage, you can stop all indexes from building by
setting 
"autoupdate": {"indexes": false}
. Or you can stop views from auto-updating 
by adding one of the following options to a design
document. You can stop all index types from indexing if you set 
"autoupdate": false
.
Cloudant
   
321View freshness
By default, all index results reflect the current state of the database. IBM Cloudant builds its indexes automatically and asynchronously in the
background. This practice usually means that the index is fully up to date when you query it. If 
not, by default, IBM Cloudant applies the remaining
updates at query time.
IBM Cloudant provides a few parameters, described next to alter this behavior. We recommend against using them as the side-effects typically
outweigh their benefit.
Parameters
The 
update
 option indicates whether you're prepared to accept view results without waiting for the view to be updated. The default value is 
true
,
meaning that the view is updated before results are returned. The 
lazy
 
value means that the results are returned before the view is updated, but
that the view must then be updated anyway.
The 
stable
 option indicates whether you would prefer to get results from a single, consistent set of shards. The 
false
 value means that all
available shard replicas are queried and IBM Cloudant uses the fastest response. 
By contrast, setting 
stable=true
 forces the database to use just
one replica of the index.
Combining parameters
If you specify 
stable=false
 and 
update=false
, you see greater inconsistency between results, even for the same query and without making
database changes. We recommend against this combination unless you are sure that 
your system can tolerate this behavior.
Sorting returned rows
The data that is returned by a view query is in the form of an array. Each element within the array is sorted by using standard 
UTF-8
 sorting. The sort
is applied to the key defined in the view function.
The basic order of the output is shown in the following table:
Table 2. Order of returned rows
Value
Order
null
First
false
true
Numbers
Text (lowercase)
Text (uppercase)
Arrays (according to the values of each element, by using the order given in this table)
Objects (according to the values of keys, in key order by using the order given in this table)
Last
You can reverse the order of the returned view information by setting the 
descending
 query value 
true
.
 Important: 
While IBM Cloudant strives to keep indexes updated in the background, no guarantee exists about how out-of-date the view is
when queried with 
update=false
 or 
update=lazy
.
 Important: 
Using 
stable=true
 can cause high latency as it consults only one of the copies of the index, even if the other copies would
respond faster.
 Tip: 
When you issue a view request that specifies the 
keys
 parameter, the results are returned in the same order as the supplied 
keys
array.
Cloudant
   
322See the example of using HTTP to request the records in reversed sort order:
GET
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME?descending=true
 
HTTP/1.1
Accept
: 
application/json
See the example of requesting the records in reverse sort order.
Curl
curl -X GET 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails?descending=true"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .descending(
true
)
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
descending
: 
true
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  descending=
True
).get_result()
print
(response)
Go
Client libraries use 
POST
 method instead of 
GET
 because they have a similar behavior.
Cloudant
   
323postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
postViewOptions.SetDescending(
true
)
viewResult, response, err := service.PostView(postViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the example response of requesting the records in reverse sort order:
{
  
"total_rows"
:
 
2
,
  
"offset"
:
 
0
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"abc123"
,
      
"key"
:
 
"bob.smith@aol.com"
,
      
"value"
:
 
[
        
"Bob Smith"
,
        
true
,
        
"2019-01-24T10:42:59.000Z"
      
]
    
}
,
    
{
      
"id"
:
 
"abc125"
,
      
"key"
:
 
"amelie.smith@aol.com"
,
      
"value"
:
 
[
        
"Amelie Smith"
,
        
true
,
        
"2020-04-24T10:42:59.000Z"
      
]
    
}
  
]
}
Specifying start and end keys
The 
start_key
 and 
end_key
 query arguments can be used to specify the range of values that are returned when querying the view.
The sort direction is always applied first. Next, filtering is applied by using the 
start_key
 and 
end_key
 query arguments. It is possible that no rows
match your keyrange if sort and filter plans don't make sense when 
combined.
See the example of using HTTP to make a global query that includes 
start_key
 and 
end_key
 query arguments:
GET
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME?start_key="alpha"&end_key="beta"
 
HTTP/1.1
See the example of a global query that includes 
start_key
 and 
end_key
 query arguments.
Cloudant
   
324Curl
curl -X GET 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails?start_key=\"alpha\"&end_key=\"beta\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .startKey(
"alpha"
)
    .endKey(
"beta"
)
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
startKey
: 
'alpha'
,
  
endKey
: 
'beta'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  start_key=
'alpha'
,
  end_key=
'beta'
  
).get_result()
print
(response)
Go
postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
Client libraries use 
POST
 method instead of 
GET
 because they have the same behavior.
Cloudant
   
325postViewOptions.StartKey = 
"alpha"
postViewOptions.EndKey = 
"beta"
viewResult, response, err := service.PostView(postViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
For example, if you have a database that returns one result when you use a 
start_key
 of 
alpha
 and an 
end_key
 of 
beta
, you would get a 
400
(Bad request) error with a reversed order. 
The reason is that the entries in the view are reversed before the key filter is applied.
See the example that uses HTTP to illustrate why reversing the order of 
start_key
 and 
end_key
 might return a query parse error:
GET
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME?descending=true&start_key="alpha"&end_key="beta"
 
HTTP/1.1
See the example illustrating why reversing the order of 
start_key
 and 
end_key
 might cause a 
400
 error.
Curl
curl -X GET 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails?
descending=true&start_key=\"alpha\"&end_key=\"beta\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .descending(
true
)
    .startKey(
"alpha"
)
    .endKey(
"beta"
)
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
Client libraries use 
POST
 method instead of 
GET
 because they have the same behavior.
Cloudant
   
326const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
descending
: 
true
,
  
startKey
: 
'alpha'
,
  
endKey
: 
'beta'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  descending=
True
,  
  start_key=
'alpha'
,
  end_key=
'beta'
  
).get_result()
print
(response)
Go
postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
postViewOptions.SetDescending(
true
)
postViewOptions.StartKey = 
"alpha"
postViewOptions.EndKey = 
"beta"
viewResult, response, err := service.PostView(postViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
The 
end_key
 of 
beta
 is seen before the 
start_key
 of 
alpha
, resulting in a query parse error.
The solution is to reverse not just the sort order, but also the 
start_key
 and 
end_key
 parameter values.
The following example shows correct filtering and reversing the order of output, by using the 
descending
 query argument, and reversing the
Cloudant
   
327start_key
 and 
end_key
 query arguments.
See the example that uses HTTP to apply correct filtering and sorting to a global query:
GET
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME?descending=true&start_key="beta"&end_key="alpha"
 
HTTP/1.1
See the example to apply correct filtering and sorting to a global query.
Curl
curl -X GET 
"
$SERVER_URL
/users/_design/allusers/_view/getVerifiedEmails?
descending=true&start_key=\"beta\"&end_key=\"alpha\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .descending(
true
)
    .startKey(
"beta"
)
    .endKey(
"alpha"
)
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
descending
: 
true
,
  
startKey
: 
'beta'
,
  
endKey
: 
'alpha'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  descending=
True
,  
  start_key=
'beta'
,
Client libraries use 
POST
 method instead of 
GET
 because they have the same behavior.
Cloudant
   
328  end_key=
'alpha'
  
).get_result()
print
(response)
Go
postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
postViewOptions.SetDescending(
true
)
postViewOptions.StartKey = 
"beta"
postViewOptions.EndKey = 
"alpha"
viewResult, response, err := service.PostView(postViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Querying a view by using a list of keys
You can also run a query by providing a list of keys to use.
Requesting information from a database in this way uses the specified 
$VIEW_NAME
 from the specified 
$DDOC
 design document. Like the 
keys
parameter for the 
GET
 
method, you can use the 
POST
 method to specify the keys to use to retrieve the view results. In all other aspects, the 
POST
method is the same as the 
GET
 API request. In 
particular, you can use any of its query parameters in either the query string or the JSON body.
See the example HTTP request that returns all users, where the key for the view matches either 
amelie.smith@aol.com
 or 
bob.smith@aol.com
:
POST
 
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW_NAME
 
HTTP/1.1
Content-Type
: 
application/json
{
  
"keys"
: [
    
"amelie.smith@aol.com"
,
    
"bob.smith@aol.com"
  ]
}
See the example of a global query that returns all users (where the key for the view matches is either 
amelie.smith@aol.com
 or
bob.smith@aol.com
):
Curl
curl -X POST 
"
$SERVICE_URL
/users/_design/allusers/_view/getVerifiedEmails"
 -H 
"Content-Type: application/json"
 --data 
'{
  "keys": [
    "amelie.smith@aol.com",
    "bob.smith@aol.com"
Cloudant
   
329  ]
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostViewOptions
 
viewOptions
 
=
 
new
 
PostViewOptions
.Builder()
    .db(
"users"
)
    .ddoc(
"allusers"
)
    .view(
"getVerifiedEmails"
)
    .keys(Arrays.asList(
"amelie.smith@aol.com"
, 
"bob.smith@aol.com"
))
    .build();
ViewResult
 
response
 
=
    service.postView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postView
({
  
db
: 
'users'
,
  
ddoc
: 
'allusers'
,
  
view
: 
'getVerifiedEmails'
,
  
keys
: [
'amelie.smith@aol.com'
, 
'bob.smith@aol.com'
]
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_view(
  db=
'users'
,
  ddoc=
'allusers'
,
  view=
'getVerifiedEmails'
,
  keys=[
'amelie.smith@aol.com'
, 
'bob.smith@aol.com'
]
).get_result()
print
(response)
Go
postViewOptions := service.NewPostViewOptions(
  
"users"
,
  
"allusers"
,
  
"getVerifiedEmails"
,
)
keys := []
interface
{}{
"amelie.smith@aol.com"
, 
"bob.smith@aol.com"
}
postViewOptions.SetKeys(keys)
viewResult, response, err := service.PostView(postViewOptions)
Cloudant
   
330if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
The response contains the standard view information, but only documents where the keys match.
See the example response after you run a query by using a list of keys:
{
  
"total_rows"
:
 
2
,
  
"offset"
:
 
0
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"abc125"
,
      
"key"
:
 
"amelie.smith@aol.com"
,
      
"value"
:
 
[
        
"Amelie Smith"
,
        
true
,
        
"2020-04-24T10:42:59.000Z"
      
]
    
}
,
    
{
      
"id"
:
 
"abc123"
,
      
"key"
:
 
"bob.smith@aol.com"
,
      
"value"
:
 
[
        
"Bob Smith"
,
        
true
,
        
"2019-01-24T10:42:59.000Z"
      
]
    
}
  
]
}
Multi-document fetching
The following section covers a 
POST
 request to many documents from a database.
For a client application, this technique is more efficient than using multiple 
GET
 API requests.
However, 
include_docs=true
 might require extra processing time when compared to accessing the view on its own.
The reason is that by using 
include_docs=true
 in a view query, all of the result documents must be retrieved to construct the response for the
client application. In effect, a whole series of document 
GET
 requests are 
run, each of which competes for resources with other application
requests.
One way to mitigate this effect is by retrieving results directly from the view index file. Omit 
include_docs=true
 to retrieve results directly from the
view index file. Instead, in the map function in a design document, emit the 
fields that are required as the value for the view index.
For example, in your map function, you might use the following design specification:
$ 
function
(
user
) {
  
if
(user.
email_verified
 === 
true
) {
    
emit
(user.
email
, {
name
: user.
name
, 
email_verified
: user.
email_verified
, 
joined
: user.
joined
});
Cloudant
   
331  }
}
See the example request that uses HTTP to obtain the full content of documents that match the listed keys within a partition:
POST
 
$SERVICE_URL/$DATABASE/_partition/$PARTITION_KEY/_design/$DDOC/_view/$VIEW_NAME
 
HTTP/1.1
Content-Type
: 
application/json
{
  
"include_docs"
: 
true
,
  
"keys"
 : [
    
"1000043"
,
    
"1000044"
  ]
}
See the example request to obtain the full content of documents that match the listed keys within the 
products
 partition:
Curl
curl -X POST 
"
$SERVICE_URL
/products/_partition/small-appliances/_design/appliances/_view
/byApplianceProdId"
 -H 
"Content-Type: application/json"
 --data 
'{
  "include_docs": true,
  "keys" : [
    "1000043",
    "1000044"
  ]
}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostPartitionViewOptions
 
viewOptions
 
=
    
new
 
PostPartitionViewOptions
.Builder()
        .db(
"products"
)
        .ddoc(
"appliances"
)
        .keys(Arrays.asList(
"1000043"
, 
"1000044"
))
        .includeDocs(
true
)
        .partitionKey(
"small-appliances"
)
        .view(
"byApplianceProdId"
)
        .build();
ViewResult
 
response
 
=
    service.postPartitionView(viewOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postPartitionView
({
  
db
: 
'products'
,
  
ddoc
: 
'appliances'
,
  
keys
: [
'1000043'
, 
'1000044'
],
  
includeDocs
: 
true
,
  
partitionKey
: 
'small-appliances'
,
  
view
: 
'byApplianceProdId'
Cloudant
   
332}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_partition_view(
  db=
'products'
,
  ddoc=
'appliances'
,
  keys=[
'1000043'
, 
'1000044'
],
  include_docs=
True
,  
  partition_key=
'small-appliances'
,
  view=
'byApplianceProdId'
).get_result()
print
(response)
Go
postPartitionViewOptions := service.NewPostPartitionViewOptions(
  
"products"
,
  
"small-appliances"
,
  
"appliances"
,
  
"byApplianceProdId"
,
)
keys := []
interface
{}{
"1000043"
, 
"1000044"
}
postPartitionViewOptions.SetKeys(keys)
postPartitionViewOptions.SetIncludeDocs(
true
)
viewResult, response, err := service.PostPartitionView(postPartitionViewOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(viewResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the example (abbreviated) response, returning the full document for each appliance that matches a provided key:
{
  
"total_rows"
:
 
4
,
  
"offset"
:
 
1
,
  
"rows"
:
 
[
    
{
      
"id"
:
 
"small-appliances:1000043"
,
      
"key"
:
 
"1000043"
,
      
"value"
:
 
[
        
"Bar"
,
        
"Pro"
,
        
"A professional, high powered innovative tool with a sleek design and outstanding performance"
Cloudant
   
333      
]
,
      
"doc"
:
 
{
        
"_id"
:
 
"small-appliances:1000043"
,
        
"_rev"
:
 
"2-b595c929aabc3ab13415cd0cc03e665d"
,
        
"type"
:
 
"product"
,
        
"taxonomy"
:
 
[
          
"Home"
,
          
"Kitchen"
,
          
"Small Appliances"
        
]
,
        
"keywords"
:
 
[
          
"Bar"
,
          
"Blender"
,
          
"Kitchen"
        
]
,
        
"productId"
:
 
"1000043"
,
        
"brand"
:
 
"Bar"
,
        
"name"
:
 
"Pro"
,
        
"description"
:
 
"A professional, high powered innovative tool with a sleek design and outstanding performance"
,
        
"colours"
:
 
[
          
"black"
        
]
,
        
"price"
:
 
99.99
,
        
"image"
:
 
"assets/img/barpro.jpg"
      
}
    
}
,
    
{
      
"id"
:
 
"small-appliances:1000044"
,
      
"key"
:
 
"1000044"
,
      
"value"
:
 
[
        
"Baz"
,
        
"Omelet Maker"
,
        
"Easily make delicious and fluffy omelets without flipping - Innovative design - Cooking and cleaning is easy"
      
]
,
      
"doc"
:
 
{
        
"_id"
:
 
"small-appliances:1000044"
,
        
"_rev"
:
 
"2-d54d022a9407ab9f06b1889cb2ab8a6e"
,
        
"type"
:
 
"product"
,
        
"taxonomy"
:
 
[
          
"Home"
,
          
"Kitchen"
,
          
"Small Appliances"
        
]
,
        
"keywords"
:
 
[
          
"Baz"
,
          
"Maker"
,
          
"Kitchen"
        
]
,
        
"productId"
:
 
"1000044"
,
        
"brand"
:
 
"Baz"
,
        
"name"
:
 
"Omelet Maker"
,
        
"description"
:
 
"Easily make delicious and fluffy omelets without flipping - Innovative design - Cooking and
 
cleaning is easy"
,
        
"colours"
:
 
[
          
"black"
        
]
,
        
"price"
:
 
29.99
,
        
"image"
:
 
"assets/img/bazomeletmaker.jpg"
      
}
    
}
  
]
}
Using IBM Cloudant Search
Search indexes provide a way to query a database by using 
Lucene Query Parser Syntax
. 
A search index uses one or more fields from your
documents.
You can use a search index to run queries, find documents based on the content they include, or work with groups, facets, or geographical searches.
Cloudant
   
334To create a search index, you add a JavaScript function to a design document in the database. An index builds after it processes one search request
or after the server detects a document update. The 
index
 function takes the following 
parameters:
a
. 
Field name - The name of the field you want to use when you query the index. If you set this parameter to 
default
, then this field is queried if
no field is specified in the query syntax.
b
. 
Data that you want to index, for example, 
doc.address.country
.
c
. 
(Optional) The third parameter includes the following fields: 
boost
, 
facet
, 
index
, and 
store
. These fields are described in more detail
later.
By default, a search index response returns 25 rows. The number of rows that is returned can be changed by using the 
limit
 parameter. However,
a result set from a search is limited to 200 rows. Each response includes a 
bookmark
 
field. You can include the value of the 
bookmark
 field in later
queries to look through the responses.
You can query the API by using one of the following methods: URI, IBM Cloudant Dashboard, curl, or a browser plug-in, such as Postman or
RESTClient.
See the following example design document that defines a search index:
{
 
"_id"
:
 
"_design/search_example"
,
 
"indexes"
:
 
{
  
"animals"
:
 
{
   
"index"
:
 
"function(doc){ ... }"
  
}
 
}
}
Search index partitioning type
A search index inherits the partitioning type from the 
options.partitioned
 field of the design document that contains it.
Index functions
If you attempt to index by using a data field that doesn't exist, it fails. To avoid this problem, use an appropriate 
guard clause
.
Within a search index, don't index the same field name with more than one data type. If the same field name is indexed with different data types in
the same search index function, you might get an error. This error occurs when you query the 
search index that says the field 
was indexed without
position data
. For example, don't include both of these lines in the same search index function. These lines index the 
myfield
 field as two
different data types, 
a string 
"this is a string"
 and a number 
123
.
$ 
index(
"myfield"
,
 
"this is a string"
);
index(
"myfield"
,
 
123
);
The function that is contained in the index field is a JavaScript function that is called for each document in the database. The function takes the
document as a parameter, extracts some data from it, and then calls the function that is defined 
in the 
index
 field to index that data.
The 
index
 function takes three parameters, where the third parameter is optional.
The first parameter is the name of the field that you intend to use when querying the index, which is specified in the Lucene syntax portion of later
queries. An example appears in the following query:
query=color:red
The Lucene field name 
color
 is the first parameter of the 
index
 function.
The 
query
 parameter can be abbreviated to 
q
, so another way of writing the query is shown in the following example.
q=color:red
If the special value 
"default"
 is used when you define the name, you don't have to specify a field name at query time. The effect is that the query
can be simplified:
 Note: 
Your indexing functions operate in a memory-constrained environment where the document itself forms a part of the memory that is
used in that environment. Your code's stack and document must fit inside this memory. Documents are limited to a 
maximum size of 64 MB.
Cloudant
   
335query=red
The second parameter is the data to be indexed. Keep the following information in mind when you index your data:
This data must be only a string, number, or boolean. Other types return an error from the index function call.
If an error is returned when your function is running, for this reason or others, the document isn't added to that search index.
The third, optional, parameter is a JavaScript object with the following fields:
Table 1. Fields for the JavaScript object (optional parameter)
Option
Description
Values
Default
boost
A number that specifies the relevance in search results. Content that is indexed with a boost value
greater than 1 is more relevant than content that is indexed without a boost value. Content with a
boost value less than one isn't so relevant.
A positive
floating
point
number
1 (No
boosting)
facet
Creates a faceted index. For more information, see 
Faceting
.
true
false
index
Whether the data is indexed, and if so, how. If set to 
false
, the data can't be used for searches, but
can still be retrieved from the index if 
store
 is set to 
true
. For more information, see 
Analyzers
.
true
, 
false
true
store
If 
true
, the value is returned in the search result; otherwise, the value isn't returned.
true
, 
false
false
See the following example search index function:
function
(
doc
) {
 
index
(
"default"
, doc.
_id
);
 
if
 (doc.
min_length
) {
  
index
(
"min_length"
, doc.
min_length
, {
"store"
: 
true
});
 }
 
if
 (doc.
diet
) {
  
index
(
"diet"
, doc.
diet
, {
"store"
: 
true
});
 }
 
if
 (doc.
latin_name
) {
  
index
(
"latin_name"
, doc.
latin_name
, {
"store"
: 
true
});
 }
 
if
 (doc.
class
) {
  
index
(
"class"
, doc.
class
, {
"store"
: 
true
});
 }
}
Index guard clauses
The 
index
 function requires the name of the data field to index as the second parameter. However, if that data field doesn't exist for the document,
an error occurs. The solution is to use an appropriate "guard clause" 
that checks whether the field exists. This clause contains the expected type of
data before any attempt to create the corresponding index.
See the following example definition that doesn't have any validation on the type of the index data field:
if
 (doc.
min_length
) {
 
index
(
"min_length"
, doc.
min_length
, {
"store"
: 
true
});
}
You might use the JavaScript 
typeof
 operator to implement the guard clause test. If the field exists and has the expected type, the correct type
name is returned. The guard clause test succeeds, which means it's safe to use the 
index function. If the field does not exist, you wouldn't get back
the expected type of field, that's why you wouldn't try to index the field.
JavaScript considers a result to be false if one of the following values is tested:
'undefined'
Null
 Tip: 
If you don't set the 
store
 parameter, the index data results for the document aren't returned in response to a query.
Cloudant
   
336The number +0
The number -0
NaN (not a number)
"" (the empty string)
See the following example that uses a guard clause to check whether the required data field exists, and holds a number, before you try to index:
if
 (
typeof
 doc.
min_length
 === 
'number'
) {
    
index
(
"min_length"
, doc.
min_length
, {
"store"
: 
true
});
}
Use a generic guard clause test to ensure that the type of the candidate data field is defined.
See the following example of a "generic" guard clause:
if
 (
typeof
 doc.
min_length
) !== 
'undefined'
) {
 
// The field exists, and does have a type, so we can proceed to index using it.
 ...
}
Analyzers
Analyzers are settings that define how to recognize terms within text. For more information, see 
Search analyzers
.
Analyzers can be helpful if you need to 
index multiple languages
.
The following table shows a list of generic analyzers that are supported by IBM Cloudant search:
Table 2. Generic analyzers
Analyzer
Description
classic
The standard Lucene analyzer, circa version 3.1.
email
Like the 
standard
 analyzer, but tries harder to match an email address as a complete token.
keyword
Input isn't tokenized at all.
simple
Divides text at nonletters.
standard
The default analyzer. It implements the Word Break rules from the 
Unicode™ text segmentation algorithm)
.
whitespace
Divides text at white-space boundaries.
See the following example analyzer document:
{
 
"_id"
:
 
"_design/analyzer_example"
,
 
"indexes"
:
 
{
  
"INDEX_NAME"
:
 
{
   
"index"
:
 
"function (doc) { ... }"
,
   
"analyzer"
:
 
"$ANALYZER_NAME"
  
}
 
}
}
Language-specific analyzers
These analyzers omit common words in the specific language, and many also 
remove prefixes and suffixes
. The name of the language is also the
name of the 
analyzer.
arabic
armenian
Cloudant
   
337basque
bulgarian
brazilian
catalan
cjk
 (Chinese, Japanese, Korean)
chinese
 (
smartcn
)
czech
danish
dutch
english
finnish
french
german
greek
galician
hindi
hungarian
indonesian
irish
italian
japanese
 (
kuromoji
)
latvian
norwegian
persian
polish
 (
stempel
)
portuguese
romanian
russian
spanish
swedish
thai
turkish
Per-field analyzers
The 
perfield
 analyzer configures many analyzers for different fields.
See the following example that defines different analyzers for different fields:
{
 
"_id"
:
 
"_design/analyzer_example"
,
 
"indexes"
:
 
{
  
"INDEX_NAME"
:
 
{
   
"analyzer"
:
 
{
    
"name"
:
 
"perfield"
,
    
"default"
:
 
"english"
,
    
"fields"
:
 
{
     
"spanish"
:
 
"spanish"
,
     
"german"
:
 
"german"
    
}
   
}
,
   
"index"
:
 
"function (doc) { ... }"
  
}
 
}
 Note: 
Language-specific analyzers are optimized for the specified language. You can't combine a generic analyzer with a language-specific
analyzer. Instead, you might use a 
perfield
 analyzer
 to select 
different analyzers for different fields within the documents.
Cloudant
   
338}
Stop words
Stop words are words that don't get indexed. You define them within a design document by turning the analyzer string into an object.
The default stop words for the 
standard
 analyzer are included in the following list:
$ 
 
"a"
,
 
"an"
,
 
"and"
,
 
"are"
,
 
"as"
,
 
"at"
,
 
"be"
,
 
"but"
,
 
"by"
,
 
"for"
,
 
"if"
,
 
 
"in"
,
 
"into"
,
 
"is"
,
 
"it"
,
 
"no"
,
 
"not"
,
 
"of"
,
 
"on"
,
 
"or"
,
 
"such"
,
 
 
"that"
,
 
"the"
,
 
"their"
,
 
"then"
,
 
"there"
,
 
"these"
,
 
"they"
,
 
"this"
,
 
 
"to"
,
 
"was"
,
 
"will"
,
 
"with"
 
See the following example that defines nonindexed ('stop') words:
{
 
"_id"
:
 
"_design/stop_words_example"
,
 
"indexes"
:
 
{
  
"INDEX_NAME"
:
 
{
   
"analyzer"
:
 
{
    
"name"
:
 
"portuguese"
,
    
"stopwords"
:
 
[
     
"foo"
,
     
"bar"
,
     
"baz"
    
]
   
}
,
   
"index"
:
 
"function (doc) { ... }"
  
}
 
}
}
Testing analyzer tokenization
You can test the results of analyzer tokenization by posting sample data to the 
_search_analyze
 endpoint.
See the following example that uses HTTP to test the 
keyword
 analyzer:
Host
: 
$ACCOUNT.cloudant.com
POST
 
/_search_analyze
 
HTTP/1.1
Content-Type
: 
application/json
{"analyzer":"keyword", "text":"ablanks@renovations.com"}
See the following example that uses the command line to test the 
keyword
 analyzer:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/_search_analyze"
 \
 -H 
"Content-Type: application/json"
 \
 -d 
'{"analyzer":"keyword", "text":"ablanks@renovations.com"}'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostSearchAnalyzeOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchAnalyzeResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostSearchAnalyzeOptions
 
searchAnalyzerOptions
 
=
    
new
 
PostSearchAnalyzeOptions
.Builder()
        .analyzer(
"keyword"
)
        .text(
"ablanks@renovations.com"
)
        .build();
 Tip: 
The 
keyword
, 
simple
, and 
whitespace
 analyzers don't support stop words.
Cloudant
   
339SearchAnalyzeResult
 
response
 
=
    service.postSearchAnalyze(searchAnalyzerOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postSearchAnalyze
({
 
analyzer
: 
'keyword'
,
 
text
: 
'ablanks@renovations.com'
,
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_search_analyze(
 analyzer=
'keyword'
,
 text=
'ablanks@renovations.com'
).get_result()
print
(response)
Go
postSearchAnalyzeOptions := service.NewPostSearchAnalyzeOptions(
 
"keyword"
,
 
"ablanks@renovations.com"
,
)
searchAnalyzeResult, _, err := service.PostSearchAnalyze(postSearchAnalyzeOptions)
if
 err != 
nil
 {
 
panic
(err)
}
b, _ := json.MarshalIndent(searchAnalyzeResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following result that tests the 
keyword
 analyzer:
{
 
"tokens"
:
 
[
  
"ablanks@renovations.com"
 
]
}
See the following example that uses HTTP to test the 
standard
 analyzer:
Cloudant
   
340Host
: 
$ACCOUNT.cloudant.com
POST
 
/_search_analyze
 
HTTP/1.1
Content-Type
: 
application/json
{"analyzer":"standard", "text":"ablanks@renovations.com"}
See the following example that uses the command line to test the 
standard
 analyzer:
curl 
"https://
$ACCOUNT
.cloudant.com/_search_analyze"
 -H 
"Content-Type: application/json"
 -d 
'{"analyzer":"standard", "text":"ablanks@renovations.com"}'
See the following result of testing the 
standard
 analyzer:
{
 
"tokens"
:
 
[
  
"ablanks"
,
  
"renovations.com"
 
]
}
Queries
After you create a search index, you can query it.
Run a partition query by using the following request:
GET /$DATABASE/_partition/$PARTITION_KEY/_design/$DDOC/_search/$INDEX_NAME
Run a global query by using the following request:
GET /$DATABASE/_design/$DDOC/_search/$INDEX_NAME
Specify your search by using the 
query
 parameter.
See the following example that uses HTTP to query a partitioned index:
GET
 
/$DATABASE/_partition/$PARTITION_KEY/_design/$DDOC/_search/$INDEX_NAME?include_docs=true&query="*:*"&limit=1
 
HTTP/1.1
Content-Type
: 
application/json
Host
: 
$ACCOUNT.cloudant.com
See the following example that uses the command line to query a partitioned index:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/
$DATABASE
/_partition/
$PARTITION_KEY
/_design/
$DDOC
/_search/
$INDEX_NAME
?
include_docs=true&query=\"*:*\"&limit=1"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostPartitionSearchOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostPartitionSearchOptions
 
searchOptions
 
=
    
new
 
PostPartitionSearchOptions
.Builder()
  .db(
"<db-name>"
)
  .partitionKey(
"<partition-key>"
)
  .ddoc(
"<ddoc>"
)
  .index(
"<index-name>"
)
  .query(
"*:*"
)
  .includeDocs(
true
)
  .limit(
1
)
  .build();
SearchResult
 
response
 
=
Cloudant
   
341    service.postPartitionSearch(searchOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postSearch
({
 
db
: 
'<db-name>'
,
 
partitionKey
: 
'<partition-key>'
,
 
ddoc
: 
'<ddoc>'
,
 
index
: 
'<index-name>'
,
 
query
: 
'*:*'
,
 
includeDocs
: 
true
,
 
limit
: 
1
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_search(
 db=
'<db-name>'
,
 partition_key=
'<partition-key>'
,
 ddoc=
'<ddoc>'
,
 index=
'<index-name>'
,
 query=
'*:*'
,
 include_docs=
True
,
 limit=
1
).get_result()
print
(response)
Go
postPartitionSearchOptions := service.NewPostPartitionSearchOptions(
 
"<db-name>"
,
 
"<partition-key>"
,
 
"<ddoc>"
,
 
"<index-name>"
,
 
"*:*"
,
)
postPartitionSearchOptions.SetIncludeDocs(
true
)
postPartitionSearchOptions.SetLimit(
1
)
searchResult, _, err := service.PostPartitionSearch(postPartitionSearchOptions)
if
 err != 
nil
 {
 
panic
(err)
}
b, _ := json.MarshalIndent(searchResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
Cloudant
   
342   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example that uses HTTP to query a global index:
GET
 
/$DATABASE/_design/$DDOC/_search/$INDEX_NAME?include_docs=true&query="*:*"&limit=1
 
HTTP/1.1
Content-Type
: 
application/json
Host
: 
$ACCOUNT.cloudant.com
See the following example that uses the command line to query a global index:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/
$DATABASE
/_design/
$DDOC
/_search/
$INDEX_NAME
?include_docs=true&query=\"*:*\"&limit=1"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostSearchOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostSearchOptions
 
searchOptions
 
=
 
new
 
PostSearchOptions
.Builder()
    .db(
"<db-name>"
)
    .ddoc(
"<ddoc>"
)
    .index(
"<index-name>"
)
    .query(
"*:*"
)
 .includeDocs(
true
)
 .limit(
1
)
    .build();
SearchResult
 
response
 
=
    service.postSearch(searchOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postSearch
({
 
db
: 
'<db-name>'
,
 
ddoc
: 
'<ddoc>'
,
 
index
: 
'<index-name>'
,
 
query
: 
'*:*'
,
 
includeDocs
: 
true
,
 
limit
: 
1
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_search(
 db=
'<db-name>'
,
 ddoc=
'<ddoc>'
,
 index=
'<index-name>'
,
 query=
'*:*'
,
 include_docs=
True
,
 limit=
1
Cloudant
   
343).get_result()
print
(response)
Go
postSearchOptions := service.NewPostSearchOptions(
 
"<db-name>"
,
 
"<ddoc>"
,
 
"<index-name>"
,
 
"*:*"
,
)
postSearchOptions.SetIncludeDocs(
true
)
postSearchOptions.SetLimit(
1
)
searchResult, _, err := service.PostSearch(postSearchOptions)
if
 err != 
nil
 {
 
panic
(err)
}
b, _ := json.MarshalIndent(searchResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
Query Parameters
Argument
Description
Optional
Type
Supported Values
Partition
Query
bookmark
A bookmark that was received
from a previous search. This
parameter enables paging
through the results. If no results
exist after the bookmark, you
get a response with an empty
rows array and the same
bookmark, confirming the end
of 
the result list.
yes
String
Yes
counts
This field defines an array of
names of string fields, for which
counts are requested. The
response includes counts for
each unique value of this field
name among the documents
that match the search query.
Faceting
 
must be enabled for
this parameter to function.
Yes
JSON
A JSON array of field names.
No
 Important: 
You must enable 
faceting
 before you can use the following parameters: 
counts
 and 
drilldown
.
Cloudant
   
344drilldown
This field can be used several
times. Each use defines a pair of
a field name and a value. The
search matches only
documents that include the
value that was provided in the
named field. It differs from
using 
"fieldname:value"
 
in
the 
q
 parameter only in that the
values aren't analyzed.
Faceting
 must be enabled for
this parameter to function.
No
JSON
A JSON array that includes two
elements: the field name and the value.
Yes
group_field
Field by which to group search
matches.
Yes
String
A string that includes the name of a
string field. Fields that include other
data such as numbers, objects, or
arrays can't be used.
No
group_limit
Maximum group count. This
field can be used only if
group_field
 is specified.
Yes
Numeric
No
group_sort
This field defines the order of
the groups in a search that uses
group_field
. The default sort
order is relevance.
Yes
JSON
This field can have the same values as
the sort field, so single fields and arrays
of fields are supported.
No
highlight_fields
Specifies which fields to
highlight. If specified, the result
object includes a 
highlights
field with an entry for each
specified field.
Yes
Array of
strings
Yes
highlight_pre_tag
A string that is inserted before
the highlighted word in the
highlights output.
Yes,
defaults
to 
<em>
String
Yes
highlight_post_tag
A string that is inserted after the
highlighted word in the
highlights output.
Yes,
defaults
to 
</em>
String
Yes
highlight_number
Number of fragments that are
returned in highlights. If the
search term exceeds the
fragment size, then the entire
search term is returned.
Yes,
defaults
to 1
Numeric
Yes
highlight_size
Slice up field content into
number of characters, so-called
fragments, and highlights
matches only inside the
specified fragments.
Yes,
defaults
to 100
characters
Numeric
Yes
include_docs
Include the full content of the
documents in the response.
Yes
Boolean
Yes
include_fields
A JSON array of field names to
include in search results. Any
fields that are included must be
indexed with the 
store:true
option.
Yes, the
default is
all fields.
Array of
strings
Yes
Cloudant
   
345Table 3. Query parameters
limit
Limit the number of the
returned documents to the
specified number. For a
grouped search, this parameter
limits the number of documents
per group.
Yes
Numeric
The limit value can be any positive
integer number up to and including
200.
Yes
q
Abbreviation for 
query
. Runs a
Lucene query.
No
String or
Number
Yes
query
Runs a Lucene query.
No
String or
Number
Yes
ranges
This field defines ranges for
faceted, numeric search fields.
The value is a JSON object
where the fields names are
faceted numeric search fields,
and the values of the fields are
JSON objects. The field names
of the JSON objects are 
names
for ranges. The values are
strings that describe the range,
for example 
"[0 TO 10]"
.
Yes
JSON
The value must be an object with fields
that have objects as their values. These
objects must have strings with ranges
as their field values.
No
sort
Specifies the sort order of the
results. In a grouped search
(when 
group_field
 is used),
this parameter specifies the sort
order within a group. The
default sort order is relevance.
Yes
JSON
A JSON string of the form
"fieldname<type>"
 or 
-
fieldname<type>
 for descending order.
The 
fieldname
 is the name of a String
or Number field, and 
type
 is either 
a
number, a string, or a JSON array of
strings. The 
type
 part is optional, and
defaults to 
number
. Some examples are
"foo"
, 
"-foo"
, 
"bar<string>"
, 
"-
foo<number>"
, and 
["-
foo<number>","bar<string>"]
. String
fields that are used for sorting must not
be analyzed fields. Fields that are used
for sorting must 
be indexed by the
same indexer that is used for the search
query.
Yes
stale
Do not wait for the index to
finish building to return results.
Yes
String
OK
Yes
Do not combine the 
bookmark
 and 
stale
 options. These options constrain the choice of shard replicas to use for the response. When used
together, the options might cause problems when you try to contact replicas that 
are slow or not available.
Relevance
When more than one result might be returned, it is possible for them to be sorted. By default, the sorting order is determined by 'relevance'.
Relevance is measured according to 
Apache Lucene Scoring
. As an example, if you search a simple database for the word 
example
, two documents
might contain the word. 
If one document mentions the word 
example
 10 times, but the second document mentions it only twice, then the first
document is considered to be more 'relevant'.
If you don't provide a 
sort
 parameter, relevance is used by default. The highest scoring matches are returned first.
If you provide a 
sort
 parameter, then matches are returned in that order, ignoring relevance.
If you want to use a 
sort
 parameter, and also include ordering by relevance in your search results, use the special fields 
-<score>
 or 
<score>
 Important: 
Using 
include_docs=true
 might have 
performance implications
.
Cloudant
   
346within the 
sort
 parameter.
POSTing search queries
Instead of using the 
GET
 HTTP method, you can also use 
POST
. The main advantage of 
POST
 queries is that they can have a request body, so you
can specify the request as a JSON object. Each parameter in 
the previous table corresponds to a field in the JSON object in the request body.
See the following example that uses HTTP to 
POST
 a search request:
POST
 
/db/_design/ddoc/_search/searchname
 
HTTP/1.1
Content-Type
: 
application/json
Host
: 
$ACCOUNT.cloudant.com
See the following example that uses the command line to 
POST
 a search request:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/
$DATABASE
/_design/
$DDOC
/_search/
$INDEX_NAME
"
 -X POST -H 
"Content-Type:
 
application/json"
 -d @search.json
See the following example JSON document that includes a search request:
{
    
"q"
:
 
"index:my query"
,
    
"sort"
:
 
"foo"
,
    
"limit"
:
 
3
}
Query syntax
The IBM Cloudant search query syntax is based on the 
Lucene syntax
. Search queries take the form of 
name:value
 unless 
the name is omitted, in
which case they use the default field, as demonstrated in the following examples:
See the following example search query expressions:
// Birds
class:bird
// Animals that begin with the letter 
"l"
l*
// Carnivorous birds
class:bird AND diet:carnivore
// Herbivores that start with letter 
"l"
l* AND diet:herbivore
// Medium-sized herbivores
min_length:[1 TO 3] AND diet:herbivore
// Herbivores that are 2m long or less
diet:herbivore AND min_length:[-Infinity TO 2]
// Mammals that are at least 1.5m long
class:mammal AND min_length:[1.5 TO Infinity]
// Find 
"Meles meles"
latin_name:
"Meles meles"
// Mammals who are herbivore or carnivore
diet:(herbivore OR omnivore) AND class:mammal
// Return all results
*:*
Queries over multiple fields can be logically combined, and groups and fields can be further grouped. The available logical operators are case-
sensitive and are 
AND
, 
+
, 
OR
, 
NOT
, and 
-
. Range queries can run over strings or numbers.
Cloudant
   
347If you want a fuzzy search, you can run a query with 
~
 to find terms like the search term. For instance, 
look~
 finds the terms 
book
 and 
took
.
You can alter the importance of a search term by adding 
^
 and a positive number. This alteration creates matches that contain the term more or less
relevant, proportional to the power of the boost value. The default value is 1, 
which means no increase or decrease in the strength of the match. A
decimal value of 0 - 1 reduces importance, making the match strength weaker. A value greater than one increases importance, making the match
strength stronger.
Wildcard searches are supported, for both single (
?
) and multiple (
*
) character searches. For example, 
dat?
 would match 
date
 and 
data
, and
dat*
 would match 
date
, 
data
, 
database
, and 
dates
. Wildcards must come after the search term.
Use 
*:*
 to return all results.
Result sets from searches are limited to 200 rows, and return 25 rows by default. The number of rows that are returned can be changed by using the
limit
 parameter
.
If the search query does not specify the 
"group_field"
 argument, the response includes a bookmark. If this bookmark is later provided as a URL
parameter, the response skips the rows that were seen already, making it quick 
and easy to get the next set of results.
The response never includes a bookmark if the 
"group_field"
 parameter
 is included in the search query.
The following characters require escaping if you want to search on them:
+ - && || ! ( ) { } [ ] ^ " ~ * ? : \ /
To escape one of these characters, use a preceding backslash character (
\
).
The response to a search query includes an 
order
 field for each of the results. The 
order
 field is an array where the first element is the field or
fields that are specified in the 
sort
 parameter. If no 
sort
 parameter
 is included in the query, then the 
order
 field contains the 
Lucene relevance
score
. 
If you use the 
sort by distance
 feature as described in 
Geographical searches
, then the first element is the distance from a point. The
distance is measured by using either kilometers or miles.
Faceting
IBM Cloudant Search also supports faceted searching, which enables the discovery of aggregate information about matches quickly and easily. You
can match all documents by using the special 
?q=*:*
 query syntax, and use the returned 
facets to refine your query. To indicate that a field must be
indexed for faceted queries, set 
{"facet": true}
 in its options.
See the following example search query, specifying that faceted search is enabled:
function
(
doc
) {
    
index
(
"type"
, doc.
type
, {
"facet"
: 
true
});
    
index
(
"price"
, doc.
price
, {
"facet"
: 
true
});
}
To use facets, all the documents in the index must include all the fields that have faceting enabled. If your documents don't include all the fields, you
receive a 
bad_request
 error with the following reason, "The 
field_name
 
does not exist." If each document does not contain all the fields for
facets, create separate indexes for each field. If you don't create separate indexes for each field, you must include only documents that contain all
the fields. Verify 
that the fields exist in each document by using a single 
if
 statement.
See the following example 
if
 statement to verify that the required fields exist in each document:
if
 (
typeof
 doc.
town
 == 
"string"
 && 
typeof
 doc.
name
 == 
"string"
) {
        
index
(
"town"
, doc.
town
, {
facet
: 
true
});
        
index
(
"name"
, doc.
name
, {
facet
: 
true
});        
    }
 Note: 
If the higher bounds of a range query are both strings that contain only numeric digits, the bounds are treated as numbers not as
strings. For example, if you search by using the query 
mod_date:["20170101" TO "20171231"]
, 
the results include documents for which
mod_date
 is between the numeric values 20170101 and 20171231, not between the strings "20170101" and "20171231".
 Tip: 
The 
group_field
, 
group_limit
, and 
group_sort
 options are only available when you make global queries.
 Tip: 
The second element in the order array can be ignored. It is used for troubleshooting purposes only.
Cloudant
   
348Counts
The 
counts
 facet syntax takes a list of fields, and returns the number of query results for each unique value of each named field.
The 
count
 operation works only if the indexed values are strings. The indexed values can't be mixed types. For example, if 100 strings are indexed,
and one number, then the index can't be used for 
count
 operations. 
You can check the type by using the 
typeof
 operator, and convert it by using
the 
parseInt
, 
parseFloat
, or 
.toString()
 functions.
See the following example query that uses the 
counts
 facet syntax:
?q=*:*&counts=["type"]
See the following example response after you use the 
counts
 facet syntax:
{
    
"total_rows"
:
100000
,
    
"bookmark"
:
"g..."
,
    
"rows"
:
[
...
]
,
    
"counts"
:
{
        
"type"
:
{
            
"sofa"
:
 
10
,
            
"chair"
:
 
100
,
            
"lamp"
:
 
97
        
}
    
}
}
drilldown
You can restrict results to documents with a dimension equal to the specified label. Restrict the results by adding 
drilldown=
["dimension","label"]
 to a search query. You can include multiple 
drilldown
 
parameters to restrict results along multiple dimensions.
Using a 
drilldown
 parameter is similar to using 
key:value
 in the 
q
 parameter, but the 
drilldown
 parameter returns values that the analyzer
might skip.
For example, if the analyzer didn't index a stop word like 
"a"
, the 
drilldown
 parameter returns it when you specify 
drilldown=["key","a"]
.
Ranges
The 
range
 facet syntax reuses the standard Lucene syntax for ranges to return counts of results that fit into each specified category. Inclusive range
queries are denoted by brackets (
[
, 
]
). Exclusive 
range queries are denoted by curly brackets (
{
, 
}
).
The indexed values can't be mixed types. For example, if 100 strings are indexed, and one number, then the index can't be used for 
range
operations. You can check the type by using the 
typeof
 operator, and convert 
it by using the 
parseInt
, 
parseFloat
, or 
.toString()
 functions.
See the following example of a request that uses faceted search for matching 
ranges
:
?q=*:*&ranges={"price":{"cheap":"[0 TO 100]","expensive":"{100 TO Infinity}"}}
See the following example results after a 
ranges
 check on a faceted search:
{
    
"total_rows"
:
100000
,
    
"bookmark"
:
"g..."
,
    
"rows"
:
[
...
]
,
    
"ranges"
:
 
{
        
"price"
:
 
{
            
"expensive"
:
 
278682
,
 Tip: 
The 
counts
 option is only available when you make global queries.
 Tip: 
The 
drilldown
 option is only available when you make global queries.
 Tip: 
The 
ranges
 option is only available when you make global queries.
Cloudant
   
349            
"cheap"
:
 
257023
        
}
    
}
}
Geographical searches
In addition to searching by the content of textual fields, you can also sort your results by their distance from a geographic coordinate.
To sort your results in this way, you must index two numeric fields that represent the longitude and latitude.
You can then query by using the special 
<distance...>
 sort field, which takes five parameters:
Longitude field name - The name of your longitude field (
mylon
 in the example).
Latitude field name - The name of your latitude field (
mylat
 in the example).
Longitude of origin - The longitude of the place you want to sort by distance from.
Latitude of origin - The latitude of the place you want to sort by distance from.
Units - The units to use include, 
km
 for kilometers or 
mi
 for miles. The distance is returned in the order field.
You can combine sorting by distance with any other search query, such as range searches on the latitude and longitude, or queries that involve
nongeographical information.
That way, you can search in a bounding box, and narrow down the search with extra criteria.
See the following example geographical data:
{
    
"name"
:
"Aberdeen, Scotland"
,
    
"lat"
:
57.15
,
    
"lon"
:
-2.15
,
    
"type"
:
"city"
}
See the following example of a design document that includes a search index for the geographic data:
function
(
doc
) {
    
if
 (doc.
type
 && doc.
type
 == 
'city'
) {
        
index
(
'city'
, doc.
name
, {
'store'
: 
true
});
        
index
(
'lat'
, doc.
lat
, {
'store'
: 
true
});
        
index
(
'lon'
, doc.
lon
, {
'store'
: 
true
});
    }
}
See the following example that uses HTTP for a query that sorts cities in the northern hemisphere by their distance to New York:
GET
 
/examples/_design/cities-designdoc/_search/cities?q=lat:[0+TO+90]&sort="<distance,lon,lat,-74.0059,40.7127,km>"
 
HTTP/1.1
Host
: 
$ACCOUNT.cloudant.com
See the following example that uses the command line for a query that sorts cities in the northern hemisphere by their distance to New York:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/examples/_design/cities-designdoc/_search/cities?q=lat:\[0+TO+90\]&sort=\"
<distance,lon,lat,-74.0059,40.7127,km>\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostSearchOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchResult;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostSearchOptions
 
searchOptions
 
=
 
new
 
PostSearchOptions
.Builder()
Cloudant
   
350 .db(
"examples"
)
 .ddoc(
"cities-designdoc"
)
 .index(
"cities"
)
 .query(
"lat:\\[0+TO+90\\]"
)
 .sort(Arrays.asList(
"<distance,lon,lat,-74.0059,40.7127,km>"
))
 .build();
SearchResult
 
response
 
=
    service.postSearch(searchOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postSearch
({
 
db
: 
'examples'
,
 
ddoc
: 
'cities-designdoc'
,
 
index
: 
'cities'
,
 
query
: 
'lat:\\[0+TO+90\\]'
,
 
sort
: [
'<distance,lon,lat,-74.0059,40.7127,km>'
]
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_search(
 db=
'examples'
,
 ddoc=
'cities-designdoc'
,
 index=
'cities'
,
 query=
'lat:\\[0+TO+90\\]'
,
 sort=[
'<distance,lon,lat,-74.0059,40.7127,km>'
]
).get_result()
print
(response)
Go
postSearchOptions := service.NewPostSearchOptions(
 
"examples"
,
 
"cities-designdoc"
,
 
"cities"
,
 
"lat:\\[0+TO+90\\]"
,
)
postSearchOptions.SetSort([]
string
{
"<distance,lon,lat,-74.0059,40.7127,km>"
})
searchResult, _, err := service.PostSearch(postSearchOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(searchResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
Cloudant
   
351   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example (abbreviated) response that includes a list of northern hemisphere cities that are sorted by distance to New York:
{
    
"total_rows"
:
 
205
,
    
"bookmark"
:
 
"g1A...XIU"
,
    
"rows"
:
 
[
        
{
            
"id"
:
 
"city180"
,
            
"order"
:
 
[
                
8.530665755719783
,
                
18
            
]
,
            
"fields"
:
 
{
                
"city"
:
 
"New York, N.Y."
,
                
"lat"
:
 
40.78333333333333
,
                
"lon"
:
 
-73.96666666666667
            
}
        
}
,
        
{
            
"id"
:
 
"city177"
,
            
"order"
:
 
[
                
13.756343205985946
,
                
17
            
]
,
            
"fields"
:
 
{
                
"city"
:
 
"Newark, N.J."
,
                
"lat"
:
 
40.733333333333334
,
                
"lon"
:
 
-74.16666666666667
            
}
        
}
,
        
{
            
"id"
:
 
"city178"
,
            
"order"
:
 
[
                
113.53603438866077
,
                
26
            
]
,
            
"fields"
:
 
{
                
"city"
:
 
"New Haven, Conn."
,
                
"lat"
:
 
41.31666666666667
,
                
"lon"
:
 
-72.91666666666667
            
}
        
}
    
]
}
Highlighting search terms
Sometimes it is useful to get the context in which a search term was mentioned so that you can show more emphasized results to a user.
To get more emphasized results, add the 
highlight_fields
 parameter to the search query. Specify the field names for which you would like
excerpts, with the highlighted search term returned.
By default, the search term is placed in 
<em>
 tags to highlight it, but the highlight can be overridden by using the 
highlights_pre_tag
 and
highlights_post_tag
 parameters.
The length of the fragments is 100 characters by default. A different length can be requested with the 
highlights_size
 parameter.
The 
highlights_number
 parameter controls the number of fragments that are returned, and defaults to 1.
In the response, a 
highlights
 field is added, with one subfield per field name.
For each field, you receive an array of fragments with the search term highlighted.
 Tip: 
For highlighting to work, store the field in the index by using the 
store: true
 option.
Cloudant
   
352See the following example that uses HTTP to search with highlighting enabled:
GET
 
/movies/_design/searches/_search/movies?q=movie_name:Azazel&highlight_fields=["movie_name"]&highlight_pre_tag="
 
"&highlight_post_tag=" 
"&highlights_size=30&highlights_number=2
 
HTTP/1.1
HOST
: 
$ACCOUNT.cloudant.com
Authorization
: 
...
See the following example that the command line to search with highlighting enabled:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/movies/_design/searches/_search/movies?q=\"movie_name:Azazel\"&highlight_fields=\
[\"movie_name\"\]&highlight_pre_tag=\" \"&highlight_post_tag=\" \"&highlights_size=30&highlights_number=2"
 \
 -X GET
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostSearchOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchResult;
import
 java.util.Arrays;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostSearchOptions
 
searchOptions
 
=
 
new
 
PostSearchOptions
.Builder()
    .db(
"movies"
)
    .ddoc(
"searches"
)
    .index(
"movies"
)
    .query(
"movie_name:Azazel"
)
    .highlightFields(Arrays.asList(
"[\"movie_name\"]"
))
    .highlightPreTag(
"\" \""
)
    .highlightPostTag(
"\" \""
)
    .highlightSize(
30
)
    .highlightNumber(
2
)
    .build();
SearchResult
 
response
 
=
    service.postSearch(searchOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postSearch
({
 
db
: 
'movies'
,
 
ddoc
: 
'searches'
,
 
index
: 
'movies'
,
 
query
: 
'movie_name:Azazel'
,
 
highlightFields
: [
'["movie_name"]'
],
 
highlightPreTag
: 
'" "'
,
 
highlightPostTag
: 
'" "'
,
 
highlightSize
: 
30
,
 
highlightNumber
: 
2
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
Cloudant
   
353response = service.post_search(
 db=
'movies'
,
 ddoc=
'searches'
,
 index=
'movies'
,
 query=
'movie_name:Azazel'
,
 highlight_fields=[
'["movie_name"]'
],
 highlight_pre_tag=
'" "'
,
 highlight_post_tag=
'" "'
,
 highlight_size=
30
,
 highlight_number=
2
).get_result()
print
(response)
Go
postSearchOptions := service.NewPostSearchOptions(
 
"movies"
,
 
"searches"
,
 
"movies"
,
 
"movie_name:Azazel"
,
)
postSearchOptions.SetHighlightFields([]
string
{
"[\"movie_name\"]"
})
postSearchOptions.SetHighlightPreTag(
"\" \""
)
postSearchOptions.SetHighlightPostTag(
"\" \""
)
postSearchOptions.SetHighlightSize(
30
)
postSearchOptions.SetHighlightNumber(
2
)
searchResult, _, err := service.PostSearch(postSearchOptions)
if
 err != 
nil
 {
 
panic
(err)
}
b, _ := json.MarshalIndent(searchResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
See the following example of highlighted search results:
{
    
"highlights"
:
 
{
        
"movie_name"
:
 
[
            
" on the Azazel Orient Express"
,
            
" Azazel manuals, you"
        
]
    
}
}
Search index metadata
To retrieve information about a search index, you send a 
GET
 request to the 
_search_info
 endpoint, as shown in the following example. 
DDOC
refers to the design document that includes the index, and 
INDEX_NAME
 is the name of the index.
See the following example that uses HTTP to request search index metadata:
GET
 
/$DATABASE/_design/$DDOC/_search_info/$INDEX_NAME
 
HTTP/1.1
Cloudant
   
354See the following example that uses the command line to request search index metadata:
Curl
curl 
"https://
$ACCOUNT
.cloudant.com/
$DATABASE
/_design/
$DDOC
/_search_info/
$INDEX_NAME
"
 \
     -X GET
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.GetSearchInfoOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchInfoResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetSearchInfoOptions
 
infoOptions
 
=
    
new
 
GetSearchInfoOptions
.Builder()
        .db(
"<db-name>"
)
        .ddoc(
"<ddoc>"
)
        .index(
"<index-name>"
)
        .build();
SearchInfoResult
 
response
 
=
    service.getSearchInfo(infoOptions).execute()
        .getResult();
System.out.println(response);
Node
import
 { 
Cloudant
V1 } 
from
 
'@ibm-cloud/cloudant'
;
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getSearchInfo
({
 
db
: 
'<db-name>'
,
 
ddoc
: 
'<ddoc>'
,
 
index
: 
'<index-name>'
}).
then
(
response
 =>
 {
 
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_search_info(
 db=
'<db-name>'
,
 ddoc=
'<ddoc>'
,
 index=
'<index-name>'
).get_result()
print
(response)
Go
getSearchInfoOptions := service.NewGetSearchInfoOptions(
 
"<db-name>"
,
 
"<ddoc>"
,
 
"<index-name>"
,
)
searchInfoResult, _, err := service.GetSearchInfo(getSearchInfoOptions)
if
 err != 
nil
 {
  
panic
(err)
}
Cloudant
   
355b, _ := json.MarshalIndent(searchInfoResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
The response includes information about your index, such as the number of documents in the index and the size of the index on disk.
See the following example response after you request search index metadata:
{
    
"name"
:
 
"_design/DDOC/INDEX"
,
    
"search_index"
:
 
{
        
"pending_seq"
:
 
7125496
,
        
"doc_del_count"
:
 
129180
,
        
"doc_count"
:
 
1066173
,
        
"disk_size"
:
 
728305827
,
        
"committed_seq"
:
 
7125496
    
}
}
Search analyzers
IBM® Cloudant® for IBM Cloud® Search is the free-text search technology that is built into the IBM Cloudant database that is powered by 
Apache
Lucene
.
When you create an IBM Cloudant Search index, you must consider which fields from your documents need to be indexed, and how they are to be
indexed.
One aspect of the indexing process is the choice of analyzer. An analyzer is code that can have the following effect:
Make the search case-insensitive by ensuring the string is lowercase.
Tokenize the string by breaking a sentence into individual words.
Stem the words by removing language-specific word endings, for example, farmer becomes farm.
Remove stop words by ignoring words like 
a
, 
is
, or 
if
, which can make the index smaller and more efficient.
At indexing-time, source data is processed by using the analyzer logic sorts and stores data in the index. At query-time, the search terms are
processed by using the same analyzer code before it interrogates the index.
Testing the analyzer
If you want to see the effect of each analyzer, use the 
IBM Cloudant Search API call
 that applies to one of the built-in Lucene analyzers with a
supplied 
string.
To look at each analyzer in turn, you can pass the following string to each analyzer to measure the effect:
"My name is Chris Wright-Smith. I live at 21a Front Street, Durham, UK - my email is chris7767@aol.com."
Standard analyzer
The Standard analyzer changes the string in the following ways:
Removes punctuation.
Splits words based on spaces and punctuation.
Removes stop words, including "is" and "at".
Changes words to use lowercase letters.
Note how "aol.com" stays intact.
Cloudant
   
356{
"tokens"
:
[
"my"
,
 
"name"
,
 
"chris"
,
 
"wright"
,
 
"smith"
,
 
"i"
,
 
"live"
,
 
"21a"
,
 
"front"
,
 
"street"
,
 
"durham"
,
 
"uk"
,
 
"my"
,
 
"email"
,
 
"chris7767"
,
 
"aol.com"
]
}
Keyword analyzer
With the Keyword analyzer, the string stays intact. See the following example:
{
"tokens"
:
[
"My name is Chris Wright-Smith. I live at 21a Front Street, Durham, UK - my email is chris7767@aol.com."
]
}
Simple analyzer
The Simple analyzer changes the string in the following ways:
Removes punctuation.
Splits words based on spaces and punctuation.
No stop words removed (notice "is" and "at").
Changes words to use lowercase letters.
Note how 
chris7767
 changes to 
chris
 and 
21a
 changes to 
a
.
{
"tokens"
:
[
"my"
,
 
"name"
,
 
"is"
,
 
"chris"
,
 
"wright"
,
 
"smith"
,
 
"i"
,
 
"live"
,
 
"at"
,
 
"a"
,
 
"front"
,
 
"street"
,
 
"durham"
,
 
"uk"
,
 
"my"
,
 
"email"
,
 
"is"
,
 
"chris"
,
 
"aol"
,
"com"
]
}
White space analyzer
The White space analyzer changes the string in the following ways:
Removes some punctuation.
Splits words on spaces.
No stop words removed (notice "is" and "at").
Words remain case-sensitive.
Note how email stays intact.
{
"tokens"
:
[
"My"
,
 
"name"
,
 
"is"
,
 
"Chris"
,
 
"Wright-Smith."
,
 
"I"
,
 
"live"
,
 
"at"
,
 
"21a"
,
 
"Front"
,
 
"Street,"
,
 
"Durham,"
,
 
"UK"
,
 
"-"
 
,
 
"my"
 
,
"email"
,
 
"is"
,
 
"chris7767@aol.com."
]
}
Classic analyzer
The Classic analyzer changes the string in the following ways:
Removes punctuation.
Splits words based on spaces and punctuation.
Removes stop words (no "is" or "at").
Changes words to use lowercase letters.
Note how email stays intact.
{
"tokens"
:
[
"my"
,
 
"name"
,
 
"chris"
,
 
"wright"
,
 
"smith"
,
 
"i"
,
 
"live"
,
 
"21a"
,
 
"front"
,
 
"street"
,
 
"durham"
,
 
"uk"
,
 
"my"
,
 
"email"
,
 
"chris7767@aol.com"
]
}
English analyzer
The English analyzer changes the string in the following ways:
Removes punctuation.
Splits words based on spaces and punctuation.
Stems words (notice "
chris
" changes to "
chri
").
Removes stop words (no "is" or "at").
Changes words to use lowercase letters.
Note how email stays intact.
{
"tokens"
:
[
"my"
,
 
"name"
,
"chri"
,
 
"wright"
,
 
"smith"
,
 
"i"
,
 
"live"
,
 
"21a"
,
 
"front"
,
 
"street"
,
 
"durham"
,
 
"uk"
,
 
"my"
,
 
"email"
,
 
Cloudant
   
357"chris7767"
,
"aol.com"
]
}
Language-specific analyzers make the most changes to the source data. See the following two examples:
The quick brown fox jumped over the lazy dog.
{
"tokens"
:[
"quick"
,
"brown"
,
"fox"
,
"jump"
,
"over"
,
"lazi"
,
"dog"
]}
Four score and seven years ago our fathers brought forth, on this continent, a new nation, conceived 
in
 Liberty, and
 
dedicated to the proposition that all men are created equal.
{
"tokens"
:
[
"four"
,
"score"
,
"seven"
,
"year"
,
"ago"
,
"our"
,
"father"
,
"brought"
,
"forth"
,
"contin"
,
"new"
,
"nation"
,
"conceiv"
,
"liberti"
,
"dedic"
,
"proposit"
,
"all"
}
Which analyzer must I pick?
It depends on your data. If your data is structured (email addresses, postal codes, names, and so on) in separate fields, then select an analyzer that
retains the data you need to search.
Only index the fields that you need. Keeping the index small helps to improve performance.
Consider the common data sources and look at the best analyzer choices.
Names
It's likely that name fields must use an analyzer that doesn't stem words. The White space analyzer keeps the words' case (meaning the search
terms must be full, case-sensitive matches) and leaves double-barreled names intact. If you want 
to split up double-barreled names, then the
Standard analyzer can do the job.
Email addresses
The built-in email analyzer serves this purpose, which changes everything to lowercase and then behaves like the Keyword analyzer.
Unique ID
Order numbers, payment references, and UUIDs such as "A1324S", "PayPal0000445", and "ABC-1412-BBG" must be kept without any pre-
processing, so the Keyword analyzer is preferred.
Country codes
Country codes like "UK" must also use the Keyword analyzer to prevent the removal of "stopwords" that match the country codes, for example, "IN"
for India. The Keyword analyzer is case-sensitive.
Text
It is best to process a block of free-form text with a language-specific analyzer, such as the English analyzer, or in a more general case, the Standard
analyzer.
Which option is best?
When IBM Cloudant returns data from a search, you can choose between the following options: 
store: true
 or 
include_docs=true
. See the
following descriptions:
a
. 
At index-time, choose the 
{store: true}
 option. This option indicates that the field you're dealing with needs to be stored inside the index. A
field can be "stored" even if it isn't used for indexing itself. For example, 
you might want to "store" a telephone number, even if your search
algorithm doesn't include searching by phone number.
b
. 
At query-time, pass 
?include_docs=true
 to indicate to IBM Cloud that you want the entire body of each matching document to be returned.
The first option means you have a larger index, but it's the fastest way of retrieving data. The second option keeps the index small, but adds extra
query-time work for IBM Cloud as it must fetch document bodies after the search result set is 
calculated. This process can be slower to run and adds
a further burden to the IBM Cloud cluster.
If possible, choose the first option use the following guidelines:
Index only the fields that you want to be searchable.
Store only the fields that you need to retrieve at query-time.
Cloudant
   
358Entity extraction
Providing a good search experience depends on the alignment of your users' search needs with structure in the data. Running lots of unstructured
data with an indexing engine gets you only so far. If you can add further structure to unstructured 
data, then the search experience benefits since
fewer "false positives" are returned. Look at this example:
"Edinson Cavani scored two superb goals as Uruguay beat Portugal to set up a World Cup quarter-final meeting with France.
 
Defeat for the European champions finished Cristiano Ronaldo's hopes of success in Russia just hours after Lionel Messi and
 
Argentina were knocked out, beaten 4-3 by Les Bleus."
Source: BBC News https://www.bbc.co.uk/sport/football/44439361
From this snippet, I would manually extract the following "entities".
Edinson Cavani - a footballer
Uruguay - a country
Portugal - another country
World Cup - a football competition
Cristiano Ronaldo - a footballer
Russia - a country
Lionel Messi - a footballer
Argentina - a country
Les Bleus - a nickname of the French national football team
Entity extraction is the process of locating known entities (given a database of such entities) and storing the entities in the search engine instead of,
or as well as, the source text. The 
Watson Natural Language and Understanding API
 
can be fed raw text and returns entities it knows about (you can
provide your own entity model for your domain-specific application):
Cloudant
   
359Figure 1. Analyzers
As well as entities, the API can also place the article in a hierarchy of categories. In this case, Watson suggests the following categories:
Travel, tourist destinations France
Sports, soccer
Sports, football
You can pre-process your raw data by calling the Watson API for each document and storing a list of entities, concepts, and categories in your IBM
Cloud document. This pre-processing provides automatic metadata about your free-text information. 
It can also provide an easier means to search
and navigate your app.
Pagination and bookmarks
Bookmarks help release the next page of results from a result set. While with pagination, you iterate through a range of documents efficiently.
You can use the 
skip
/
limit
 pattern to 
iterate through a result set
, but it gets progressively slower the larger the value of 
skip
.
IBM Cloudant Query
 and 
IBM Cloudant Search
 both use bookmarks as the key to unlock the next 
page of results from a result set. This practice is
described in full in a later section that is called 
Bookmarks
. It's less complicated to manage since no key manipulation is required to formulate the
request for the 
next result set. You pass the bookmark that was received in the first response to the second request.
Now, you can see a better way to page through a large document set.
Paging with 
_all_docs
 and views
If you use the 
GET
 or 
POST
 
$SERVICE_URL/$DATABASE/_all_docs
 endpoint to fetch documents in bulk, then you might see the 
limit
 and 
skip
parameters. By using these parameters, you 
can define how many documents you would like, and the offset into the range you want to start from.
Using the 
skip
/
limit
 pattern to iterate through results works, but it gets progressively slower the larger the value 
of 
skip
.
What is the 
_all_docs
 endpoint?
The 
GET
 and 
POST
 
$SERVICE_URL/$DATABASE/_all_docs
 are used to fetch data from an IBM Cloudant database's 
primary index
, that is, the index
that keeps each document's 
_id
 in order. 
The 
_all_docs
 endpoint takes a number of optional parameters that configure the range of data that is
requested and whether to return each document's body or not. With no parameters provided, 
_all_docs
 streams all 
of a database's documents,
returning only the document 
_id
 and its current 
_rev
 token.
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 -X GET 
"
$SERVICE_URL
/orders/_all_docs"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostAllDocsOptions
 
docsOptions
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .build();
AllDocsResult
 
response
 
=
    service.postAllDocs(docsOptions).execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postAllDocs
({
Cloudant
   
360  
db
: 
'orders'
,
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_all_docs(
  db=
'orders'
,
).get_result()
print
(response)
Go
postAllDocsOptions := service.NewPostAllDocsOptions(
  
"orders"
,
)
allDocsResult, response, err := service.PostAllDocs(postAllDocsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(allDocsResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
{
  
"total_rows"
: 11,
  
"offset"
: 0,
  
"rows"
: [
    {
      
"id"
: 
"4eee973603bf77f30b1f880ed83df76a"
,
      
"key"
: 
"4eee973603bf77f30b1f880ed83df76a"
,
      
"value"
: {
        
"rev"
: 
"1-3b5e6b73e57745787ad5627fe8f268c1"
      }
    },
    {
      
"id"
: 
"4eee973603bf77f30b1f880ed83f469a"
,
      
"key"
: 
"4eee973603bf77f30b1f880ed83f469a"
,
      
"value"
: {
        
"rev"
: 
"1-967a00dff5e02add41819138abb3284d"
      }
    }
...
If you supply 
include_docs=true
, then another 
doc
 attribute is added to each "row" in the result set that includes the document body.
The 
limit
, 
startkey
, and 
endkey
 parameters
Cloudant
   
361To access data from 
_all_docs
 in reasonably sized pages, you must supply the 
limit
 parameter to tell IBM Cloudant how many documents to
return:
# get me 5 documents
GET
 
$SERVICE_URL/$DATABASE/_all_docs?limit=5
 
HTTP/1.1
You can also limit the range of document 
_id
s that you want by supplying one or more values to 
startkey
 or 
endkey
.
Curl
# get me 5 documents from _id order00057 onwards
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=5&startkey=\"order00057\""
 \
    
# get me 5 documents between _id order00057 --> order00077
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?
limit=5&startkey=\"order00057\"&endkey=\"order00077\""
 \
    
# get me 5 documents up to _id order00077
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=5&endkey=\"order00077\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
// get me 5 documents from _id order00057 onwards
PostAllDocsOptions
 
docsOptions
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .startKey(
"order00057"
)
        .limit(
5
)
        .build();
AllDocsResult
 
response1
 
=
    service.postAllDocs(docsOptions).execute().getResult();
System.out.println(response1);
// get me 5 documents between _id order00057 --> order00077
PostAllDocsOptions
 
docsOptions2
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .startKey(
"order00057"
)
        .endKey(
"order00077"
)
        .limit(
5
)
        .build();
AllDocsResult
 
response2
 
=
    service.postAllDocs(docsOptions2).execute().getResult();
System.out.println(response2);
// get me 5 documents up to _id order00077
PostAllDocsOptions
 
docsOptions3
 
=
    
new
 
PostAllDocsOptions
.Builder()
        .db(
"orders"
)
        .endKey(
"order00077"
)
        .limit(
5
)
        .build();
AllDocsResult
 
response3
 
=
        service.postAllDocs(docsOptions3).execute().getResult();
System.out.println(response3);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
Cloudant
   
362// get me 5 documents from _id order00057 onwards
service.
postAllDocs
({
  
db
: 
'orders'
,
  
startKey
: 
'order00057'
,
  
limit
: 
5
}).
then
(
response1
 =>
 {
  
console
.
log
(response1.
result
);
});
// get me 5 documents from _id order00057 onwards
service.
postAllDocs
({
  
db
: 
'orders'
,
  
startKey
: 
'order00057'
,
  
endKey
: 
'order00077'
,
  
limit
: 
5
}).
then
(
response2
 =>
 {
  
console
.
log
(response2.
result
);
});
// get me 5 documents up to _id order00077
service.
postAllDocs
({
  
db
: 
'orders'
,
  
endKey
: 
'order00077'
,
  
limit
: 
5
}).
then
(
response3
 =>
 {
  
console
.
log
(response3.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
# get me 5 documents from _id order00057 onwards
response1 = service.post_all_docs(
  db=
'orders'
,
  start_key=
'order00057'
,
  limit=
5
).get_result()
print
(response1)
# get me 5 documents between _id order00057 --> order00077
response2 = service.post_all_docs(
  db=
'orders'
,
  start_key=
'order00057'
,
  end_key=
'order00077'
,
  limit=
5
).get_result()
print
(response2)
# get me 5 documents up to _id order00077
response3 = service.post_all_docs(
  db=
'orders'
,
  end_key=
'order00077'
,
  limit=
5
).get_result()
print
(response3)
Go
//  get me 5 documents from _id order00057 onwards
postAllDocsOptions1 := cloudantv1.PostAllDocsOptions{
 Db: core.StringPtr(
"orders"
),
 StartKey: core.StringPtr(
"order00057"
),
 Limit: core.Int64Ptr(
5
),
}
allDocsResult1, response1, err := service.PostAllDocs(postAllDocsOptions1)
if
 err != 
nil
 {
    
panic
(err)
Cloudant
   
363}
b, _ := json.MarshalIndent(allDocsResult1, 
""
, 
"  "
)
fmt.Println(
string
(b))
//  get me 5 documents between _id order00057 --> order00077
postAllDocsOptions2 := cloudantv1.PostAllDocsOptions{
    Db: core.StringPtr(
"orders"
),
    StartKey: core.StringPtr(
"order00057"
),
    EndKey: core.StringPtr(
"order00077"
),
    Limit: core.Int64Ptr(
5
),
}
allDocsResult2, response2, err := service.PostAllDocs(postAllDocsOptions2)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(allDocsResult2, 
""
, 
"  "
)
fmt.Println(
string
(b))
// get me 5 documents up to _id order00077
postAllDocsOptions3 := cloudantv1.PostAllDocsOptions{
    Db: core.StringPtr(
"orders"
),
    EndKey: core.StringPtr(
"order00077"
),
    Limit: core.Int64Ptr(
5
),
}
allDocsResult3, response3, err := service.PostAllDocs(postAllDocsOptions3)
if
 err != 
nil
 {
    
panic
(err)
}
b, _ := json.MarshalIndent(allDocsResult3, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
 
"github.com/IBM/go-sdk-core/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
This practice means you define the size of the data set and the range of the 
_id
 field to return, but that isn't quite the same as pagination.
Pagination options
For performance reasons, if you are displaying large amounts of data, you must consider using pagination. In these examples, documents are
fetched in blocks of five. However, in a real application, the page size might be different and depends 
on document size, latency demands, memory
consumption, and other tradeoffs.
You can use the options that are described in the following sections.
Option 1 - Fetch one document too many
Instead of fetching five documents (
limit=5
), fetch 5+1 (
limit=6
), but hide the sixth document from your users. The 
_id
 of the sixth document
becomes the 
startkey
 of your request for the 
next page of results.
See the following example of a first request:
Curl
The 
startkey
/
endkey
 values are in double quotation marks because they're expected to be JSON-encoded and
JSON.stringify('order00077') === "order00077"
.
Cloudant
   
364curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=6"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.DocsResultRow;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
int
 
pageSize
 
=
 
5
;
PostAllDocsOptions.
Builder
 
docsOptionsBuilder
 
=
        
new
 
PostAllDocsOptions
.Builder()
                .db(
"orders"
)
                .limit(pageSize + 
1
); 
// Fetch pageSize + 1 documents
AllDocsResult
 
response
 
=
        service.postAllDocs(docsOptionsBuilder.build())
        .execute()
        .getResult();
while
 (response.getRows().size() > 
1
) {
    List<DocsResultRow> responseDocuments = response.getRows();
    
// on the last page, show all documents:
    
if
 (responseDocuments.size() <= pageSize) {
        System.out.println(responseDocuments);
    } 
else
 { 
// otherwise, hide the last document:
        System.out.println(responseDocuments.subList(
0
, pageSize));
    }
    
// The startKey of the next request becomes the hidden document id:
    docsOptionsBuilder
        .startKey(responseDocuments
                    .get(responseDocuments.size() - 
1
)
                    .getId()
        );
    response =
        service.postAllDocs(docsOptionsBuilder.build())
        .execute()
        .getResult();
}
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
async
 
function
 
paginate
(
pageSize
) {
  
let
 allDocsResult = (
await
 service.
postAllDocs
({
    
db
: 
'orders'
,
    
limit
: pageSize + 
1
  })).
result
;
  
while
(allDocsResult.
rows
.
length
 > 
1
) {
    
let
 documents = allDocsResult.
rows
;
    
// on the last page, show all documents:
    
if
(documents.
length
 <= pageSize) {
      
console
.
log
(documents);
    } 
else
 { 
// otherwise, hide the last document:
      
console
.
log
(documents.
slice
(
0
, documents.
length
 - 
1
))
    }
    allDocsResult = (
await
 service.
postAllDocs
({
      
db
: 
'orders'
,
      
limit
: pageSize + 
1
,
      
startKey
: documents[documents.
length
 - 
1
].
id
    })).
result
;
  }
}
Cloudant
   
365paginate
(
5
)
Python
import
 json
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
page_size = 
5
response = service.post_all_docs(
  db=
'orders'
,
  limit=page_size+
1
,  
# Fetch page_size + 1 documents
).get_result()
while
 
len
(response[
"rows"
]) > 
1
:
  documents = response[
'rows'
]
  
# on the last page, show all documents:
  
if
 
len
(documents) <= page_size:
    
print
(json.dumps(documents, indent=
2
))
  
else
:  
# otherwise, hide the last document:
    
print
(json.dumps(documents[
0
:-
1
], indent=
2
))
  response = service.post_all_docs(
    db=
'orders'
,
    limit=page_size+
1
,  
# Fetch page_size + 1 documents
    start_key=documents[-
1
][
'id'
]
  ).get_result()
Go
pageSize := core.Int64Ptr(
5
)
postAllDocsOptions := service.NewPostAllDocsOptions(
    
"orders"
,
)
postAllDocsOptions.SetLimit(*pageSize + 
1
)
allDocsResult, _, err := service.PostAllDocs(postAllDocsOptions)
if
 err != 
nil
 {
    
panic
(err)
}
for
 
len
(viewResult.Rows) > 
1
 {
    documents := allDocsResult.Rows
    
// on the last page, show all documents:
    
if
 
int64
(
len
(documents)) <= *pageSize {
        b, err := json.MarshalIndent(documents, 
""
, 
"  "
)
        
if
 err != 
nil
 {
            
panic
(err)
        }
        fmt.Printf(
string
(b))
        } 
else
 { 
// otherwise, hide the last document:
            b, err := json.MarshalIndent(documents[
0
:*pageSize], 
""
, 
"  "
)
            
if
 err != 
nil
 {
                
panic
(err)
            }
            fmt.Printf(
string
(b))
        }
        
// The startKey of the next request becomes the hidden document id:
        postAllDocsOptions.SetStartKey(*documents[
len
(documents)
-1
].ID)
        allDocsResult, _, err = service.PostAllDocs(postAllDocsOptions)
        
if
 err != 
nil
 {
            
panic
(err)
        }
}
See the following example of a first response:
Curl
Cloudant
   
366{
  
"total_rows"
: 11,
  
"offset"
: 0,
  
"rows"
: [
    { 
"id"
: 
"4eee973603bf77f30b1f880ed83df76a"
 ....},
    { 
"id"
: 
"4eee973603bf77f30b1f880ed83f469a"
 ....},
    { 
"id"
: 
"65fa623a384648740ec1f39b495d591c"
 ....},
    { 
"id"
: 
"d7404903579d6d5880514c22ad983529"
 ....},
    { 
"id"
: 
"example"
 ....},
    { 
"id"
: 
"mydoc"
 ....} // <-- This is the 6th result we use as the startkey of the next request
   ]
}    
See the following example of a second request:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=6&startkey=\"mydoc\""
See the following example of a second response:
Curl
{
  
"total_rows"
: 11,
  
"offset"
: 5,
  
"rows"
: [
    { 
"id"
: 
"mydoc"
 ....},
    { 
"id"
: 
"order00057"
 ....},
    ...
   ]
} 
The previous Go example requires the following import block:
Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
 
"github.com/IBM/go-sdk-core/core"
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
This option works, but you end up fetching 
n+1
 documents when only 
n
 are required.
Option 2 - The \u0000 trick
If you're determined to fetch only 
n
 documents each time, then you need to calculate a value of 
startkey
, which means 
the next ID after the
last _id in the result set
. For example, if the last document 
in the first page of results is "example", what must the 
startkey
 of the next call
to 
_all_docs
 be? It can't be "example", otherwise you get the same document ID again. It turns out that you 
can append 
\u0000
 to the end of a
key string to indicate the "next key" (
\u0000
 is a Unicode null character, which can be placed in a URL as-is or with the percent code 
%00
). ).
See the following example of a first request:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=5"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.AllDocsResult;
import
 com.ibm.cloud.cloudant.v1.model.DocsResultRow;
import
 com.ibm.cloud.cloudant.v1.model.PostAllDocsOptions;
Cloudant
   
367Long
 
pageSize
 
=
 
5L
;
PostAllDocsOptions.
Builder
 
docsOptionsBuilder
 
=
        
new
 
PostAllDocsOptions
.Builder()
                .db(
"orders"
)
                .limit(pageSize); 
// Fetch pageSize documents
AllDocsResult
 
response
 
=
        service.postAllDocs(docsOptionsBuilder.build())
        .execute()
        .getResult();
while
 (response.getRows().size() > 
0
) {
    List<DocsResultRow> responseDocuments = response.getRows();
    System.out.println(responseDocuments);
    
// The startKey of the next request becomes the last document id appended with `\u0000`
    docsOptionsBuilder.startKey(
            responseDocuments
                    .get(responseDocuments.size() - 
1
)
                    .getId() + 
'\u0000'
    );
    response =
            service.postAllDocs(docsOptionsBuilder.build())
                    .execute()
                    .getResult();
}
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
async
 
function
 
paginate
(
n
) {
  
let
 allDocsResult = (
await
 service.
postAllDocs
({
    
db
: 
'orders'
,
    
limit
: n
  })).
result
;
  
while
 (allDocsResult.
rows
.
length
 > 
0
) {
    
let
 documents = allDocsResult.
rows
;
    
console
.
log
(documents);
    allDocsResult = (
await
 service.
postAllDocs
({
      
db
: 
'orders'
,
      
limit
: n,
      
startKey
: documents[documents.
length
 - 
1
].
id
 + 
'\u0000'
    })).
result
;
  }
}
paginate
(
5
)
Python
import
 json
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
page_size = 
5
response = service.post_all_docs(
    db=
'orders'
,
    limit=page_size,
).get_result()
while
 
len
(response[
"rows"
]) > 
0
:
    documents = response[
"rows"
]
    
print
(json.dumps(documents, indent=
2
))
    response = service.post_all_docs(
        db=
'orders'
,
        limit=page_size+
1
,  
# Fetch page_size + 1 documents
        start_key=documents[-
1
][
"id"
] + 
'\u0000'
Cloudant
   
368    ).get_result()
Go
pageSize := core.Int64Ptr(
5
)
postAllDocsOptions := service.NewPostAllDocsOptions(
    
"orders"
,
)
postAllDocsOptions.SetLimit(*pageSize)
allDocsResult, _, err := service.PostAllDocs(postAllDocsOptions)
if
 err != 
nil
 {
    
panic
(err)
}
for
 
len
(allDocsResult.Rows) > 
0
 {
    documents := allDocsResult.Rows
    b, err := json.MarshalIndent(documents, 
""
, 
"  "
)
    
if
 err != 
nil
 {
        
panic
(err)
    }
    fmt.Printf(
string
(b))
    
// The startKeyDocId of the next request becomes the last document id appended with `\u0000`
    postAllDocsOptions.SetStartKey(*documents[
len
(documents)
-1
].ID + 
"\u0000"
)
    allDocsResult, _, err = service.PostAllDocs(postAllDocsOptions)
    
if
 err != 
nil
 {
        
panic
(err)
    }
}
See the following example of a first response:
Curl
{
  
"total_rows"
: 11,
  
"offset"
: 0,
  
"rows"
: [
    { 
"id"
: 
"4eee973603bf77f30b1f880ed83df76a"
 ....},
    { 
"id"
: 
"4eee973603bf77f30b1f880ed83f469a"
 ....},
    { 
"id"
: 
"65fa623a384648740ec1f39b495d591c"
 ....},
    { 
"id"
: 
"d7404903579d6d5880514c22ad983529"
 ....},
    { 
"id"
: 
"example"
 ....} // <-- append \u0000 to this to get the startkey of the next request
   ]
}    
See the following example of a second request:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/orders/_all_docs?limit=5&startkey=\"example\u0000\""
See the following example of a second response:
Curl
{
  
"total_rows"
: 11,
  
"offset"
: 5,
  
"rows"
: [
    { 
"id"
: 
"mydoc"
 ....},
    { 
"id"
: 
"order00057"
 ....},
    ...
    { 
"id"
: 
"order00067"
 ....} <-- append \u0000 to this to get the startkey of the next request
   ]
} 
The previous Go example requires the following import block:
Cloudant
   
369Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
 
"github.com/IBM/go-sdk-core/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
Pagination of views
MapReduce views, secondary indexes, can be queried in a similar way to the 
_all_docs
 endpoint, but with the 
GET
 or 
POST
$SERVICE_URL/$DATABASE/_design/$DDOC/_view/$VIEW
 endpoint instead. MapReduce 
views are defined by 
key-value
 pairs that are produced
from user-supplied JavaScript functions. You can define your query in the following ways:
Spool all the data from a view with no parameters.
Include document bodies by supplying 
include_docs=true
.
Choose the range of keys that are required by using 
startkey
/
endkey
, but in this case, the data type of the keys might not be a string.
Another complication is that unlike the primary index, where every 
_id
 is unique, the secondary index might have entries with the same key. For
example, lots of entries that include the key 
"herbivore"
. This 
situation makes pagination by using only 
startkey
/
endkey
 tricky, so you can use
other parameters to help: 
startkey_docid
/
endkey_docid
.
See the following example of a first request:
Curl
# get first page of animals by diet
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/animaldb/_design/views101/_view/diet?
limit=3&startkey=\"herbivore\"&endkey=\"herbivore\""
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostViewOptions;
import
 com.ibm.cloud.cloudant.v1.model.ViewResult;
import
 com.ibm.cloud.cloudant.v1.model.ViewResultRow;
int
 
pageSize
 
=
 
3
;
String
 
diet
 
=
 
"herbivore"
;
PostViewOptions.
Builder
 
viewOptionsBuilder
 
=
        
new
 
PostViewOptions
.Builder()
                .db(
"animaldb"
)
                .ddoc(
"views101"
)
                .view(
"diet"
)
                .limit(pageSize) 
// Fetch pageSize documents
                .startKey(diet)
                .endKey(diet);
ViewResult
 
response
 
=
        service.postView(viewOptionsBuilder.build())
                .execute()
                .getResult();
while
 (response.getRows().size() > 
0
) {
    List<ViewResultRow> responseDocuments = response.getRows();
    System.out.println(responseDocuments);
    
// The startKeyDocId of the next request becomes the last document id appended with `\u0000`
    viewOptionsBuilder.startKeyDocId(
            responseDocuments
                    .get(responseDocuments.size() - 
1
)
                    .getId() + 
'\u0000'
    );
    response =
            service.postView(viewOptionsBuilder.build())
Cloudant
   
370                    .execute()
                    .getResult();
}
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
async
 
function
 
paginate
(
pageSize
) {
  
let
 diet = 
'herbivore'
;
  
let
 requestParams = {
    
db
: 
'animaldb'
,
    
ddoc
: 
'views101'
,
    
view
: 
'diet'
,
    
limit
: pageSize,
    
startKey
: diet,
    
endKey
: diet,
  };
  
let
 viewResult = (
await
 service.
postView
(requestParams)).
result
;
  
while
 (viewResult.
rows
.
length
 > 
0
) {
    
let
 documents = viewResult.
rows
;
    
console
.
log
(documents);
    
// The startKeyDocId of the next request becomes the last document id appended with `\u0000`
    requestParams.
startKeyDocId
 = documents[documents.
length
 - 
1
].
id
 + 
'\u0000'
;
    viewResult = (
await
 service.
postView
(requestParams)).
result
;
  }
}
paginate
(
3
)
Python
import
 json
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
page_size = 
3
diet = 
'herbivore'
request_params = d = 
dict
(
  db=
'animaldb'
,
  ddoc=
'views101'
,
  view=
'diet'
,
  limit=page_size,
  start_key=diet,
  end_key=diet,
)
response = service.post_view(**request_params).get_result()
while
 
len
(response[
"rows"
]) > 
0
:
  documents = response[
"rows"
]
  
print
(json.dumps(documents, indent=
2
))
  
# The startKeyDocId of the next request becomes the last document id appended with `\u0000`
  request_params[
'start_key_doc_id'
] = documents[-
1
][
"id"
] + 
'\u0000'
  response = service.post_view(**request_params).get_result()
Go
pageSize := core.Int64Ptr(
5
)
diet := 
"herbivore"
viewOptions := service.NewPostViewOptions(
    
"animaldb"
,
    
"views101"
,
    
"diet"
,
)
viewOptions.SetLimit(*pageSize)
viewOptions.SetStartKey(diet)
Cloudant
   
371viewOptions.SetEndKey(diet)
viewResult, _, err := service.PostView(viewOptions)
if
 err != 
nil
 {
    
panic
(err)
}
for
 
len
(viewResult.Rows) > 
0
 {
    documents := viewResult.Rows
    b, err := json.MarshalIndent(documents, 
""
, 
"  "
)
    
if
 err != 
nil
 {
        
panic
(err)
    }
    fmt.Printf(
string
(b))
    
// The startKeyDocId of the next request becomes the last document id appended with `\u0000`
    viewOptions.SetStartKey(*documents[
len
(documents)
-1
].ID + 
"\u0000"
)
    viewResult, _, err = service.PostView(viewOptions)
    
if
 err != 
nil
 {
        
panic
(err)
    }
}
See the following example of a first response:
Curl
{
  
"total_rows"
: 10,
  
"offset"
: 2,
  
"rows"
: [
    {
      
"id"
: 
"elephant"
,
      
"key"
: 
"herbivore"
,
      
"value"
: 1
    },
    {
      
"id"
: 
"giraffe"
,
      
"key"
: 
"herbivore"
,
      
"value"
: 1
    },
    {
      
"id"
: 
"llama"
, // <-- append \u0000 to the startkey_docid to of the next request
      
"key"
: 
"herbivore"
,
      
"value"
: 1
    }
  ]
}
See the following example of a second request:
Curl
# get next page of animals by diet
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/animaldb/_design/views101/_view/diet?
limit=3&startkey=\"herbivore\"&endkey=\"herbivore\"&startkey_docid=llama%00"
See the following example of a second response:
Curl
{
  
"total_rows"
: 10,
  
"offset"
: 5,
  
"rows"
: [
    {
      
"id"
: 
"zebra"
,
      
"key"
: 
"herbivore"
,
      
"value"
: 1
    }
Cloudant
   
372  ]
}
The previous Go example requires the following import block:
Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
 
"github.com/IBM/go-sdk-core/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
In other words, the second request has a value of 
startkey_docid
 that is the last document ID from the previous page of results (llama) plus the
magic 
\u0000
 character (which becomes 
llama%00
 in the URL).
Bookmarks
Imagine you're creating a web application that shows a set of search results, whether they be books, actors, or products in your store. As the user
scrolls through the search results, another page of matches is appended at the end. This behavior 
is known as an "infinite scroll" design pattern. It
allows the user to endlessly scroll through a large data set with ease, while they fetch only smaller batches of data from the database each time.
How do IBM Cloudant bookmarks work?
It's this sort of access pattern that IBM Cloudant 
bookmarks
 are built for. Here's how it works:
Your application runs a search on an IBM Cloudant database, for example, 
find me the first 10 cities where the country is "US"
.
IBM Cloudant provides an array of 10 IBM Cloudant documents and a 
bookmark
, an opaque key that represents a pointer to the next
documents in the result set.
When the next set of results is required, the search is repeated. However, the query is sent, with the bookmark from the first response, to IBM
Cloudant in the request.
IBM Cloudant replies with the second set of documents and another bookmark, which can be used to get a third page of results.
Repeat!
Now you can see how to do that with code.
How can I use IBM Cloudant Query to search?
First, you search for all the cities in the US. You're using 
IBM Cloudant Query
, so the operation is specified as a block of JSON:
$ 
{
  
"selector"
: {
    
"$eq"
: {
      
"country"
: 
"US"
    }
  },
  
"limit"
: 
5
}
By using the 
/db/_find
 API endpoint, the results are passed to IBM Cloudant.
Curl
curl -X POST \
      -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 \
      -H 
'Content-type: application/json'
 \
 Note: 
The 
startkey_docid
 parameter works only if a 
startkey
 is supplied and where all index entries share a key. If they don't share a
key, then pagination can be achieved with manipulation of 
startkey
/
endkey
 
parameters only. Also, the 
startkey_docid
 parameter is not
JSON encoded.
Cloudant
   
373      -d 
'{"selector":{"country":{"$eq": "US"}},"limit":5}'
 \
      
"
$SERVICE_URL
/cities/_find"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.FindResult;
import
 com.ibm.cloud.cloudant.v1.model.PostFindOptions;
import
 java.util.Collections;
import
 java.util.Map;
Cloudant
 
service
 
=
 Cloudant.newInstance();
Map<String, Object> selector = Collections.singletonMap(
    
"country"
,
    Collections.singletonMap(
"$eq"
, 
"US"
));
PostFindOptions.
Builder
 
findOptions
 
=
 
new
 
PostFindOptions
.Builder()
    .db(
"cities"
)
    .selector(selector)
    .limit(
5
);
FindResult
 
response
 
=
 service.postFind(findOptions.build()).execute().getResult();
while
 (response.getDocs().size() > 
0
) {
    System.out.println(response.getDocs());
    
// The bookmark of the next request becomes the bookmark of this response
    findOptions.bookmark(response.getBookmark());
    response = service.postFind(findOptions.build()).execute().getResult();
}
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
async
 
function
 
paginate
(
pageSize
) {
  
let
 requestParams = {
      
db
: 
'cities'
,
      
selector
: {
country
: {
'$eq'
: 
'US'
}},
      
limit
: pageSize,
  }
  
let
 findResult = (
await
 service.
postFind
(requestParams)).
result
;
  
while
 (findResult.
docs
.
length
 > 
0
) {
    
let
 documents = findResult.
docs
;
    
console
.
log
(documents);
    
// The bookmark of the next request becomes the bookmark of this response
    requestParams.
bookmark
 = findResult.
bookmark
;
    findResult = (
await
 service.
postFind
(requestParams)).
result
;
  }
}
paginate
(
5
)
Python
request_params = 
dict
(
    db=
'cities'
,
    selector={
'country'
: {
'$eq'
: 
'US'
}},
    limit=
5
,
)
response = service.post_find(**request_params).get_result()
while
 
len
(response[
'docs'
]) > 
0
:
    documents = response[
'docs'
]
    
print
(json.dumps(documents, indent=
2
))
    
# The bookmark of the next request becomes the bookmark of this response
    request_params[
'bookmark'
] = response[
'bookmark'
]
Cloudant
   
374    response = service.post_find(**request_params).get_result()
Go
findOptions := service.NewPostFindOptions(
    
"cities"
,
    
map
[
string
]
interface
{}{
        
"country"
: 
map
[
string
]
bool
{
            
"$eq"
: 
"US"
,
        },
    },
)
findOptions.SetLimit(
5
)
findResult, _, err := service.PostFind(findOptions)
if
 err != 
nil
 {
    
panic
(err)
}
for
 
len
(findResult.Docs) > 
0
 {
    documents := findResult.Docs
    b, err := json.MarshalIndent(documents, 
""
, 
"  "
)
    
if
 err != 
nil
 {
        
panic
(err)
    }
    fmt.Printf(
string
(b))
    
// The bookmark of the next request becomes the bookmark of this response
    findOptions.Bookmark = findResult.Bookmark
    findResult, _, err = service.PostFind(findOptions)
    
if
 err != 
nil
 {
        
panic
(err)
    }
}
The previous Go example requires the following import block:
Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
Curl
$ 
{
  
"docs"
:[
    {
"_id"
:
"10104153"
,
"_rev"
:
"1-32aab6258c65c5fc5af044a153f4b994"
,
"name"
:
"Silver Lake"
,
"latitude"
:34.08668,
"longitude"
:-
118.27023,
"country"
:
"US"
,
"population"
:32890,
"timezone"
:
"America/Los_Angeles"
},
    {
"_id"
:
"10104154"
,
"_rev"
:
"1-125f589bf4e39d8e119b4b7b5b18caf6"
,
"name"
:
"Echo Park"
,
"latitude"
:34.07808,
"longitude"
:-
118.26066,
"country"
:
"US"
,
"population"
:43832,
"timezone"
:
"America/Los_Angeles"
},
    {
"_id"
:
"4046704"
,
"_rev"
:
"1-2e4b7820872f108c077dab73614067da"
,
"name"
:
"Fort Hunt"
,
"latitude"
:38.73289,
"longitude"
:-
77.05803,
"country"
:
"US"
,
"population"
:16045,
"timezone"
:
"America/New_York"
},
    {
"_id"
:
"4048023"
,
"_rev"
:
"1-744baaba02218fd84b350e8982c0b783"
,
"name"
:
"Bessemer"
,
"latitude"
:33.40178,
"longitude"
:-
86.95444,
"country"
:
"US"
,
"population"
:27456,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4048662"
,
"_rev"
:
"1-e95c97013ece566b37583e451c1864ee"
,
"name"
:
"Paducah"
,
"latitude"
:37.08339,
"longitude"
:-
88.60005,
"country"
:
"US"
,
"population"
:25024,
"timezone"
:
"America/Chicago"
}
  ],
  
"bookmark"
: 
"g1AAAAA-eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWJiZGYGkOWDSyBJZAPCBD58"
}
The response includes an array of 
docs
, and a 
bookmark
, which you use to paginate through the results in the next request. When you need page
two of the results, you repeat the query by passing IBM Cloudant the bookmark 
from the first response.
Curl
$ 
curl -X POST \
      -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 \
Cloudant
   
375      -H 
'Content-type: application/json'
 \
      -d 
'{"selector":{"country":{"$eq": "US"}},"limit":5,"bookmark":"g1AAAAA-
eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWJiZGYGkOWDSyBJZAPCBD58"}'
 \
      
"
$SERVICE_URL
/cities/_find"
Curl
$ 
{
  
"docs"
:[
    {
"_id"
:
"4049979"
,
"_rev"
:
"1-1fa2591477c774a07c230571568aeb66"
,
"name"
:
"Birmingham"
,
"latitude"
:33.52066,
"longitude"
:-
86.80249,
"country"
:
"US"
,
"population"
:212237,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4054378"
,
"_rev"
:
"1-a750085697685e7bc0e49d103d2de59d"
,
"name"
:
"Center Point"
,
"latitude"
:33.64566,
"longitude"
:-
86.6836,
"country"
:
"US"
,
"population"
:16921,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4058219"
,
"_rev"
:
"1-9b4eb183c9cdf57c19be660ec600330c"
,
"name"
:
"Daphne"
,
"latitude"
:30.60353,
"longitude"
:-
87.9036,
"country"
:
"US"
,
"population"
:21570,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4058553"
,
"_rev"
:
"1-56100f7e7742028facfcc50ab6b07a04"
,
"name"
:
"Decatur"
,
"latitude"
:34.60593,
"longitude"
:-
86.98334,
"country"
:
"US"
,
"population"
:55683,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4059102"
,
"_rev"
:
"1-612ae37d982dc71eeecf332c1e1c16aa"
,
"name"
:
"Dothan"
,
"latitude"
:31.22323,
"longitude"
:-
85.39049,
"country"
:
"US"
,
"population"
:65496,
"timezone"
:
"America/Chicago"
}
  ],
  
"bookmark"
: 
"g1AAAAA-eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWhoaGIGkOWDSyBJZAO9qD40"
,
  
"warning"
: 
"no matching index found, create an index to optimize query time"
}
This time, you get the next five cities and a new bookmark ready for the next request.
How does IBM Cloudant Search work?
Pagination works in the same way for 
IBM Cloudant Search
 queries. Pass the 
bookmark
 parameter in the URL for GET requests or in the JSON body
for POST requests. See the 
following example:
Curl
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/cities/_search/search/_search/freetext?q=country:US&limit=5"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.PostSearchOptions;
import
 com.ibm.cloud.cloudant.v1.model.SearchResult;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostSearchOptions.
Builder
 
searchOptions
 
=
 
new
 
PostSearchOptions
.Builder()
    .db(
"cities"
)
    .ddoc(
"search"
)
    .index(
"freetext"
)
    .query(
"country:US"
);
    .limit(
5
);
SearchResult
 
response
 
=
 service.postSearch(searchOptions.build()).execute().getResult();
while
 (response.getRows().size() > 
0
) {
    System.out.println(response.getRows());
    
// The bookmark of the next request becomes the bookmark of this response
    searchOptions.bookmark(response.getBookmark());
    response = service.postSearch(searchOptions.build()).execute().getResult();
}
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
async
 
function
 
paginate
(
pageSize
) {
  
let
 requestParams = {
    
db
: 
'cities'
,
    
ddoc
: 
'search'
,
    
index
: 
'freetext'
,
    
query
: 
'country:US'
,
    
limit
: 
5
Cloudant
   
376  };
  
let
 searchResult = (
await
 service.
postSearch
(requestParams)).
result
;
  
while
 (searchResult.
rows
.
length
 > 
0
) {
    
let
 documents = searchResult.
rows
;
    
console
.
log
(documents);
    
// The bookmark of the next request becomes the bookmark of this response
    requestParams.
bookmark
 = searchResult.
bookmark
;
    searchResult = (
await
 service.
postSearch
(requestParams)).
result
;
  }
}
paginate
(
5
);
Python
selector = {
'country'
: {
'$eq'
: 
'US'
}}
request_params = 
dict
(
  db=
'cities'
,
  ddoc=
'search'
,
  index=
'freetext'
,
  query=
'country:US'
,
  limit=
5
,
)
response = service.post_search(**request_params).get_result()
while
 
len
(response[
'rows'
]) > 
0
:
  documents = response[
'rows'
]
  
print
(json.dumps(documents, indent=
2
))
  
# The bookmark of the next request becomes the bookmark of this response
  request_params[
'bookmark'
] = response[
'bookmark'
]
  response = service.post_search(**request_params).get_result()
Go
searchOptions := service.NewPostSearchOptions(
    
"cities"
,
    
"search"
,
 
"freetext"
,
 
"country:US"
)
searchOptions.SetLimit(
5
)
searchResult, _, err := service.PostSearch(searchOptions)
if
 err != 
nil
 {
    
panic
(err)
}
for
 
len
(searchResult.Rows) > 
0
 {
    documents := searchResult.Rows
    b, err := json.MarshalIndent(documents, 
""
, 
"  "
)
    
if
 err != 
nil
 {
        
panic
(err)
    }
    fmt.Printf(
string
(b))
    
// The bookmark of the next request becomes the bookmark of this response
    searchOptions.Bookmark = searchResult.Bookmark
    searchResult, _, err = service.PostSearch(searchOptions)
    
if
 err != 
nil
 {
        
panic
(err)
    }
}
The previous Go example requires the following import block:
Go
import
 (
 
"encoding/json"
 
"fmt"
 
"github.com/IBM/cloudant-go-sdk/cloudantv1"
Cloudant
   
377)
Curl
$ 
{
  
"total_rows"
: 65,
  
"rows"
:[
    {
"_id"
:
"10104153"
,
"_rev"
:
"1-32aab6258c65c5fc5af044a153f4b994"
,
"name"
:
"Silver Lake"
,
"latitude"
:34.08668,
"longitude"
:-
118.27023,
"country"
:
"US"
,
"population"
:32890,
"timezone"
:
"America/Los_Angeles"
},
    {
"_id"
:
"10104154"
,
"_rev"
:
"1-125f589bf4e39d8e119b4b7b5b18caf6"
,
"name"
:
"Echo Park"
,
"latitude"
:34.07808,
"longitude"
:-
118.26066,
"country"
:
"US"
,
"population"
:43832,
"timezone"
:
"America/Los_Angeles"
},
    {
"_id"
:
"4046704"
,
"_rev"
:
"1-2e4b7820872f108c077dab73614067da"
,
"name"
:
"Fort Hunt"
,
"latitude"
:38.73289,
"longitude"
:-
77.05803,
"country"
:
"US"
,
"population"
:16045,
"timezone"
:
"America/New_York"
},
    {
"_id"
:
"4048023"
,
"_rev"
:
"1-744baaba02218fd84b350e8982c0b783"
,
"name"
:
"Bessemer"
,
"latitude"
:33.40178,
"longitude"
:-
86.95444,
"country"
:
"US"
,
"population"
:27456,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4048662"
,
"_rev"
:
"1-e95c97013ece566b37583e451c1864ee"
,
"name"
:
"Paducah"
,
"latitude"
:37.08339,
"longitude"
:-
88.60005,
"country"
:
"US"
,
"population"
:25024,
"timezone"
:
"America/Chicago"
}
  ],
  
"bookmark"
: 
"g1AAAAA-eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWJiZGYGkOWDSyBJZAPCBD58"
}
You get the first five cities and a bookmark ready for the next request with the 
bookmark
 request parameter.
Curl
$ 
curl -H 
"Authorization: Bearer 
$API_BEARER_TOKEN
"
 
"
$SERVICE_URL
/cities/_search/search/_search/freetext?
q=country:US&limit=5&bookmark=g1AAAAA-eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWJiZGYGkOWDSyBJZAPCBD58"
Curl
$ 
{
  
"total_rows"
: 65,
  
"rows"
:[
    {
"_id"
:
"4049979"
,
"_rev"
:
"1-1fa2591477c774a07c230571568aeb66"
,
"name"
:
"Birmingham"
,
"latitude"
:33.52066,
"longitude"
:-
86.80249,
"country"
:
"US"
,
"population"
:212237,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4054378"
,
"_rev"
:
"1-a750085697685e7bc0e49d103d2de59d"
,
"name"
:
"Center Point"
,
"latitude"
:33.64566,
"longitude"
:-
86.6836,
"country"
:
"US"
,
"population"
:16921,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4058219"
,
"_rev"
:
"1-9b4eb183c9cdf57c19be660ec600330c"
,
"name"
:
"Daphne"
,
"latitude"
:30.60353,
"longitude"
:-
87.9036,
"country"
:
"US"
,
"population"
:21570,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4058553"
,
"_rev"
:
"1-56100f7e7742028facfcc50ab6b07a04"
,
"name"
:
"Decatur"
,
"latitude"
:34.60593,
"longitude"
:-
86.98334,
"country"
:
"US"
,
"population"
:55683,
"timezone"
:
"America/Chicago"
},
    {
"_id"
:
"4059102"
,
"_rev"
:
"1-612ae37d982dc71eeecf332c1e1c16aa"
,
"name"
:
"Dothan"
,
"latitude"
:31.22323,
"longitude"
:-
85.39049,
"country"
:
"US"
,
"population"
:65496,
"timezone"
:
"America/Chicago"
}
  ],
  
"bookmark"
: 
"g1AAAAA-eJzLYWBgYMpgSmHgKy5JLCrJTq2MT8lPzkzJBYqzmxiYWhoaGIGkOWDSyBJZAO9qD40"
,
}
See the documentation about 
query parameters
 for further details.
Do MapReduce views accept bookmarks?
No. MapReduce views don't accept a 
bookmark
. Instead, use one of the following tricks to page through results:
The \u0000 trick
.
Fetch one document too many
.
Skip and limit
.
Can I jump straight to page X of the results?
No. Bookmarks make sense only to IBM Cloudant if they come from the previous page of results. If you need page 3 of the results, you must fetch
pages 1 and 2 first.
What happens if I supply an incorrect bookmark?
IBM Cloudant responds with an 
HTTP 400 Bad Request { error: 'invalid_bookmark'}
 response if you supply an invalid bookmark. Remember,
you don't need a bookmark for the first search in a sequence.
Cloudant
   
378What happens if I change the query?
You must keep the same query (the same selector in IBM Cloudant Query or the same "q" in IBM Cloudant Search) to get the next page of results. If
you change the query, you might get an empty result set in reply.
IBM Cloudant Geospatial notice
What is IBM Cloudant Geospatial?
Data is stored as GeoJSON in the IBM Cloudant database to describe point, line, polygon, multi-point, multi-line, and multi-polygon objects. Each
object, as well as the geographic information, can have optional properties: Metadata about the 
object, which is returned in the search results.
Again, an index is defined as a JavaScript function, and then, queries can be used to ask questions of your collection of geographic features. For
example, find me the nearest object to this point; find objects within this polygon; find objects 
along this path; or find objects that intersect with this
object.
To summarize, IBM Cloudant Geo is something unique to the IBM Cloudant service and is used to perform advanced geospatial queries against your
databases of GeoJSON objects. It cannot be combined with other index types. It is only of use to Geographic 
Information Systems or use-cases that
have a purely geographic purpose.
What is changing?
As of 1 February 2023, the following conditions apply:
Users cannot query 
/$DATABASE/_design/$DDOCS/_geo
 endpoints. Requests to those endpoints return a 
404 Not Found
 response.
Users can define indexes by using the 
st_indexes
 keyword in design documents, but those indexes are ignored by the service. This ensures
that existing design documents can be updated, and replications that contain geospatial indexes 
do not fail. Existing Geo indexes will be
deleted, and customers will no longer be billed for the space they consume.
IBM Cloud® support will no longer answer questions or assist with issues that are related to the Geospatial feature of the IBM Cloudant service.
Alternatives to geospatial
Many simple geospatial queries can be done without using the Geospatial capability that was removed from the IBM Cloudant service. These
alternatives are described in this 
IBM Cloudant blog post
.
 Deprecated: 
Support for the IBM® Cloudant® for IBM Cloud® Geospatial capability ends on 31 January 2023. In many cases, existing
applications will fail if changes are not made to address the removal of this functionality before the end of support.
Cloudant
   
379Replicating databases
What is replication?
Data can be copied from one database to another in the same IBM® Cloudant® for IBM Cloud® account, across accounts and across data centers.
Data can even be replicated to and from an IBM Cloudant account and a mobile device by using 
IBM Cloudant Sync
 or 
PouchDB
. Replication can run
in one direction or in both directions, as a "single shot" or continuous operation, and can be finely tuned by using parameters.
IBM Cloudant’s replication protocol is compatible with a range of other databases and libraries, making it a great fit for Internet of Things (IoT) and
mobile applications.
IBM Cloudant is a distributed JSON data store with an HTTP API. IBM Cloudant can be run as a service on multiple clouds, or in your server rack.
Documents are stored in databases and can grow to any size as IBM Cloudant shards its data across 
many nodes. Replication is the copying of data
from a source database to a target database. The source and target databases do not need to be on the same IBM Cloudant account, or even in the
same data center.
Figure 1. Replication in pictures
Cloudant
   
380Replication is complete when the most recent version of each document in the source transfers to the destination database. Transfers include new
documents, updates to existing documents, and deletions. Only the most recent version of a document 
remains after replication; older versions are
omitted.
The source database remains unaltered by replication, apart from checkpoint data that is written to it to allow partial replications to resume from the
last known position. Any pre-existing data in the destination database remains.
How to start replicating with the dashboard
The IBM Cloudant Dashboard provides a convenient user interface to trigger replication. Click 
Replication
 on the IBM Cloudant Dashboard, and
click 
Start Replication
. Complete the following Replication form:
Figure 2. Replication form
Using the form, define the source and target databases, then click 
Start Replication
.
The status of each replication task can be seen by clicking 
Replication
. Each job changes state from 
Running
 to 
Completed
 as it progresses.
The following screen capture shows the 
Completed
 
state.
Figure 3. Completed state
How to replicate across different IBM Cloudant accounts
The source and target of a replication are URLs of IBM Cloudant databases, as shown in the following example.
See the following example that defines source and target URLs for replication:
 Important: 
For security purposes, the IBM Cloudant team recommends that you use IAM API keys or IBM Cloudant legacy authentication
API keys
 rather than account-level credentials 
for replication jobs. For more information, see 
Managing access
 or legacy 
authentication
 
and
authorization
 documentation.
Cloudant
   
381{
    
"source"
:
 
"https://myfirstaccount.cloudant.com/a"
,
    
"target"
:
 
"https://mysecondaccount.cloudant.com/b"
}
The source and target do not need to be on the same account. The source and target database names do not need to match. You must be authorized
to access both the source and target, and you must be authorized to write to the target.
Is replication run on the source or the destination?
Replication can be started at either the source or the destination end. This choice means that you can decide whether account A is pushing data to
account B, or account B is pulling data from account A. In some cases, it might not be possible 
to run replication in either configuration, for example
when one account is behind a firewall. Replication happens over HTTPS and so no non-standard ports need be opened. The decision as to which
device starts replication is yours.
How does replication affect the list of changes?
You can get a list of changes made to a document by using the 
_changes
 endpoint
. However, the distributed nature of IBM Cloudant databases
means that the response 
that is provided by the 
_changes
 feed cannot be a simple list of changes that occurred after a particular date and time.
The 
CAP Theorem
 discussion makes it clear that IBM Cloudant uses an "eventually consistent" model. This model means you might get different
results when you ask two 
different replicas of a database for a document at the same time. This can happen when one of the database copies is still
waiting to finish replication.
Eventually, the database copies complete their replication so that all the changes to a document are present in each copy.
This "eventual consistency" model has two characteristics that affect a list of changes:
a
. 
A change that affects a document almost certainly takes place at different times in different copies of the database.
b
. 
The order in which changes affect documents might differ between different copies of the database, depending on when and from where the
replication took place.
A consequence of the first characteristic is that, when you ask for a list of changes, it is meaningless to ask for a list of changes after a specific point in
time. The reason is that the list of changes might be supplied by a different database 
copy, which resulted in document updates at different times.
However, it 
is
 meaningful to ask for a list of changes after a specific change, which is specified by using a sequence identifier.
An extra consequence of the first characteristic is that it might be necessary to "look back" at preceding changes to agree on the list of changes. In
other words, to get a list of changes, you start from the most recent change that 
the database copies agree on. The point of agreement between
database copies is identified within IBM Cloudant by using the 
checkpoint
 mechanism that enables replication between database copies to be
synchronized.
Finally, when you look at a list of changes, they might be presented in a different order in subsequent requests. The order depends on how
documents were changed between different database copies. In other words, an initial list of changes might 
report changes 
A
, 
B
, then 
C
 in that
order. But a subsequent list of changes might report changes 
C
, 
A
, then 
B
 in that order. All the changes are listed, but in a different order. This
difference is because the sequence of changes that are received during replication might vary between two different copies of the 
database.
What does "eventual consistency" mean for the list of changes?
When you request a list of changes, the response you get might vary depending on which database copy supplies the list.
The 
since
 option obtains a list of changes after a specific update sequence identifier. The list always includes changes after the update, but
changes before the update might also be included. The reason is that the database copy 
that responds to the list request must ensure that it lists the
changes, consistent with all the replicas. To achieve that consistency, the database copy might have to start the list of changes from the point when
all the copies agreed. 
This point is identified by using checkpoints.
Therefore, an application that uses the 
_changes
 feed must be 
'idempotent'
. Idempotency means that the application must be able to safely
receive the same data multiple times, and potentially in a different order for repeated requests.
Checkpoints
Internally, the replication process writes its state in "checkpoint" documents that are stored in both the source and destination databases.
Checkpoints allow a replication task to be resumed from where it stopped, without having to 
start from the beginning. Checkpoint creation can be
prevented by supplying the 
"use_checkpoints": false
 option when you request replication. It is helpful to leave the feature on if your replication is
to resume efficiently 
from its last known position.
Cloudant
   
382Permissions
Admin access is necessary to insert a document into the 
_replicator
 database. The login credentials that are supplied in the source and target
parameters do not require full admin permissions. It is sufficient if the credentials 
perform the following tasks:
Write documents at the destination end.
Write checkpoint documents at both ends.
IBM Cloudant has a special 
_replicator
 user permission. This permission allows checkpoint documents to be created, but does not allow the
creation of ordinary documents in a database. In general, 
create API keys
 that have:
_reader
 and 
_replicator
 access at the source side.
_reader
 and 
_writer
 access at the destination side.
API keys can be created and configured within the IBM Cloudant Dashboard, on a per-database basis.
Figure 4. IBM Cloudant users and API keys with permissions
They can also be created 
programmatically
 by using the IBM Cloudant API.
Two-way replication
Data can be copied in both directions in a process that is known as two-way replication or synchronization. You enable this synchronization by setting
up two separate replication processes, one taking the data from A to B, the other taking data 
from B to A. Both replication processes work
independently, with data moved seamlessly in both directions.
 Important: 
For security purposes, the IBM Cloudant team recommends that you use IAM API keys or IBM Cloudant legacy authentication
API keys
 rather than account-level credentials 
for replication jobs. For more information, see 
Managing access
 or legacy 
authentication
, 
and
authorization
 documentation.
Cloudant
   
383Figure 5. Two-way replication
Discussion about continuous replication
So far, the discussion deals only with one-shot replication, which finishes when all of the source data is written to the target database. With
continuous replication, data flows continuously. All subsequent changes to the source database are 
transmitted to the target database in real time.
Continuous replication is triggered by clicking the 
Make this replication continuous
 check box when you define a replication task in the IBM
Cloudant Dashboard, or by setting the 
continuous
 flag in the IBM Cloudant API.
Two-way replication can be made continuous in one or both of the directions, by setting the 
continuous
 flag.
See the following example that uses HTTP to start a continuous replication:
POST
 
/_replicator
 
HTTP/1.1
Content-Type
: 
application/json
Host
: 
$SERVICE_URL
Authorization
: 
...
See the following example to start a continuous replication:
Curl
Cloudant
   
384curl -X POST \
    -H 
"Content-type: application/json"
 \
    
"
$SERVICE_URL
/_replicator"
 \
    -d 
'{ "_id": "repldoc-example",
          "continuous": true,
          "create_target": true,
          "source": { "url": "'
"
$SOURCE_SERVICE_URL
/source"
'" },
          "target": { 
            "auth": { "iam": { "api_key": "'
"
$API_KEY
"
'" } },
            "url": "'
"
$TARGET_SERVICE_URL
/target"
'"
          }
        }'
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PutReplicationDocumentOptions;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabase;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabaseAuth;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabaseAuthIam;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDocument;
Cloudant
 
service
 
=
 Cloudant.newInstance();
ReplicationDatabase
 
sourceDb
 
=
 
new
 
ReplicationDatabase
.Builder()
    .url(
"<your-source-service-url>/source"
)
    .build();
ReplicationDatabaseAuthIam
 
targetAuthIam
 
=
    
new
 
ReplicationDatabaseAuthIam
.Builder()
        .apiKey(
"<your-iam-api-key>"
)
        .build();
ReplicationDatabaseAuth
 
targetAuth
 
=
 
new
 
ReplicationDatabaseAuth
.Builder()
    .iam(targetAuthIam)
    .build();
ReplicationDatabase
 
targetDb
 
=
 
new
 
ReplicationDatabase
.Builder()
    .auth(targetAuth)
    .url(
"<your-target-service-url>/target"
)
    .build();
ReplicationDocument
 
replDocument
 
=
 
new
 
ReplicationDocument
();
replDocument.setSource(sourceDb);
replDocument.setTarget(targetDb);
replDocument.setContinuous(
true
);
PutReplicationDocumentOptions
 
replicationDocumentOptions
 
=
    
new
 
PutReplicationDocumentOptions
.Builder()
        .docId(
"repldoc-example"
)
        .replicationDocument(replDocument)
        .build();
DocumentResult
 
response
 
=
    service.putReplicationDocument(replicationDocumentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
sourceDb
: 
Cloudant
V1.
ReplicationDatabase
 = {
  
url
: 
'<your-source-service-url>/source'
};
Cloudant
   
385const
 
targetDb
: 
Cloudant
V1.
ReplicationDatabase
 = {
  
auth
: {
    
iam
: {
      
'api_key'
: 
'<your-iam-api-key>'
    }
  },
  
url
: 
'<your-target-service-url>/target'
};
const
 
replDocument
: 
Cloudant
V1.
ReplicationDocument
 = {
  
id
: 
'repldoc-example'
,
  
continuous
: 
true
,
  
create_target
: 
true
,
  
source
: sourceDb,
  
target
: targetDb
}
service.
putReplicationDocument
({
  
docId
: 
'repldoc-example'
,
  
replicationDocument
: replDocument
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, ReplicationDocument, ReplicationDatabase, ReplicationDatabaseAuthIam,
 
ReplicationDatabaseAuth
service = CloudantV1.new_instance()
source_db = ReplicationDatabase(
  url=
'<your-source-service-url>/source'
)
target_auth_iam = ReplicationDatabaseAuthIam(
  api_key=
'<your-iam-api-key>'
)
target_auth = ReplicationDatabaseAuth(
  iam=target_auth_iam
)
target_db = ReplicationDatabase(
  auth=target_auth,
  url=
'<your-target-service-url>/target'
)
replication_document = ReplicationDocument(
  
id
=
'repldoc-example'
,
  continuous=
True
,
  create_target=
True
,
  source=source_db,
  target=target_db
)
response = service.put_replication_document(
  doc_id=
'repldoc-example'
,
  replication_document=replication_document
).get_result()
print
(response)
Go
source, err := service.NewReplicationDatabase(
  
"<your-source-service-url>/source"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
Cloudant
   
386target, err := service.NewReplicationDatabase(
  
"<your-target-service-url>/target"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
auth, err := service.NewReplicationDatabaseAuthIam(
  
"<your-iam-api-key>"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
target.Auth = &cloudantv1.ReplicationDatabaseAuth{Iam: auth}
replicationDoc, err := service.NewReplicationDocument(
  source,
  target,
)
if
 err != 
nil
 {
  
panic
(err)
}
replicationDoc.Continuous = core.BoolPtr(
true
)
replicationDoc.CreateTarget = core.BoolPtr(
true
)
putReplicationDocumentOptions := service.NewPutReplicationDocumentOptions(
  
"repldoc-example"
,
  replicationDoc,
)
documentResult, response, err := service.PutReplicationDocument(putReplicationDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the following example of a JSON document that defines a continuous replication:
{
    
"_id"
:
 
"weekly_continuous_backup"
,
    
"source"
:
 
"https://$USERNAME:$PASSWORD@$SOURCE_SERVICE_DOMAIN/source"
,
    
"target"
:
 
"https://$USERNAME:$PASSWORD@$TARGET_SERVICE_DOMAIN/target"
,
    
"continuous"
:
 
true
}
Other replication use cases
IBM Cloudant’s replication protocol is compatible with other databases and libraries for various real-world applications.
Apache CouchDB
Cloudant
   
387Apache CouchDB
 is an open source database that can communicate with IBM Cloudant, and that requires minimal setup. The following applications
are included:
Backup - Replicate your data from IBM Cloudant to your own CouchDB databases and take nightly snapshots of your data for archiving
purposes. Send the data to a backup service such as 
Amazon Glacier
 for safe keeping.
Local-first data collection - Write your data to local Apache CouchDB first, then replicate it to IBM Cloudant for long-term storage, aggregation,
and analysis.
PouchDB
PouchDB
 is an open source, in-browser database that allows data to be replicated in both directions between the browser and IBM Cloudant. Storing
the data in a web browser 
on the client side allows web applications to function even without an internet connection. PouchDB can synchronize any
changed data to and from IBM Cloudant when an internet connection is present. Setting up replication from the client 
side requires a few lines of
JavaScript.
See the following example JavaScript that uses PouchDB to enable replication:
var
 db = 
new
 
Pouch
DB(
"myfirstdatabase"
);
var
 
URL
 = 
"https://$USERNAME:$PASSWORD@$SERVICE_DOMAIN/my_database"
);
db.
sync
(
URL
, { 
live
: 
true
 });
Filtered replications
It is useful to be able to remove some data during the replication process, when you replicate one database to another, as you can see in the
following examples:
Removing all traces of deleted documents, making the target database smaller than the source.
Separating data into smaller chunks, such as storing UK data in one database and US data in another.
Replication filter functions
IBM Cloudant’s filtered replication allows the definition of a JavaScript function that uses the return value to determine whether each document in a
database is to be filtered or not. 
Filter functions
 are stored in 
design documents
.
See the following example filter function for replicating non-deleted documents:
function
(
doc, req
) {
    
if
 (doc.
_deleted
) {
        
return
 
false
;
    }
    
return
 
true
;
}
When a replication job starts, a filter function’s name is specified as a combination of the design document where it is stored, and the filter function’s
name. You can also specify a 
query_params
 value. This value is an object 
that contains properties that are passed to the filter function in the
query
 field of its second (
req
) argument.
See the following example that uses HTTP to start a filtered replication:
POST
 
/_replicator
 
HTTP/1.1
Content-Type
: 
application/json
Host
: 
$SERVICE_URL
Authorization
: 
...
See the following example that uses the command line to start a filtered replication:
Curl
curl -X POST \
    -H 
"Content-type: application/json"
 \
    
"
$SERVICE_URL
/_replicator"
 \
    -d @filtered-replication.json
Java
Cloudant
   
388import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DocumentResult;
import
 com.ibm.cloud.cloudant.v1.model.PutReplicationDocumentOptions;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabase;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabaseAuth;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDatabaseAuthIam;
import
 com.ibm.cloud.cloudant.v1.model.ReplicationDocument;
Cloudant
 
service
 
=
 Cloudant.newInstance();
ReplicationDatabase
 
sourceDb
 
=
 
new
 
ReplicationDatabase
.Builder()
    .url(
"<your-source-service-url>/source"
)
    .build();
ReplicationDatabaseAuthIam
 
targetAuthIam
 
=
    
new
 
ReplicationDatabaseAuthIam
.Builder()
        .apiKey(
"<your-iam-api-key>"
)
        .build();
ReplicationDatabaseAuth
 
targetAuth
 
=
 
new
 
ReplicationDatabaseAuth
.Builder()
    .iam(targetAuthIam)
    .build();
ReplicationDatabase
 
targetDb
 
=
 
new
 
ReplicationDatabase
.Builder()
    .auth(targetAuth)
    .url(
"<your-target-service-url>/target"
))
    .build();
ReplicationDocument
 
replDocument
 
=
 
new
 
ReplicationDocument
();
replDocument.setSource(sourceDb);
replDocument.setTarget(targetDb);
replDocument.setFilter(
"mydesigndoc/myfilter"
);
Map
 
queryParams
 
=
 
new
 
HashMap
<>();
queryParams.put(
"foo"
, 
"bar"
);
queryParams.put(
"baz"
, 
5
);
replDocument.setQueryParams(queryParams);
PutReplicationDocumentOptions
 
replicationDocumentOptions
 
=
    
new
 
PutReplicationDocumentOptions
.Builder()
        .docId(
"repldoc-example"
)
        .replicationDocument(replDocument)
        .build();
DocumentResult
 
response
 
=
    service.putReplicationDocument(replicationDocumentOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
const
 
sourceDb
: 
Cloudant
V1.
ReplicationDatabase
 = {
  
url
: 
'<your-source-service-url>/source'
};
const
 
targetDb
: 
Cloudant
V1.
ReplicationDatabase
 = {
  
auth
: {
    
iam
: {
      
'api_key'
: 
'<your-iam-api-key>'
    }
  },
  
url
: 
'<your-target-service-url>/target'
};
const
 
replDocument
: 
Cloudant
V1.
ReplicationDocument
 = {
Cloudant
   
389  
id
: 
'repldoc-example'
,
  
filter
: 
'mydesigndoc/myfilter'
,
  
query_params
: {
'foo'
: 
'bar'
, 
'baz'
: 
5
},
  
source
: sourceDb,
  
target
: targetDb
}
service.
putReplicationDocument
({
  
docId
: 
'repldoc-example'
,
  
replicationDocument
: replDocument
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1, ReplicationDocument, ReplicationDatabase, ReplicationDatabaseAuthIam,
 
ReplicationDatabaseAuth
service = CloudantV1.new_instance()
source_db = ReplicationDatabase(
  url=
'<your-source-service-url>/source'
)
target_auth_iam = ReplicationDatabaseAuthIam(
  api_key=
'<your-iam-api-key>'
)
target_auth = ReplicationDatabaseAuth(
  iam=target_auth_iam
)
target_db = ReplicationDatabase(
  auth=target_auth,
  url=
'<your-target-service-url>/target'
)
replication_document = ReplicationDocument(
  
id
=
'repldoc-example'
,
  
filter
=
'mydesigndoc/myfilter'
,
  query_params={
'foo'
: 
'bar'
, 
'baz'
: 
5
},
  source=source_db,
  target=target_db
)
response = service.put_replication_document(
  doc_id=
'repldoc-example'
,
  replication_document=replication_document
).get_result()
print
(response)
Go
source, err := service.NewReplicationDatabase(
  
"<your-source-service-url>/source"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
target, err := service.NewReplicationDatabase(
  
"<your-target-service-url>/target"
,
)
if
 err != 
nil
 {
  
panic
(err)
}
auth, err := service.NewReplicationDatabaseAuthIam(
  
"<your-iam-api-key>"
,
)
Cloudant
   
390if
 err != 
nil
 {
  
panic
(err)
}
target.Auth = &cloudantv1.ReplicationDatabaseAuth{Iam: auth}
replicationDoc, err := service.NewReplicationDocument(
  source,
  target,
)
if
 err != 
nil
 {
  
panic
(err)
}
replicationDoc.Filter := 
"mydesigndoc/myfilter"
replicationDoc.QueryParams := 
map
[
string
]
interface
{}{
"foo"
: 
"bar"
, 
"baz"
: 
5
}
putReplicationDocumentOptions := service.NewPutReplicationDocumentOptions(
  
"repldoc-example"
,
  replicationDoc,
)
documentResult, response, err := service.PutReplicationDocument(putReplicationDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(documentResult, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/core"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
See the following example of a JSON document that defines a filtered replication:
{
    
"_id"
:
 
"weekly_backup"
,
    
"source"
:
 
"https://$USERNAME:$PASSWORD@$SOURCE_SERVICE_DOMAIN/source"
,
    
"target"
:
 
"https://$USERNAME:$PASSWORD@$TARGET_SERVICE_DOMAIN/target"
,
    
"filter"
:
 
"mydesigndoc/myfilter"
,
    
"query_params"
:
 
{
        
"foo"
:
 
"bar"
,
        
"baz"
:
 
5
    
}
}
Changes feed
IBM Cloudant publishes the adds, edits, and deletes affecting a database through a single HTTP feed from the 
_changes
 endpoint
. This feed can be
used by your application to trigger 
events. You can access the feed by using HTTP or 
curl
, as shown in the examples. Using the 
feed=continuous
option means that the stream provides you with every change that is necessary to get the most recent version 
of every document in the database.
For more information, see 
Using the IBM Cloudant changes feed FAQ
.
See the following example that uses HTTP to query the changes feed:
GET
 
/$DATABASE/_changes?feed=continuous
 
HTTP/1.1
Host
: 
$SERVICE_URL
Cloudant
   
391Authorization
: 
...
See the following example that uses the command line to query the changes feed:
curl 
"
$SERVICE_URL
/
$DATABASE
/_changes?feed=continuous"
The changes are described by using one line per change. Each change consists of:
a
. 
A string that contains a sequence number (
seq
).
b
. 
A string that contains the ID of the document that was changed.
c
. 
An array of changes.
To see the document body itself, append 
&include_docs=true
 to the curl command.
Each change is described by using the format that is shown in the following (abbreviated) example.
See the following example 
_changes
 feed:
{
    
"seq"
:
"11-g1A...c1Q"
,
    
"id"
:
"6f8ab9fa52c117eb76240daa1a55827f"
,
    
"changes"
:
[
        
{
          
"rev"
:
"1-619d7981d7027274a4b88810d318a7b1"
        
}
    
]
}
To join the changes feed from a known position, pass a 
since
 argument
 with the sequence number you want to start from.
See the following example (abbreviated) that uses HTTP to supply the 
since
 option to join a 
_changes
 feed at a known position:
GET
 
/$DATABASE/_changes?feed=continuous&include_docs=true&since=11-g1A...c1Q
 
HTTP/1.1
HOST
: 
$SERVICE_URL
Authorization
: 
...
See the following example (abbreviated) that uses the command line to supply the 
since
 option to join a 
_changes
 feed at a known position:
curl 
"
$SERVICE_URL
/
$DATABASE
/_changes?feed=continuous&include_docs=true&since=11-g1A...c1Q"
To rejoin the changes feed from the current moment in time, set 
since=now
.
See the following example that uses HTTP to supply 
since=now
 to join a 
_changes
 feed at the current moment in time:
GET
 
/$DATABASE/_changes?feed=continuous&include_docs=true&since=now
 
HTTP/1.1
Host
: 
$SERVICE_URL
Authorization
: 
...
See the following example that uses the command line to supply 
since=now
 to join a 
_changes
 feed at the current moment in time:
curl 
"
$SERVICE_URL
/
$DATABASE
/_changes?feed=continuous&include_docs=true&since=now"
Accessing the 
_changes
 data programmatically is straightforward. For example, see the SDK examples in the 
IBM Cloudant API docs
 to follow
changes with a few lines of code.
The following list includes some example use cases:
Adding items to a message queue to trigger actions within your application, such as sending a customer email.
Update an in-memory database to record live counts of activity.
Writing data to a text file to push data into an SQL database.
The changes feed can be filtered with a filter function, by using a similar technique to 
filtering during replication
.
See the following example that uses HTTP to filter the changes feed:
GET
 
/$DATABASE/_changes?feed=continuous&include_docs=true&since=now&filter=mydesigndoc/myfilter
 
HTTP/1.1
Cloudant
   
392Host
: 
$SERVICE_URL
Authorization
: 
...
See the following example that uses the command line to filter the changes feed:
curl 
"
$SERVICE_URL
/
$DATABASE
/_changes?feed=continuous&include_docs=true&since=now&filter=mydesigndoc/myfilter"
Replication pitfalls
To replicate successfully, the sum of the document size and all attachment sizes must be less than the maximum request size of the target cluster.
For example, if the maximum HTTP request size is 11 MB, then the following scenarios apply:
Table 1. Various scenarios based on maximum HTTP request size 11 MB
Document size
Attachment size
Total size
Replicates?
1 MB
Five 2-MB attachments
11 MB
Yes
1 MB
One 10-MB attachment
11 MB
Yes
1 MB
One hundred 1-MB attachments
101 MB
No
Several considerations apply when you use replication.
Incorrect user permissions
For replication to proceed optimally when you replicate from database "a" to database "b", the credentials that are supplied must have:
_reader
 and 
_replicator
 permissions on database "a".
_writer
 permissions on database "b".
API keys are generated in the IBM Cloudant Dashboard or through the 
API
. Each key can be given individual permissions that relate to a specific IBM
Cloudant database. IBM Cloudant 
must be able to write its checkpoint documents at the "read" end of replication, otherwise no state is saved and
replication cannot resume from where it stopped. If the state is not saved, it can lead to performance problems when 
replication of large data sets
resumes. The reason is that without checkpoints, the replication process restarts from the beginning each time that it is resumed.
Replication document is conflicted
Another consequence of setting user permissions incorrectly is that the 
_replicator
 document becomes conflicted. The 
_replicator
 document
records the current state of the replication process. In an extreme case, the 
document can become huge because it contains many unresolved
conflicts. Such a large document uses much of the available space and causes extra server load.
You can check the size of your 
_replicator
 database by sending a 
GET
 request to the 
/_replicator
 endpoint:
Curl
curl 
"
$SERVICE_URL
/_replicator"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DatabaseInformation;
import
 com.ibm.cloud.cloudant.v1.model.GetDatabaseInformationOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetDatabaseInformationOptions
 
databaseInfoOptions
 
=
    
new
 
GetDatabaseInformationOptions
.Builder()
        .db(
"_replicator"
)
        .build();
 Tip: 
The ordering of documents within the 
_changes
 feed is not always the same. In other words, changes might not appear in strict time
order. The reason is that data is returned from multiple IBM Cloudant nodes, and eventual consistency 
rules apply.
Cloudant
   
393DatabaseInformation
 
response
 
=
    service.getDatabaseInformation(databaseInfoOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getDatabaseInformation
({
db
: 
'_replicator'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_database_information(db=
'_replicator'
).get_result()
print
(response)
Go
getDatabaseInformationOptions := service.NewGetDatabaseInformationOptions(
  
"_replicator"
,
)
databaseInformation, response, err := service.GetDatabaseInformation(getDatabaseInformationOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(databaseInformation, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Get conflicts from replication document
In the returned JSON, look for the 
disk_size
 value. If the value indicates a size of over 1 GB, go to the 
IBM Cloud Support portal
 for further advice.
You can check an individual 
_replicator
 document for conflicts, as shown in the following example:
Curl
curl 
"
$SERVICE_URL
/_replicator/
$DOCID
?conflicts=true"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.GetReplicationDocumentOptions;
Cloudant
   
394import
 com.ibm.cloud.cloudant.v1.model.ReplicationDocument;
Cloudant
 
service
 
=
 Cloudant.newInstance();
GetReplicationDocumentOptions
 
replicationDocOptions
 
=
    
new
 
GetReplicationDocumentOptions
.Builder()
        .conflicts(
true
)
        .docId(
"$DOCID"
)
        .build();
ReplicationDocument
 
response
 
=
    service.getReplicationDocument(replicationDocOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getReplicationDocument
({
  
conflicts
: 
true
,
  
docId
: 
'$DOCID'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_replication_document(
  conflicts=
True
,
  doc_id=
'$DOCID'
).get_result()
print
(response)
Go
getReplicationDocumentOptions := service.NewGetReplicationDocumentOptions(
  
"$DOCID"
,
)
replicationDocument, response, err := service.GetReplicationDocument(getReplicationDocumentOptions)
if
 err != 
nil
 {
  
panic
(err)
}
replicationDocument.Conflicts = core.BoolPtr(
true
)
b, _ := json.MarshalIndent(replicationDocument, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
   
"github.com/IBM/go-sdk-core/core"
)
Cloudant
   
395All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Cancel all replications
If you want to cancel all replications and start with a new, clean 
_replicator
 database, delete then re-create the 
replicator
 database.
See the following HTTP to remove and re-create the 
_replicator
 database:
DELETE
 
/_replicator
 
HTTP/1.1
HOST
: 
$SERVICE_URL
Authorization
: 
...
PUT
 
/_replicator
 
HTTP/1.1
HOST
: 
$SERVICE_URL
Authorization
: 
...
Delete the replicator database
See the following example to remove the 
_replicator
 database:
Curl
curl -X DELETE 
"
$SERVICE_URL
/_replicator"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.DeleteDatabaseOptions;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
Cloudant
 
service
 
=
 Cloudant.newInstance();
DeleteDatabaseOptions
 
deleteDatabaseOptions
 
=
 
new
 
DeleteDatabaseOptions
.Builder()
        .db(
"_replicator"
)
        .build();
Ok
 
response
 
=
 service.deleteDatabase(deleteDatabaseOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
deleteDatabase
({
db
: 
'_replicator'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.delete_database(db=
'_replicator'
).get_result()
print
(response)
Go
deleteDatabaseOptions := service.NewDeleteDatabaseOptions(
  
"_replicator"
,
)
Cloudant
   
396ok, response, err := service.DeleteDatabase(deleteDatabaseOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Re-create the replicator database
See the following example to re-create the 
_replicator
 database:
Curl
curl -X PUT 
"
$SERVICE_URL
/_replicator"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PutDatabaseOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PutDatabaseOptions
 
databaseOptions
 
=
 
new
 
PutDatabaseOptions
.Builder()
    .db(
"_replicator"
)
    .build();
Ok
 
response
 
=
    service.putDatabase(databaseOptions).execute()
        .getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
putDatabase
({
  
db
: 
'_replicator'
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.put_database(db=
'_replicator'
).get_result()
Cloudant
   
397print
(response)
Go
putDatabaseOptions := service.NewPutDatabaseOptions(
  
"_replicator"
,
)
ok, response, err := service.PutDatabase(putDatabaseOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(ok, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 for
examples.
Many simultaneous replications
It is easy to forget that you previously set up replication between two databases, and so create extra replication processes in error. Each replication
job is independent of the other, so IBM Cloudant does not prevent you from doing creating 
extra replication processes. However, each replication
task uses up system resources.
You can check your "active replications" in the IBM Cloudant Dashboard to ensure that no unwanted replication tasks are in progress. Delete any
_replicator
 documents that are no longer needed.
Tuning replication speed
By default, IBM Cloudant replication runs at an appropriate rate to get the data from the source to the target without adversely affecting
performance. Choosing between replication rate and cluster performance for other tasks is a tradeoff. 
Your use case might require faster replication
at the expense of other IBM Cloudant services. Alternatively, you might require cluster performance to take priority, with replication treated as a
background process.
Advanced replication API options
 are available. These options enable an increase or decrease in the amount of computing power that is used during
replication, 
as shown in the following examples:
If your documents contain attachments, you might want to consider reducing the batch_size and increasing the worker_processes, to
accommodate larger documents in smaller batches.
If you have many tiny documents, then you might consider increasing the 
worker_process
 and 
http_connections
 
values.
If you want to run replication with minimal impact, setting 
worker_processes
 and 
http_connections
 to 1 might be appropriate.
For more information, see 
Consumption of Read and Write Operations by Replication
.
For further assistance about the best configuration for your use case, go to the 
IBM Cloud Support portal
.
Replication performance can be improved by enabling the 
"use_bulk_get": true"
 replication option. In that case, the replicator fetches
documents from the source in batches rather than individually.
{
  "_id": "rep_doc_id",
  "source": "https://account1.cloudant.com/db1",
  "target": "https://account2.cloudant.com/db2",
  "use_bulk_get": true
}
Cloudant
   
398The increased replication rate might consume the available read or write rate capacity on the source and target endpoint accounts.
Removing conflicting document revisions with replication
One way to remove conflicted document revisions via replication is by enabling the 
"winning_revs_only": true
 option. This option only replicates
the 
winning
 document revisions. That is the revision returned by 
default by a 
GET $SERVICE_URL/$DATABASE/$DOCID
 request. This option is an
advanced option, as it discards conflicted document revisions. 
Use this option with care.
IBM Cloudant Replication
IBM® Cloudant® for IBM Cloud® replication is the process that synchronizes the state of two databases.
Any change that occurred in the source database is reproduced in the target database. You can create replications between any number of
databases, either continuously or as a "one off" task.
Depending on your application requirements, you use replication to share and aggregate state and content.
Replication takes place in one direction only. To keep two databases synchronized with each other, you must replicate in both directions. Complete
this process by replicating from 
database1
 to 
database2
, and separately 
from 
database2
 to 
database1
.
First, when replication finishes, all active documents in the source database also exist in the destination or "target" database. Second, documents
that are deleted from the source database are also removed from the destination database 
(if they exist there).
Replication operation
Replication has two forms: push or pull replication:
Push replication
 - where the source is a local database, and the destination is a remote database.
Pull replication
 - where the source is a remote database instance, and the destination is the local database.
Pull replication is helpful if your source database has a permanent IP address, and your destination database is local and has a dynamically assigned
IP address, for example, obtained through DHCP. Pull replication is appropriate if you are 
replicating to a mobile or other device from a central
server.
In all cases, the requested databases in the source and target specification must exist. If they do not, an error is returned within the JSON object.
See the following example request to replicate between a database on the source server 
example.com
, and a target database on IBM Cloudant.
POST /_replicate
Content-Type
: 
application/json
Accept
: 
application/json
{
  "source" : "https://$USERNAME1:$PASSWORD1@example.com/db",
  "target" : "https://$USERNAME2:$PASSWORD2@$ACCOUNT2.cloudant.com/db",
}
See the following example error response if one of the requested databases for a replication does not exist.
{
  
"error"
 
:
 
"db_not_found"
,
  
"reason"
 
:
 
"could not open https://example.com/db/"
}
Continuous replication
By default, the synchronization of a database during replication happens one time when the replicate request is made. To ensure that replication
from the source database to the target database takes place continually, set the 
continuous
 
field of the JSON object within the request to 
true
.
With continuous replication, changes in the source database are replicated to the target database forever until you specifically cancel the replication.
Changes are replicated between the two databases while a network connection is available between the two instances.
When in operation, the replication process does not stop when it finishes processing all current updates. Instead, the replication process continues
to wait for further updates to the source database, and applies them to the target.
Cloudant
   
399The 
_replicator
 database
The 
_replicator
 database is a special database within your account, where you can 
PUT
 or 
POST
 replication documents to specify the
replications you want.
Before you start a replication, you must create the 
_replicator
 database. To create a database, send a 
PUT
 request to:
$ 
https://$ACCOUNT.cloudant.com/_replicator
For more information, see 
Databases
.
To cancel a replication, you 
DELETE
 the replication document. The fields that are supplied in the replication document are described in the 
Create
or modify a replication operation
 
description under Request information.
Important notes
A new and more powerful 
replication scheduler
 changes the previous behavior of the IBM Cloudant replication mechanisms. Ensure that your
applications 
are updated.
Replications can severely impact the performance of an IBM Cloudant instance. Performance testing helps you understand the impact on your
environment under an increasing number of concurrent replications.
Continuous replication
 can result in many internal calls. Requiring many calls might affect the costs for multi-tenant users of IBM Cloudant
systems. By default, continuous replication is not enabled.
The target database must exist. It is not automatically created if it does not exist. Add 
"create_target":true
 to the JSON document that
describes the replication if the target database does not exist before replication. 
For more information, see 
Creating a target database during
replication
.
Replicator databases must be maintained and looked after, just like any other valuable data store. For more information, see 
replication
database maintenance
.
Advanced replication
You can learn about advanced replication concepts and tasks, such as the ones in the following list and more:
Maintaining your replication database
Scheduling and monitoring replications
Authenticating during replication
You might also find it helpful to review details of the underlying 
replication protocol
, and review the 
API reference
 documentation.
Replication database maintenance
A replication database must be monitored like any other database. Without regular database maintenance, you might accumulate invalid documents
that were caused by interruptions to the replication process. Having many invalid documents can result 
in an excess load on your cluster when the
replicator process is restarted by IBM® Cloudant® for IBM Cloud® operations.
To maintain a replication database, remove old documents. You can remove old documents by determining their age and 
deleting them
 if they're no
longer needed.
The replication scheduler
 Note: 
Continuous replication forces checks to be made continuously on the source database. These checks result in an increasing number of
database accesses, even if the source database content did not change. Database accesses are counted as part 
of the work that is done
within a multi-tenant database configuration.
 Note: 
All design documents and 
_local
 documents that are added to the 
/_replicator
 database are ignored.
 Important: 
For security purposes, the IBM Cloudant team recommends that you use IAM API keys or IBM Cloudant legacy authentication
API keys
 rather than account-level credentials 
for replication jobs. For more information, see the 
IAM guide
 or the legacy 
Authentication API
document
 
and the legacy 
Authorization API document
.
Cloudant
   
400The new IBM Cloudant Replication Scheduler provides a number of improvements and enhancements when compared with the previous IBM
Cloudant replication mechanism.
In particular, network usage during replication is more efficient. The scheduler accounts for the current load for individual database nodes within a
cluster when it determines the allocation of replication tasks.
Finally, the state of a replication is now more detailed, and consists of seven distinct states:
a
. 
initializing
 - The replication was added to the scheduler, but isn't yet initialized or scheduled to run. The status occurs when a new or
updated replication document is stored within the 
_replicator
 database
.
b
. 
error
 - The replication can't be turned into a job. This error might be caused in several different ways. For example, the replication must be
filtered
, 
but it wasn't possible to fetch the filter code from the source database.
c
. 
pending
 - The replication job is scheduled to run, but isn't yet running.
d
. 
running
 - The replication job is running.
e
. 
crashing
 - A temporary error occurred that affects the replication job. The job is automatically retried later.
f
. 
completed
 - The replication job completed. This state doesn't apply to 
continuous replications
.
g
. 
failed
- The replication job failed. The failure is permanent. This state means that no further attempt is made to replicate by using this
replication task. The failure might be caused in several different ways, for example, if 
the source or target URLs aren't valid.
The transition between these states is illustrated in the following diagram:
Figure 1. Replication Scheduler states
The scheduler introduces two new endpoints:
/_scheduler/docs
/_scheduler/jobs
You can manage and determine replication status more quickly and easily by using these endpoints.
See the typical process for using the replication scheduler to manage and monitor replications:
a
. 
Create a 
replication document
 that describes the needed replication, and store the document in the 
replicator database
.
b
. 
Monitor the status of the replication by using the 
/_scheduler/docs
 endpoint.
Cloudant
   
401Authentication during replication
In any production application, security of the source and target databases is essential. In order for replication to continue, authentication is
necessary to access the databases. Checkpoints for replication are 
enabled by default
, which means that replicating the source database requires
write access.
To enable authentication during replication, include a username and password in the database URL. The replication process uses the supplied values
for HTTP Basic Authentication.
See the following example of specifying username and password values for accessing source and target databases during replication:
{
 
"source"
:
 
"https://$USERNAME:$PASSWORD@example.com/db"
,
 
 
"target"
:
 
"https://$USERNAME:$PASSWORD@$ACCOUNT.cloudant.com/db"
}
Filtered replication
Sometimes you don't want to transfer all documents from source to target. To choose which documents to transfer, include one or more filter
functions in a design document on the source. You can then tell the replicator to use these filter functions.
A filter function takes two arguments:
The document to be replicated.
The replication request.
A filter function returns a 
true
 or 
false
 value. If the result is true, the document is replicated.
To set up filtering, use the 
selector
 field whenever possible. When you use the 
selector
 field, you can specify a filter without having to replicate
the entire database. This method makes filtering faster and causes 
less load on IBM Cloudant. For more information, see the 
selector
 field
documentation.
See the following example of a filter function:
function
(
doc, req
) {
 
return
 !!(doc.
type
 && doc.
type
 == 
"foo"
);
}
Filters are stored under the topmost 
filters
 key of the design document.
See the following example of storing a filter function in a design document:
{
 
"_id"
:
 
"_design/myddoc"
,
 
"filters"
:
 
{
  
"myfilter"
:
 
"function goes here"
 
}
}
A filtered replication is started by using a JSON statement that identifies the following items:
The source database.
The target database.
The name of the filter that is stored under the 
filters
 key of the design document.
See example JSON for starting a filtered replication:
{
 
"source"
:
 
"https://$USERNAME:$PASSWORD@example.org/example-database"
,
 
"target"
:
 
"https://$USERNAME:$PASSWORD@$ACCOUNT.cloudant.com/example-database"
,
 
"filter"
:
 
"myddoc/myfilter"
}
 Tip: 
Filtering documents during replication is similar to the process of 
filtering the 
_changes
 feed
.
Cloudant
   
402Arguments can be supplied to the filter function by including key: value pairs in the 
query_params
 field of the invocation.
See example JSON for starting a filtered replication with supplied parameters:
{
 
"source"
:
 
"https://$USERNAME:$PASSWORD@example.org/example-database"
,
 
"target"
:
 
"https://$USERNAME:$PASSWORD@$ACCOUNT.cloudant.com/example-database"
,
 
"filter"
:
 
"myddoc/myfilter"
,
 
"query_params"
:
 
{
  
"key"
:
 
"value"
 
}
}
The 
selector
 option provides performance benefits when compared with using the 
filter
 option. Use the 
selector
 option whenever
possible. For more information, see the 
selector
 documentation.
Eliminating conflicts that use replication
Use the 
winning_revs_only: true
 option to replicate 
winning
 document revisions only. These revisions are the revisions that would be returned by
the 
GET $ACCOUNT/$DATABASE/$DOCID
 API endpoint by default, 
or appear in the 
_changes
 feed with the default parameters.
{
 
"source"
:
 
"https://$USERNAME:$PASSWORD@example.org/example-database"
,
 
"target"
:
 
"https://$USERNAME:$PASSWORD@$ACCOUNT.cloudant.com/example-database"
,
 
"winning_revs_only"
:
 
true
}
Replication with this mode discards conflicting revisions, so it might be one way to remove conflicts through replication.
Replication IDs and checkpoint IDs, generated by 
winning_revs_only: true
 replications are different than those replications generated by
default, so it is possible to first replicate the winning revisions, then later, to 
backfill
 the rest of the revisions with a regular replication job.
The 
winning_revs_only: true
 option can be combined with filters or other options like 
continuous: true
 or 
create_target: true
.
Named document replication
Sometimes you don't want to replicate documents. For simple replications, you don't need to write a filter function. Instead, to replicate specific
documents, add the list of keys as an array in the 
doc_ids
 field.
See the following example replication of specific documents:
{
 
"source"
:
 
"https://$USERNAME:$PASSWORD@example.org/example-database"
,
 
"target"
:
 
"https://$USERNAME:$PASSWORD@127.0.0.1:5984/example-database"
,
 
"doc_ids"
:
 
[
"foo"
,
 
"bar"
,
 
"baz"
]
}
The 
user_ctx
 property and delegations
Replication documents can have a custom 
user_ctx
 property. This property defines the user context under which a replication runs.
An older way of triggering replications, by making a 
POST
 to the 
/_replicate/
 endpoint, didn't need the 
user_ctx
 property. The reason is that at
the moment of triggering the replication, all the necessary 
information about the authenticated user is available.
By contrast, the replicator database is a regular database. The information about the authenticated user is only present at the moment that the
replication document is written to the database. In other words, the replicator database implementation 
is similar to a 
_changes
 feed consumption
application, with 
?include_docs=true
 set.
For replication, this implementation difference means that for nonadmin users, a 
user_ctx
 property that includes the user's name and a subset of
their roles must be defined in the replication document. This requirement is addressed 
by a validation function present in the default design
document of the replicator database. The function validates each document update. This validation function also ensures that a nonadmin user can't
set a username property in the 
user_ctx
 
property that doesn't correspond to the correct username. The same principle also applies for roles.
See the following example delegated replication document:
{
Cloudant
   
403 
"_id"
:
 
"my_rep"
,
 
"source"
:
  
"https://$ACCOUNT:$PASSWORD@$SERVER.com:5984/foo"
,
 
"target"
:
  
"https://$ACCOUNT:$PASSWORD@$ACCOUNT.cloudant.com/bar"
,
 
"continuous"
:
  
true
,
 
"user_ctx"
:
 
{
  
"name"
:
 
"joe"
,
  
"roles"
:
 
[
"erlanger"
,
 
"researcher"
]
 
}
}
For admins, the 
user_ctx
 property is optional. If the property is missing, the value defaults to a user context with the name 
null
 and an empty list
of roles.
The empty list of roles means that design documents aren't written to local targets during replication. If you want to write design documents to local
targets, then a user context with the 
_admin
 role must be set explicitly.
Also, for admins, the 
user_ctx
 property can be used to trigger a replication for another user. This user context is passed to local target database
document validation functions.
In summary, for admins, the 
user_ctx
 property is optional. While for regular (nonadmin) users, it's mandatory. When the roles property of
user_ctx
 is missing, it defaults to the empty list 
[ ]
.
Performance-related options
Several performance-related options can be set for a replication, by including them in the replication document.
use_bulk_get
Set to 
true
 to improve replication job performance. A replication fetches documents in batches from the source. The increased replication
rate can consume the source and target account capacity quicker, and result in concurrent 
nonreplication requests on those accounts to
experience more 429 HTTP errors.
connection_timeout
The maximum period of inactivity for a connection in milliseconds. If a connection is idle for this period, its current request is retried. Default
value is 30000 milliseconds (30 seconds).
http_connections
The maximum number of HTTP connections per replication. For push replications, the effective number of HTTP connections that are used is
min(worker_processes + 1, http_connections)
. For pull replications, the effective number 
of connections that are used corresponds to
this parameter's value. Default value is 20.
retries_per_request
The maximum number of retries per request. Before a retry, the replicator waits for a short period before it repeats the request. This period
doubles between each consecutive retry, and never goes beyond 5 minutes. The minimum value before 
the first retry is 0.25 seconds. The
default value is 10 retries.
socket_options
A list of options to pass to the connection sockets. The available options can be found in the 
documentation for the Erlang function 
setopts
 of
the 
inet
 module
. Default value is 
[{keepalive, true},{nodelay, false}]
.
worker_batch_size
Worker processes run batches of replication tasks, where the batch size is defined by this parameter. The size corresponds to the number of
_changes
 feed rows. Larger values for the batch size might result in better performance. 
Smaller values mean that checkpointing is done
more frequently. Default value is 500.
worker_processes
The number of processes the replicator uses in each replication task to transfer documents from the source to the target database. Higher
values might produce better throughput because of greater parallelism in network and disk IO activities, 
but this improvement comes at the
cost of requiring more memory and potentially CPU time. Default value is 4.
See the following example that includes performance options in a replication document:
 Note: 
The 
user_ctx
 property applies to local endpoints only.
Cloudant
   
404{
 
"source"
:
 
"https://$ACCOUNT1:$PASSWORD1@example.com/example-database"
,
 
"target"
:
 
"https://$ACCOUNT2:$PASSWORD2@example.org/example-database"
,
 
"connection_timeout"
:
 
60000
,
 
"retries_per_request"
:
 
20
,
 
"http_connections"
:
 
30
}
The effect of large attachments
Having large numbers of attachments on documents might cause an adverse effect on replication performance.
For more information about the effect of attachments on replication performance, see 
Performance considerations
.
Avoiding the 
/_replicate
 endpoint
If a problem occurs during replication, such as a stall, timeout, or application crash, a replication that is defined within the 
_replicator
 database is
automatically restarted by the system. However, if you define a replication 
by sending a request to the 
/_replicate
 endpoint, it can't be restarted
by the system if a problem occurs because the replication request doesn't persist. Replications that are defined in the 
_replicator
 database 
are
easier to monitor.
 Important: 
Use the 
_replicator
 scheduler
 instead of the 
/_replicate
 endpoint.
Cloudant
   
405Migrating your plan
Migration overview
The 
IBM® Cloudant® for IBM Cloud®
 database-as-a-service offering is a JSON document store that runs on multi-tenant clusters. The service is
available with a choice 
of geographical locations with predictable costs, scalability, and a service-level agreement (SLA).
You can migrate to an IBM Cloudant Lite or Standard plan instance on IBM Cloud from one of the following plans:
Table 1. IBM Cloudant migration paths
Plan
Description
IBM Cloudant Enterprise
Dedicated, single-tenant clusters
Apache CouchDB
The self-hosted, open source database on which IBM Cloudant is based.
Benefits of the IBM Cloudant Lite and Standard plans
With the Standard plan, you can 
reserve throughput capacity
 for your database service, that is, to specify how much throughput your application's
database is going to need to handle demand. The Standard plan also charges for the amount 
of storage you use. Capacity is measured with the
following metrics:
Table 2. Capacity metrics
Metric
Description
Reads per
second
The rate when simple document fetches are performed, for example, retrieving a document by its 
_id
, or querying against
a partitioned database that uses a partition key.
Writes per
second
The rate when data is written to the database. API calls dealing with document creation, update, or deletion count as
"writes".
Global Queries
per second
The rate when the database is queried by global indices, typically by accessing the 
_find
 endpoint, secondary
MapReduce, or search indices.
Storage
The amount of disk space occupied by your JSON data, attachments, and secondary indices.
As an example, the Lite plan offers 20 reads per second, 10 writes per second, 5 global queries per second, and 1 GB of storage for free. This plan is
ideal when you're evaluating the product and during product development. When your application 
goes into QA or production, switch to the Standard
plan to scale the instance. The Standard plan's smallest capacity has 100 reads per second, 50 writes per second, 5 global queries per second, and
20 GB of storage for ~USD$76.65 per month. 
You can buy extra storage, which is charged by the GB.
By using the slider in the IBM Cloudant Dashboard, you can reserve a smaller or larger capacity for your IBM Cloudant service whenever you need it:
Cloudant
   
406Figure 1. Slider
You're billed on the highest capacity that is selected in any given hourly window. Your database throughput can scale up to deal with seasonal
demands and scale down again for the quiet times. Your monthly bill is always predictable; upgrades 
are automatic; and your SLA is 
99.99%
.
If you exceed your quota of reads, writes, and global queries in a given second, the IBM Cloudant API responds with a 
429: too many requests
HTTP response. Your application might retry the request later. You can use our official 
libraries to retry such requests with an exponential back off.
Migrating from a Lite plan to a Standard plan
Migrating from the free Lite plan to the Standard plan by completing the following tasks.
Step 1: Authenticate with IBM Cloud Dashboard
a
. 
Go to the 
IBM Cloud® Dashboard
.
b
. 
Authenticate with your username and password. The IBM Cloud Dashboard opens to the Resource list.
Step 2: Select your IBM Cloudant instance
a
. 
Under Services, open the IBM Cloudant instance that you want to migrate.
b
. 
Select 
Plan
.
c
. 
From the list of pricing plans, select 
Standard
.
Figure 1. Standard plan
 Tip: 
The amount that you can change the throughput capacity is limited to a maximum of 10 units per change with a maximum of one change
per hour. Notice the "change limit" point on the slider. Changes downward are unlimited in size, but 
still subject to the time limit.
Cloudant
   
407Step 3: Upgrade to the Standard plan
a
. 
Click 
Upgrade
. All your existing data is kept.
b
. 
Adjust your capacity by using the Throughput Capacity slider to increase or decrease capacity as needed.
Now, you're ready to go.
Migrating an Enterprise plan to a Lite or Standard plan
Migration from the Enterprise plans to IBM Cloudant Lite or Standard plans includes these tasks, which are described in the following steps.
Step 1: Sign up for IBM Cloud
a
. 
Go to the 
IBM Cloud Dashboard
.
b
. 
Authenticate with your username and password.
The IBM Cloud Dashboard opens to the Resource list.
Step 2: Create an IBM Cloudant instance
a
. 
Click 
Create resource
.
b
. 
Click 
Databases
 > 
Cloudant
.
Figure 1. IBM Cloudant Dashboard
For more information, see the 
Getting started
 tutorial.
Step 3: Find out whether your application is ready for IBM Cloudant
a
. 
Revisit your application’s usage of IBM Cloudant to make sure it is ready to handle the capacity limits of the Standard plan. For more
information, see 
how the IBM Cloudant API works
.
b
. 
Verify that your application can handle a 
429: too many requests
 HTTP response.
The following table provides more information about these HTTP responses:
Table 1. HTTP responses
HTTP response
Issue
429: too many
requests
Retrying requests that get a 
429
 response is acceptable for occasional traffic spikes that exceed your plan's capacity. If
your application traffic is routinely generating 
429
 responses, you probably need to upgrade 
to a larger plan.
413: request
entity too
large
The maximum individual document size is 1 MB on IBM Cloudant. You receive a 
413
 message if the limit is exceeded. For
more information, see 
request and document size limits
.
Step 4: Migrate data from the old service to the new service
a
. 
Set up continuous replications from your existing service to your IBM Cloudant account.
For more information, see the 
Replication guide
 and 
Using IBM Cloudant
 about how to set up and monitor replication 
tasks.
b
. 
Alternatively, use the 
couchreplicate
 tool to coordinate the transfer of data from one IBM Cloudant account to another.
Your browser does not support the video tag.
c
. 
Verify that all your data replicates to the new service and that indexes are built.
Step 5: Test your application
 Tip: 
The 
couchreplicate
 tool sets up multiple replication jobs between the source and target accounts, ensuring that only so many
replication jobs proceed at one time. If you need to migrate hundreds of databases, then 
couchreplicate
 
can help coordinate the
replication jobs.
Cloudant
   
408a
. 
Conduct load and functional testing on your application.
b
. 
Ensure that no issues exist before you migrate to production.
Step 6: Move to the new instance
a
. 
Update your application to use the new account URL and credentials for the IBM Cloudant instance.
b
. 
(Optional) Go to the 
Getting started tutorial
 to obtain the service credentials for your IBM Cloudant instance.
Step 7: Turn off the old service
a
. 
Verify that your application is fully migrated to the Lite or Standard instance.
b
. 
Delete the old Enterprise plan instance from your IBM Cloud console to ensure that you're no longer charged for the service.
Finding your IBM Cloudant plan
You can subscribe to different IBM Cloudant plans, including the Lite, Standard, or Enterprise plans.
Step 1: Finding your plan
The following steps show where you can see the type of plan that you selected.
a
. 
Go to the 
IBM Cloud Dashboard
.
b
. 
Authenticate with your username and password.
The IBM Cloud Dashboard opens to the Resource list.
c
. 
Click an instance to find more information.
d
. 
Click 
Plan
. A checkmark indicates the plan that you use as shown in the following screen capture. For more information, see the 
Migration
FAQ
.
Figure 1. Standard dashboard
Step 2: Finding your legacy Enterprise plan
You can find your Enterprise plan in the IBM Cloudant Dashboard by following these steps.
a
. 
Open the IBM Cloudant Dashboard. For more information, see the 
Getting started
 tutorial.
 Note: 
If the Plan tab indicates that you're on the Standard plan, you don't need to read any further. You're already on a paid SLA-
backed IBM Cloudant service. No further action is required.
Cloudant
   
409b
. 
If you're using a legacy Enterprise 
cloudant.com
 account, click 
Account
.
c
. 
Review your 
cloudant.com
 Enterprise account on a dedicated cluster. The view doesn't include a Usage tab and looks like the following
example:
Figure 2. Enterprise plan
Cloudant
   
410Recovery and backup
Disaster recovery and backup for IBM Cloudant
Your data is important and valuable. You want to protect your data to help ensure it's secure, available, and maintains integrity. IBM® Cloudant® for
IBM Cloud® provides several ways to protect your data and help keep your applications operational.
Some of these protection features are automatic. For other forms of protection, IBM Cloudant provides you with supported tools that help you to
create your own high availability and disaster recovery capabilities.
This document provides an overview of the automatic capabilities and supported tools that are offered by IBM Cloudant.
Types and levels of protection
The type of protection you might want depends on the problem you're trying to solve.
For example, you might want to have a high level of data availability so that you can still access your data, even if a limited amount of hardware within
the system failed. This requirement is necessary for "High Availability" (HA). 
It means that you provide the best possible continuous data availability
after a hardware failure. Different HA techniques tolerate different levels of failure before operations are affected.
You might want to have quick and easy ways of backing up and restoring data. For example, after a severe or extensive hardware failure, you want the
ability to make all the data available on an alternative system as quickly as possible. This 
requirement is necessary for "Disaster Recovery" (DR). A
disaster generally means that a database is no longer available in one or more locations. For example, a power outage might cause all systems in a
database cluster to fail. 
Or a large-scale network failure might mean systems in a cluster can't be contacted, even though they continue to work
correctly.
Addressing your HA or DR requirements often begins by simplifying the problem into more generic requirements. When you identify your
requirements, you can apply the tools and features that help solve the generic needs. Together, the tools and 
features can address your HA or DR
requirements.
IBM Cloudant provides a number of tools and features that address general requirements:
a
. 
Data redundancy within a single region, also known as 
In-region automatic data redundancy
.
b
. 
Cross-region data redundancy and failover, also known as 
Cross-region redundancy for disaster recovery
.
c
. 
Point-in-time backup for point-in-time restores that use "traditional" 
database backup and recovery
.
In-region automatic data redundancy
Within a single IBM Cloudant account, data is stored in triplicate by using internal and automatic processes. You don't need to do anything to enable
this internal data replication.
In-region data redundancy enables high availability protection. Specifically, in-region data redundancy provides protection for your data against
hardware failure within the region. When a hardware unit within the region fails, only the copy 
of your data that is stored on that unit is no longer
available. Your applications stay usable because IBM Cloudant automatically routes requests to the copies of your data that is still available on other
hardware units within the region. 
Meanwhile, automatic monitoring of systems detects the hardware unit failure, prompting action and subsequent
restoration of full redundancy.
IBM Cloudant accounts are located within a single region, which means the data that you store within your account is stored across separate servers,
each of which is hosted within that single region.
In-region automatic data redundancy is limited to the following functions:
a
. 
Providing protection within a single region only.
b
. 
Maintaining current data.
To provide protection across more than the single region associated with your account, use 
Cross-region redundancy for disaster recovery
. To
provide protection for the "history" 
of your data, use data snapshots that are created by 
database backup and recovery
 tools. For example, you can
 Important: 
The IBM Cloud® Service has Business Continuity plans in place to provide for the recovery of the Cloud Service within hours if a
disaster occurs. You are responsible for your data backup, and associated recovery of your content.
 Tip: 
Different tools and features provide different levels of protection. The different features might be more or less suitable for your specific
HA or DR requirement.
Cloudant
   
411enable auditing of changes that are made to data by applications.
In-region data redundancy enables a High Availability capability that provides tolerance for failures that affect single systems within the region.
Cross-region redundancy for disaster recovery
The IBM Cloudant replication feature helps you build a flexible disaster recovery capability into your applications. The main way to enable disaster
recovery is to use IBM Cloudant replication to create redundancy across regions. The result 
is that your application can tolerate the situation where
one or more regions isn't available.
The basic steps in creating cross-region redundancy are included in the following list:
a
. 
Create IBM Cloudant accounts in two or more regions.
b
. 
Create databases in each region as needed.
c
. 
For databases that must be stored with cross-region redundancy, set up bidirectional continuous replications between the corresponding
databases in each account.
d
. 
Design and implement your applications so that data requests are routed depending on whether your environment is an Active-Passive or
Active-Active configuration. For more information about setting up cross-region redundancy, see 
Configuring IBM Cloudant for cross-region
disaster recovery
.
When you design your applications to work with data across multiple regions, consider the following points:
Applications can send requests to the database hosted nearest to their physical location. This use of proximity can reduce network latency and
improve response times. This configuration is referred to as an "Active-Active" method. 
An actve-active method is characterized by the
concurrent use of multiple copies of data. Applications that work within an active-active configuration must have a 
strategy for handling
conflicts
 
to avoid problems with multiple copies of data.
Applications can request data from a single region by default. If the region isn't available, the application can switch to requesting data from
another region. This configuration is referred to as an "Active-Passive" method. An 
active-passive method is characterized by the active use of
only one set of data at a time.
An application might use a hybrid configuration, where a single account is used for all data write requests, and other locations as used
exclusively for read-only requests. This configuration is considered Active-Active for reads.
In a disaster scenario, your application must reroute data requests to access the accounts that are hosted in the regions that are still online.
This requirement means that your application must detect the loss of a region, and then reroute 
data requests.
In summary, cross-region redundancy is similar to a high availability capability, but applies to failures that affect an entire region. Configuring your
applications to work correctly with cross-redundancy configurations provides real disaster 
recovery capability. Therefore, the applications can
continue working if the data in one region isn't available for an amount of time. IBM Cloudant replication helps ensure data synchronization between
regions. Your applications must "fail 
over" to copies of your data that is stored in other regions.
Database backup and recovery
In-region automatic data redundancy
 provides applications with high availability access to data. 
Cross-region redundancy for disaster recovery
provides applications with a means of recovering from a disaster. However, both of these capabilities focus on maintaining access only 
to the 
current
copy of your data.
People and applications can make mistakes and change data in unintended ways. The applications themselves can implement some protection, but
sometimes undesirable changes get through. It's useful to be able to restore data from a previous point 
in time. Database backups support this
requirement.
In addition to protecting your data with high availability and disaster recovery features, consider dumping your database data to a separate location
at periodic, regular intervals. Ensure you check and test the backups for confidence that they're 
complete and correct.
IBM Cloudant supports tools that help you dump the JSON content in databases to a file, and later restore databases from those files.
Specifically, IBM Cloudant supports tools that help you perform the following tasks:
Backup complete databases to a file that is suitable for further processing and off-site storage.
Restore complete databases from a previous state that is contained in your backup file.
The tools that are supported by IBM Cloudant have the following limitations:
_security
 settings aren't backed up by the tools.
Attachments aren't backed up by the tools.
Backups aren't precisely accurate "point-in-time" snapshots. The reason is that the documents in the database are retrieved in batches, but
other applications might be updating documents at the same time. Therefore, the data in the 
database can change between the times when
Cloudant
   
412the first and last batches are read.
Index definitions held design documents are backed up, but when data is restored the indexes must be rebuilt. This rebuilding might take a
considerable amount of time, depending on how much data is restored.
Next steps with your data protection strategies
You can develop applications that build on basic IBM Cloudant functions and supported tools to enable more complex data protection strategies.
Example scenarios are shown in the following list:
Restoring single documents from previous states.
Storing multiple previous document states to allow for restores from older backups.
Migrating older data to cheaper storage, for more cost-effective retention.
The backup tools consist of an open source node.js command-line application and library. It's available on 
NPM
.
For ideas and examples that show how to integrate the tools into your data protection strategy, see the 
IBM Cloudant backup and recovery guide
.
Configuring IBM Cloudant for cross-region disaster recovery
The 
IBM Cloudant disaster recovery guide
 explains that one way to enable disaster recovery is to use IBM Cloudant replication to create redundancy
across regions.
For more information, see how to 
retrieve replication scheduler documents
 and monitor replication status.
You can configure replication in IBM® Cloudant® for IBM Cloud® by using an "active-active" or "active-passive" topology across data centers.
The following diagram shows a typical configuration that uses two IBM Cloudant accounts, one in each region:
Figure 1. Example active-active architecture
Remember these important facts:
Within each data center, IBM Cloudant already offers high availability by storing data in triplicate across three servers.
Replication occurs at the database rather than account level and must be explicitly configured.
IBM Cloudant doesn't provide any Service Level Agreements (SLAs) or certainties about replication latency. IBM Cloudant doesn't monitor
Cloudant
   
413individual replications. Your own strategy for detecting failed replications and restarting them is advisable.
Before you begin an active-active deployment
Go to the 
IBM Cloud Support portal
 if you need help with how to model data to handle conflicts effectively.
Overview
In the following material, a bidirectional replication is created. This configuration allows two databases to work in an active-active topology.
The configuration assumes that you have two accounts in different regions:
myaccount-dc1.cloudant.com
myaccount-dc2.cloudant.com
After these accounts are created, follow these steps:
a
. 
Create
 a pair of peer databases within the accounts.
b
. 
Set up
 API keys to use for the replications between these databases.
c
. 
Grant appropriate permissions.
d
. 
Set up replications.
e
. 
Test replications are working as expected.
f
. 
Configure application and infrastructure for either active-active or active-passive use of the databases.
Step 1. Create your databases
Create the databases
 that you want to replicate between within each account.
In this example, a database that is called 
mydb
 is created.
The names that are used for the databases in this example aren't important, but using the same name is clearer.
curl 
"https://myaccount-dc1.cloudant.com/mydb"
 -XPUT -u myaccount-dc1
curl 
"https://myaccount-dc2.cloudant.com/mydb"
 -XPUT -u myaccount-dc2
Step 2. Create an API key for your replications
It's a good idea to use an 
API key
 for continuous replications. The advantage is that if your primary account details change, for example after a
password reset, your replications can continue unchanged.
API keys aren't tied to a single account. This means that a single API key can be created, then granted suitable database permissions for both
accounts.
For example, the following command requests an API key for the account 
myaccount-dc1
:
curl -XPOST 
"https://myaccount-dc1.cloudant.com/_api/v2/api_keys"
 -u myaccount-dc1
A successful response is similar to the following abbreviated example:
{
  
"password"
:
 
"YPN...Tfi"
,
  
"ok"
:
 
true
,
  
"key"
:
 
"ble...igl"
}
Step 3. Grant access permission
 Note: 
For an active-active deployment, a strategy for managing conflicts must be in place, so be sure to understand how 
replication
 and
conflicts
 
work before you consider this architecture.
 Important: 
Take careful note of the password. It isn't possible to retrieve the password later.
Cloudant
   
414Give the API Key 
permission
 to read and to write on both databases.
If you also need to replicate indexes, assign admin permissions.
Use the IBM Cloudant Dashboard, or see the 
authorization
 information for details of how to grant permissions programmatically.
Step 4. Set up replications
Replications in IBM Cloudant are always uni-directional: from one database to another database. To replicate both ways between two databases,
two replications are required, one for each direction.
A replication is created in each account that uses the API Key that is created 
earlier
.
First, create a replication from database 
myaccount-dc1.cloudant.com/mydb
 to database 
myaccount-dc2.cloudant.com/mydb
.
curl -XPOST 
"https://myaccount-dc1.cloudant.com/_replicator"
 -u myaccount-dc1
 -H 
"Content-Type: application/json"
 -d 
'{ "_id": "mydb-myaccount-dc1-to-myaccount-dc2",
 "source": "https://ble...igl:YPN...Tfi@myaccount-dc1.cloudant.com/mydb",
 "target": "https://ble...igl:YPN...Tfi@myaccount-dc2.cloudant.com/mydb",
 "continuous": true
}'
Next, create a replication from database 
myaccount-dc2.cloudant.com/mydb
 to database 
myaccount-dc1.cloudant.com/mydb
.
curl -XPOST 
"https://myaccount-dc2.cloudant.com/_replicator"
 -u myaccount-dc2
 -H 
"Content-Type: application/json"
 -d 
'{ "_id": "mydb-myaccount-dc2-to-myaccount-dc1",
 "source": "https://ble...igl:YPN...Tfi@myaccount-dc2.cloudant.com/mydb",
 "target": "https://ble...igl:YPN...Tfi@myaccount-dc1.cloudant.com/mydb",
 "continuous": true
}'
Step 5. Test your replication
Test the replication processes by creating, modifying, and deleting documents in either database.
After each change in the database, check that you can also see that change in the other database.
Step 6. Configure your application
The databases are set up to remain synchronized with each other.
The next decision is whether to use the databases in an 
active-active
 or 
active-passive
 manner.
Active-active
In an active-active configuration, different application instances can write to different databases.
For example, application "A" might write to database 
myaccount-dc1.cloudant.com/mydb
, while application "B" might write to database
myaccount-dc2.cloudant.com/mydb
.
This configuration offers several benefits:
Load can be spread over several accounts.
You can configure applications to access an account with reduced latency (not always the geographically closest).
An application can be set up to communicate with the "nearest" IBM Cloudant account. For applications hosted in DC1, it's appropriate to set their
IBM Cloudant URL to 
"https://myaccount-dc1.cloudant.com/mydb"
. 
Similarly, for applications that are hosted in DC2, you would set their IBM
Cloudant URL to 
"https://myaccount-dc2.cloudant.com/mydb"
.
 Note: 
If this step fails because the 
_replicator
 database doesn't exist, create it.
Cloudant
   
415Active-passive
In an active-passive configuration, all instances of an application are configured to use a primary database. However, the application can fail over to
the other backup database, if circumstances make it necessary. The failover might be implemented 
within the application logic itself, or by using a
load balancer, or by using some other means.
A simple test of whether a failover is required would be to use the main database endpoint as a "heartbeat". For example, a simple 
GET
 request that
is sent to the main database endpoint normally returns 
details about the database
. If no response is received, it might indicate that a failover is
necessary.
Other configurations
You might consider other hybrid approaches for your configuration.
For example, in a "Write-Primary, Read-Replica" configuration, all writes go to one database, but the read load is distributed among the replicas.
Step 7. Next steps
Consider monitoring the 
replications
 between the databases. Use the data to determine whether your configuration might be optimized
further.
Consider how your design documents and indexes are deployed and updated. You might find it more efficient to automate these tasks.
Failing over between IBM Cloudant regions
Typically, the process of managing a failover between regions or datacenters is handled higher up within your application stack, for example by
configuring application server failover changes, or by balancing the load.
IBM Cloudant doesn't provide a facility for you to manage explicitly any failover or reroute requests between regions. This constraint is partly for
technical reasons, and partly because the conditions under when it might happen tend to be application-specific. 
For example, you might want to
force a failover in response to a custom performance metric.
However, if you decide that you need the ability to manage failover, consider the following possible options:
Put your own 
HTTP proxy in front of IBM Cloudant
. Configure your application to talk to the proxy rather than the IBM Cloudant instance. This
configuration 
means that the task of changing the IBM Cloudant instances that are used by applications can be handled through a modification
to the proxy configuration rather than a modification to the application settings. Many proxies can balance the 
load, based on user-defined
health checks.
Use a global load balancer such as 
IBM Cloud® Internet Services
 to route to IBM Cloudant. This option requires 
a 
CNAME
 definition that routes
to different IBM Cloudant accounts, based on a health check or latency rule.
Recovering from failover
If a single IBM Cloudant instance is unreachable, avoid redirecting traffic back to it as soon as it becomes reachable again. The reason is that some
time is required for intensive tasks such as synchronizing the database state from any peers, 
and ensuring that indexes are up to date.
It's helpful to have a mechanism for monitoring these tasks to help decide when a database is in a suitable state to service your production traffic.
As a guide, a typical list of checks to apply include:
Replications
Indexes
Replications
Are any replications in an error state?
Do any replications need restarting?
How many pending changes are still waiting for replication into the database?
For more information, see how to 
retrieve replication scheduler documents
 and monitor replication status.
 Note: 
If you implement rerouting for requests or failover based on a health test, you might want to incorporate corresponding checks to
avoid premature rerouting back to a service instance that is still recovering.
 Note: 
If a database is being changed continuously, the replication status is unlikely to be zero. You must decide what status threshold is
Cloudant
   
416Indexes
Are the indexes sufficiently up to date? Verify that indexes are updated by using the 
active tasks
 endpoint.
Test the level of "index readiness" by sending a query to the index, and deciding whether it returns within an acceptable time.
IBM Cloudant backup and recovery
Although data is stored redundantly within an IBM Cloudant cluster, it's important to consider extra backup measures. For example, redundant data
storage doesn't protect against mistakes when data is changed.
Introducing CouchBackup
IBM Cloudant provides a supported tool for snapshot backup and restore. The tool is called CouchBackup, and is open source. It's a 
node.js
 library,
and you can install it on 
NPM
.
The CouchBackup package includes the library and two command-line tools:
a
. 
couchbackup
, which dumps the JSON data from a database to a backup text file.
b
. 
couchrestore
, which restores data from a backup text file to a database.
Backing up your IBM Cloudant data
You can do a simple backup by using the 
couchbackup
 tool. To back up the 
animaldb
 database to a text file called 
backup.txt
, you might use a
command similar to the following example:
couchbackup --url 
"
$SERVICE_URL
"
 --db animaldb > backup.txt
The 
NPM readme file
 details other options, including the ones in this list:
Environment variables to set the names of the database and URL.
Using a log file to record the progress of a backup.
The ability to resume an interrupted backup.
Sending the backup text file to a named output file, rather than redirecting the 
stdout
 output.
Restoring your IBM Cloudant data
To restore your data, use the 
couchrestore
 tool. Use 
couchrestore
 to import the backup file into a new IBM Cloudant database. Then, ensure
that you build all indexes before any application tries to use the restored 
data.
For example, to restore the data that was backed up in the earlier example:
couchrestore --url 
"https://myaccount.cloudant.com"
 --db newanimaldb < backup.txt
The 
NPM readme file
 provides details of other restore options.
Limitations
acceptable, or what represents an error state.
 Note: 
Review the 
IBM® Cloudant® for IBM Cloud® Disaster Recovery guide
 to understand where backup fits in with the other features that
IBM Cloudant 
offers to support Disaster Recovery (DR) and High Availability (HA) requirements.
 Important: 
The CouchBackup tools have 
limitations
.
 Note: 
This option is only available with the log file for the interrupted backup.
 Important: 
The CouchBackup tools have 
limitations
.
Cloudant
   
417The CouchBackup tools have the following limitations:
_security
 settings aren't backed up by the tools.
Attachments aren't backed up by the tools.
Backups aren't precise "point-in-time" snapshots. The reason is that the documents in the database are retrieved in batches, but other
applications might be updating documents at the same time. Therefore, data in the database can 
change between the times when the first and
last batches are read.
Index definitions that are held in design documents are backed up, but the content of indexes isn't backed up. This limitation means that when
data is restored, the indexes must be rebuilt. The rebuilding might take a considerable amount of 
time, depending on how much data is
restored.
Using the tools
The 
NPM page
 details the basics of using the command-line tools for backup and restore of data. The following examples show how to put those
details 
into practice by describing the use of the tools for specific tasks.
The CouchBackup package provides two ways of using its core functions.
The command-line tools can be embedded into standard UNIX™ command pipelines. For many scenarios, a combination of 
cron
 and simple
shell scripting of the 
couchbackup
 application is sufficient.
A library usable from Node.js. The library allows more complicated backup processes to be created and deployed, such as determining
dynamically which databases must be backed up.
Use either the command-line backup tool, or the library with application code, to enable backup from IBM Cloudant databases as part of more
complicated situations. A useful scenario is scheduling backups by using 
cron
, and automatically 
uploading data to 
Cloud Object Storage
 for long-
term retention.
Command line scripting examples
You frequently need to meet the following two requirements:
Saving disk space by 
'zipping' the backup
 file as you create it.
Creating a backup of a database automatically at 
regular intervals
.
Compressing a backup file
The 
couchbackup
 tool can write a backup file to disk directly, or stream the backup to 
stdout
. Streaming to 
stdout
 enables data to be
transformed before it is written to disk. This feature is used to 
compress data within the stream.
couchbackup --url 
"
$SERVICE_URL
"
 \
  --db 
"animaldb"
 | gzip > backup.gz
In this example, the 
gzip
 tool accepts the backup data directly through its 
stdin
, compresses the data, and emits it through 
stdout
. The
resulting compressed data stream is then redirected and written 
to a file called 
backup.gz
.
If the database requires you to supply access credentials, use 
$SERVICE_URL
 with the form 
https://$USERNAME:$PASSWORD@$ACCOUNT
, for
example, 
https://myusername:mypassword@myhost.cloudant.com
.
It's straightforward to extend the pipeline if you want to transform the data in other ways. For example, you might want to encrypt the data before it's
written to disk. You might also want to write the data directly to an object store service 
by using their command-line tools.
Hourly or daily backups that use 
cron
The 
cron
 scheduling tool can be set up to take snapshots of data at regular intervals.
A useful starting point is to get 
couchbackup
 to write a single backup to a file, where the file name includes the current date and time, as shown in
the following example:
couchbackup --url 
"https://
$USERNAME
:
$PASSWORD
@
$ACCOUNT
.cloudant.com"
 \
  --db 
"animaldb"
 > animaldb-backup-`date -u 
"+%Y-%m-%dT%H:%M:%SZ"
`.bak
After you check the command to ensure it works correctly, it can be entered into a 'cron job':
a
. 
Install the CouchBackup tools on the server that you want to do the backups.
Cloudant
   
418b
. 
Create a folder to store the backups.
c
. 
Create a 'cron entry' that describes the frequency of the backup.
You can create a cron entry by using the 
crontab -e
 command. See your system documentation for specific details on the 'cron' options.
A cron entry that runs a daily backup looks similar to the following example:
0 5 * * * couchbackup --url 
"https://
$USERNAME
:
$PASSWORD
@
$ACCOUNT
.cloudant.com"
 --db 
"animaldb"
 >
 
/path/to/folder/animaldb-backup-`date -u 
"+%Y-%m-%dT%H:%M:%SZ"
`.bak
This cron entry creates a daily backup at 05:00. You can modify the cron pattern to run hourly, daily, weekly, or monthly backups as needed.
Using CouchBackup as a library
The 
couchbackup
 and 
couchrestore
 command-line tools are wrappers around a library that can be used in your own Node.js applications.
The library is useful for more complicated scenarios, for example:
Backing up several databases in one task. You might do this backup by identifying all the databases by using the 
_all_dbs
 call, then doing a
backup of 
each database individually.
Longer pipelines increase the risk of errors. By using the CouchBackup library, your application can detect and address any error at the earliest
opportunity.
For more information, see the 
NPM page
.
The following script sample shows how to combine the 
couchbackup
 library with use of IBM® Cloud Object Storage. This code illustrates how you
might use Cross Region S3 API to back up a database to an object store.
/*
  Backup directly from Cloudant to an S3 bucket via a stream.
  @param {string} couchHost - URL of database root
  @param {string} couchDatabase - backup source database
  @param {object} s3Client - S3 client object
  @param {string} s3Bucket - Destination S3 bucket (must exist)
  @param {string} s3Key - Destination object's key (shouldn't exist)
  @param {boolean} shallow - Whether to use couchbackup's shallow mode
  @returns {Promise}
*/
function
 
backupToS3
(
sourceUrl, s3Client, s3Bucket, s3Key, shallow
) {
  
return
 
new
 
Promise
(
(
resolve, reject
) =>
 {
    
debug
(
'Setting up S3 upload to ${s3Bucket}/${s3Key}'
);
    
// A pass through stream that has couchbackup's output
    
// written to it and it then read by the S3 upload client.
    
// It has a 10 MB internal buffer.
    
const
 streamToUpload = 
new
 stream.
PassThrough
({
highWaterMark
: 
10485760
});
    
// Set up S3 upload.
    
const
 params = {
      
Bucket
: s3Bucket,
      
Key
: s3Key,
      
Body
: streamToUpload
    };
    s3Client.
upload
(params, 
function
(
err, data
) {
      
debug
(
'S3 upload done'
);
      
if
 (err) {
        
debug
(err);
        
reject
(
new
 
Error
(
'S3 upload failed'
));
        
return
;
      }
      
debug
(
'S3 upload succeeded'
);
      
debug
(data);
      
resolve
();
    }).
httpUploadProgress
 = 
(
progress
) =>
 {
 Note: 
A prerequisite for the code is that you initialize the S3 client object for IBM Cloud Object Storage by following the instructions in 
IBM
Cloud Object Storage - S3 API Intro
.
Cloudant
   
419      
debug
(
'S3 upload progress: ${progress}'
);
    };
    
debug
(
'Starting streaming data from ${sourceUrl}'
);
    couchbackup.
backup
(
      sourceUrl,
      streamToUpload,
      
(
err, obj
) =>
 {
        
if
 (err) {
          
debug
(err);
          
reject
(
new
 
Error
(
'CouchBackup failed with an error'
));
          
return
;
        }
        
debug
(
'Download from ${sourceUrl} complete.'
);
        streamToUpload.
end
();  
// must call end() to complete S3 upload.
        
// resolve() is called by the S3 upload
      }
    );
  });
}
Other disaster recovery options
Return to the 
IBM Cloudant Disaster Recovery guide
 to find out about the other features IBM Cloudant offers for a full disaster recovery setup.
Cloudant
   
420Enhancing security for IBM Cloudant
Managing access for IBM Cloudant
IBM Cloud® Identity and Access Management provides a unified approach to managing user identities, services, and access control.
The following text describes the integration of IBM® Cloudant® for IBM Cloud® with IBM Cloud Identity and Access Management. The following topics
are discussed:
Differences between IBM Cloudant legacy access controls and IBM Cloud IAM access controls.
Advantages and disadvantages of each to help you decide which to use.
How to use IAM within IBM Cloudant's client libraries by using HTTP calls.
Description of the IAM actions and roles available within IBM Cloudant.
For more information, see an overview of 
IAM
 that includes the following topics:
Manage user and service IDs.
Manage available credentials.
Use IAM access policies that allow and revoke access to IBM Cloudant service instances.
Differences between IBM Cloudant legacy access controls and IAM access controls
The following section provides a brief overview of the differences between IBM Cloudant legacy access controls and IBM Cloud IAM's access control
mechanisms.
IBM Cloud Identity and Access Management
Centrally managed access management across IBM Cloud.
Allow a user or service to access many different resources by using the same set of credentials (for example, same username and password or
IAM API key).
IAM API keys can be granted access to account management functions, like creating new databases.
IBM Cloudant legacy access controls
Unique to IBM Cloudant.
Access to each service instance requires its own set of credentials.
Uses HTTP basic authentication with credentials that are not bound to an individual user or service.
IBM Cloudant API keys can be granted permissions only at a database level.
API key notes
In this document, wherever API keys are mentioned it refers to IAM API keys. IBM Cloudant legacy access controls also have a concept of API keys,
and any discussion about IBM Cloudant legacy credentials or username and password combinations 
also includes IBM Cloudant API keys.
Enabling IAM with IBM Cloudant
All IBM Cloudant service instances provisioned July 2018 or later are provisioned in Resource Groups and are enabled with IBM Cloud IAM.
Optionally, you can choose to also enable the IBM Cloudant legacy authentication mechanism. When you provision 
a new IBM Cloudant instance
from the IBM Cloud catalog, select one of the following authentication methods.
Use both legacy credentials and IAM
This mode means that both IAM and legacy credentials can be used to access the account. In particular, both IAM and legacy sets of
credentials are provided to all applications bound to the account and service credentials generated.
Use only IAM
This mode means that only IAM credentials are provided by using Service binding and credential generation.
 Important: 
When you use IAM roles other than 
Manager
, such as 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
, you 
must
 use 
Use only
Cloudant
   
421IBM Cloudant service instances that are provisioned previously in a Cloud Foundry org and space can be migrated to a Resource Group. After you
migrate to a Resource Group, the instance is enabled with IBM Cloud IAM. For more information, see 
the 
Resource Groups FAQ
 about how to
migrate.
IBM Cloudant API keys and 
Use only IAM
Use of IBM Cloudant API keys alongside IAM is possible but 
not recommended
. This recommendation is made because IBM Cloudant API keys and
permissions are not visible or manageable by using the IAM policy interface, rendering 
holistic access management impossible.
The choice between 
Use only IAM
 or 
Use both legacy credentials and IAM
 affects the following factors:
a
. 
Whether legacy IBM Cloudant account-level credentials are available to manage databases and other account-level actions.
b
. 
The style of credentials that are delivered during service credential generation.
In particular, IBM Cloudant API keys can still be used to manage database access. These credentials must be generated and configured by using the
HTTP API.
Provisioning by using the command line
When you provision a new IBM Cloudant instance from the command line, provide an option to the 
ibmcloud
 tool by using the 
-p
 parameter to
enable or disable legacy credentials for an account. The option is passed in 
JSON format and is called 
legacyCredentials
.
To provision an instance as 
Use only IAM
 (recommended), run the following command:
ibmcloud resource service-instance-create  
"Instance Name"
 \
    cloudantnosqldb Standard us-south \
    -p {
"legacyCredentials"
: 
false
}
To provision an instance as 
Use both legacy credentials and IAM
, run the following command:
ibmcloud resource service-instance-create  
"Instance Name"
 \
    cloudantnosqldb Standard us-south \
    -p {
"legacyCredentials"
: 
true
}
Service credential JSON examples for each option
The choice between 
Use only IAM
 and 
Use both legacy credentials and IAM
 access control affects how credentials are delivered to your application
when you bind and generate service credentials. When you generate credentials 
within the primary IBM Cloud IAM interface, API keys are shown in
that interface when generated.
You can also generate credentials from the Service Credentials section of a service instance. Generating service credentials this way creates a
service credentials JSON blob that can be pasted into applications with all the details that are 
needed to access the service instance.
Next, you can see what the service credential JSON looks like and what each value means.
When you select 
Use only IAM
, the service credentials that are generated contain only IAM values, and look like the following example.
{
  
"apikey"
:
 
"MxVp86XHkU82Wc97tdvDF8qM8B0Xdit2RqR1mGfVXPWz"
,
  
"iam_apikey_description"
:
 
"Auto generated apikey during resource-key [...]"
,
  
"iam_apikey_name"
:
 
"auto-generated-apikey-050d21b5-5f[...]"
,
  
"iam_role_crn"
:
 
"crn:v1:bluemix:public:iam::::serviceRole:Manager"
,
  
"iam_serviceid_crn"
:
 
"crn:v1:staging:public:iam-identity::[...]"
,
  
"url"
:
 
"https://76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"username"
:
 
"76838001-b883-444d-90d0-46f89e942a15-bluemix"
}
Each value in the previous JSON example must be interpreted by using the following definitions:
IAM
 to avoid supplying users with legacy 
credentials that include greater access permissions.
 Important: 
When you use IAM roles other than 
Manager
, such as 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
, you 
must
 use 
Use only
IAM
 to avoid supplying users with 
legacy credentials that include greater access permissions.
Cloudant
   
422apikey
IAM API key.
iam_apikey_description
Description of IAM API key.
iam_apikey_name
ID of IAM API key.
iam_role_crn
The IAM role that the IAM API key has.
iam_serviceid_crn
The CRN of service ID.
url
IBM Cloudant service URL.
username
The internal IBM Cloudant account name.
When you select 
Use both legacy credentials and IAM
, the service credentials that are generated contain both IAM and legacy credentials, and look
like the values in the following example.
{
  
"apikey"
:
 
"MxVp86XHkU82Wc97tdvDF8qM8B0Xdit2RqR1mGfVXPWz"
,
  
"host"
:
 
"76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"iam_apikey_description"
:
 
"Auto generated apikey during resource-key [...]"
,
  
"iam_apikey_name"
:
 
"auto-generated-apikey-050d21b5-5f[...]"
,
  
"iam_role_crn"
:
 
"crn:v1:bluemix:public:iam::::serviceRole:Manager"
,
  
"iam_serviceid_crn"
:
 
"crn:v1:staging:public:iam-identity::[...]"
,
  
"password"
:
 
"8fb6a16b48903e87b769e7f4968521e85c2394ed8f0e69b2769e56dcb27d2e76"
,
  
"port"
:
 
443
,
  
"url"
:
 
"https://<username>:<password>@76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"username"
:
 
"apikey-v2-58B528DF5397465BB6673E1B79482A8C"
}
Each value in the previous JSON example must be interpreted by using the following definitions:
apikey
IAM API key.
host
IBM Cloudant service hostname.
iam_apikey_description
Description of IAM API key.
iam_apikey_name
ID of IAM API key.
iam_role_crn
The IAM role that the IAM API key has.
iam_serviceid_crn
The CRN of service ID.
password
The IBM Cloudant legacy credential password.
port
IBM Cloudant service port.
url
Cloudant
   
423IBM Cloudant service URL, including embedded IBM Cloudant legacy credentials.
username
The IBM Cloudant legacy credential username.
Note the included 
username
 and 
password
 are always equivalent to IAM's Manager credentials. Therefore, the use of 
Use both legacy credentials
and IAM
 is insecure when used with 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
 IAM roles.
Must I use 
Use only IAM
 or 
Use both legacy credentials and IAM
?
If possible, 
Use only IAM
 is preferred. The major advantages for using IBM Cloud IAM are shown in the following list:
Management of access to IBM Cloudant with the standard tools of IBM Cloud rather than a combination of IBM Cloud and IBM Cloudant-
specific credential management.
Credentials can be easily revoked and rotated when you use IBM Cloud IAM.
Further description of the advantages and disadvantages of each approach follows.
Advantages and disadvantages of the two access control mechanisms
Overall, IBM Cloud IAM is the recommended authentication model. However, the primary disadvantages to the approach are if you have an existing
application or are unable to use an IBM Cloudant-supported client library.
Advantages of IAM mode
Manage access for many services by using one interface.
Revoke access to a user globally.
Account-level API keys that use service IDs.
Easy-to-rotate credentials.
Activity Tracker logs capture individual humans and services.
IAM federates with other identity systems, like enterprise LDAP repositories.
Fine-grained permissions (for example, 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
).
Disadvantages of IAM mode
If you are not using the supported libraries from IBM Cloudant, application changes are likely to be required to use IAM's API keys and access
tokens.
No database-level permissions (yet).
Some endpoints are not available. For more information, see 
unavailable endpoints
.
No way to specify a database as "public", that is, not requiring an authorized user to access.
Advantages of legacy mode
No need to change existing applications or client library dependencies.
Database-level permissions.
Disadvantages of legacy mode
Separate management of IBM Cloudant credentials, so unable to get full overview of all access within centralized interface.
Create a replication job by using IAM credentials only
Follow these instructions to generate IAM API keys, generate the bearer token, create the 
_replicator
 database, and create the replication job.
Generating IAM API keys for Source and Target and one for IBM Cloudant API access
In this exercise, the first two API keys are created so that the two instances can talk to each other during the replication process. The third API key is
for the user to access the IBM Cloudant API, create the 
_replicator
 database, 
and then add the replication document to it.
 Important: 
When you use IAM roles other than 
Manager
, such as 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
, you 
must
 use 
Use only
IAM
 to avoid supplying users with legacy 
credentials that include greater access permissions.
Cloudant
   
424Follow these steps to generate IAM API keys and API access for IBM Cloudant. You must write down the credentials that are requested in the
following steps to continue with the example.
a
. 
Log in to 
cloud.ibm.com
.
b
. 
From the Resource list, select 
Services
 and your Source instance.
a
. 
Click 
Service credentials
 and click 
New credential
.
b
. 
Name the new credential 
replicator-source
, and select the Manager role.
c
. 
Click 
Add
, and make note of its 
apikey
, which is under View Credentials in the Actions column.
c
. 
Repeat steps 2 through 2.c. for the Target instance.
a
. 
Create a credential called 
replicator-target
 with the Manager role.
b
. 
Make note of its IAM API key, which is under View Credentials in the Actions column.
d
. 
Select the Source instance, and click 
Service credentials
 and 
New credential
.
a
. 
Name the new credential 
apiaccess
, and select the Manager role.
b
. 
Make note of the actual IAM API key under View Credentials in the Actions column.
e
. 
Make note of Source and Target instance URLs.
Depending on your workflow, instead of creating a service-level credential (step 4), you can use a personal IAM API key, as detailed in 
Creating an
API key
.
You can also complete these steps on the command line by using the 
IBM Cloud CLI tool chain
.
Generating a bearer token to authenticate against the IBM Cloudant API
In step 4.b., you wrote down the 
apiaccess
 key. Use that key now:
curl -k -X POST \
  --header 
"Content-Type: application/x-www-form-urlencoded"
 \
  --header 
"Accept: application/json"
 \
  --data-urlencode 
"grant_type=urn:ibm:params:oauth:grant-type:apikey"
 \
  --data-urlencode 
"apikey=aSCsx4...2lN97h_2Ts"
 \
  
"https://iam.cloud.ibm.com/identity/token"
The 
apiaccess
 key returns the following information (abbreviated):
{
   
"access_token"
: 
"eyJraWQiOiIyMDE5MD...tIwkCO9A"
,
   
"refresh_token"
: 
"ReVbNrHo3UA38...mq67g"
,
   
"token_type"
: 
"Bearer"
,
   
"expires_in"
: 3600,
   
"expiration"
: 1566313064,
   
"scope"
: 
"ibm openid"
}
Create an environment variable to save some typing by using the value under the 
access_token
 key in the response data:
export
 TOK=
"Bearer eyJraWQiOiIyMDE5MD...tIwkCO9A"
Creating the 
_replicator
 database on the Source side
URL is the Source instance URL that you previously wrote down in step 4.b.
curl -k -X PUT \
     -H
"Content-type: application/json"
 \
     -H
'Authorization: '
"
$TOK
"
''
 \
     
'https://d43caf1b-e2c8-4d3e-9b85-1d04839fa68f-bluemix.cloudant.com/_replicator'
 Note: 
Ensure that you select the specified instance, either the Source or Target.
Cloudant
   
425See the results in the following example:
{
"ok"
: 
"true"
}
Creating the replication job
Create a file called 
data.json
 that contains the following information. The two keys are the Source and Target API keys that are created in the
beginning, and the Source and Target instance URLs, with database names added.
{
  
"source"
: {
    
"url"
: 
"https://d43caf1b-e2c8-4d3e-9b85-1d04839fa68f-bluemix.cloudant.com/source"
,
    
"auth"
: {
      
"iam"
: {
        
"api_key"
: 
"xju1...TxuS"
      }
    }
  },
  
"target"
: {
    
"url"
: 
"https://dbc68dd8-f69f-4083-97dd-bf0a3e1a467a-bluemix.cloudant.com/target"
,
    
"auth"
: {
      
"iam"
: {
        
"api_key"
: 
"UElc7...QIaL01Bjn"
      }
    }
  },
  
"create_target"
: 
true
,
  
"continuous"
: 
true
}
Now, write a replication document called 
source_dest
 to the 
_replicator
 database on the Source instance.
curl -k -X PUT \
     -H
"Content-type: application/json"
 \
     -H
'Authorization: '
"
$TOK
"
''
 \
     
'https://d43caf1b-e2c8-4d3e-9b85-1d04839fa68f-bluemix.cloudant.com/_replicator/source_dest'
 -d@data.json
See the results in the following example:
{
"ok"
:
true
,
"id"
:
"source_dest"
,
"rev"
:
"1-89b01e42968acd5944ed657b87c49f0c"
}
Removing IBM Cloudant legacy credentials from an instance
IBM Cloud IAM is the recommended authentication model. For security purposes, you can request to remove the IBM Cloudant legacy credentials so
that only IAM authentication can be used for the instance. The correct process to remove legacy credentials 
is shown in the following steps:
a
. 
Ensure that the IBM Cloudant instance has IAM authentication that is enabled. If the instance is deployed in a Cloud Foundry org and space,
migrate it to a Resource Group by using the 
Resource Groups FAQ
.
b
. 
Update your application to use IAM authentication instead of IBM Cloudant legacy authentication.
c
. 
Generate 
new service credentials
 as needed.
d
. 
Open a new IBM Cloud support case that requests the removal of IBM Cloudant legacy credentials for your instance. Include the username of
the instance as shown in the service credentials. For more information, see 
Locating your service credentials
.
e
. 
After support replies that the legacy credentials were removed, any service credentials that were created before removal contain legacy
username and password details that no longer work. It is recommended to remove any of these service credential 
entries.
Making requests to instances by using IAM credentials
Now, the following section describes how to use IBM Cloudant with service instances through IAM authentication. It uses the details from the
Service credential JSON examples for each option
.
IBM Cloud IAM requires that an IAM API key is exchanged for a time-limited access token before you make a request to a resource or service. The
access token is then included in the 
Authorization
 HTTP header to the service. When 
the access token expires, the consuming application must
Cloudant
   
426handle getting a new one from the IAM token service. For more information, see 
Getting an IBM Cloud IAM token by using an API key
 
documentation
for more details.
IBM Cloudant's official client libraries handle obtaining a token from an API key for you. You can access IBM Cloudant directly by using an HTTP
client rather than an IBM Cloudant client library. However, you must handle exchanging and refreshing 
a time-limited access token by using an IAM
API key with the IAM token service. After a token expires, IBM Cloudant returns an HTTP 
401
 status code.
Required client library versions
IAM connectivity is available in the latest release of all supported client libraries. For more information, see 
Client libraries
.
Java
The following link provides the latest supported version of the IBM Cloudant Java™ library:
cloudant-java-sdk
For an example that uses IBM Cloudant SDK for Java, see the 
API and SDK documentation
.
Node.js
The following link provides the latest supported version of the IBM Cloudant Node.js library:
cloudant-node-sdk
For an example that uses IBM Cloudant SDK for Node, see the 
API and SDK documentation
.
Python
The following link provides the latest supported version of the IBM Cloudant Python library:
cloudant-python-sdk
For an example that uses IBM Cloudant SDK for Python, see the 
API and SDK documentation
.
Go
The following link provides the latest supported version of the IBM Cloudant Go library:
go-sdk
For an example that uses IBM Cloudant SDK for Go, see the 
API and SDK documentation
.
Access by using HTTP client
IBM Cloud IAM requires that an IAM API key is exchanged for a time-limited access token before you make a request to a resource or service. The
access token is then included in the 
Authorization
 HTTP header to the service. When 
the access token expires, the client must handle getting a
new one from the IAM token service.
As stated previously, if you use IBM Cloud IAM, it requires that you first exchange an IBM API key for a time-limited access token. After that, you use
the token to authenticate against the IBM Cloudant API.
In Python, an example might look like:
import
 time
import
 requests
API_KEY = 
"MxVp86XHkU82Wc97tdvDF8qM8B0Xdit2RqR1mGfVXPWz"
ACCOUNT = 
"76838001-b883-444d-90d0-46f89e942a15-bluemix"
def
 
get_access_token
(
api_key
):
    
"""Retrieve an access token from the IAM token service."""
    token_response = requests.post(
        
"https://iam.cloud.ibm.com/identity/token"
,
        data={
            
"grant_type"
: 
"urn:ibm:params:oauth:grant-type:apikey"
,
            
"response_type"
: 
"cloud_iam"
,
            
"apikey"
: api_key
        },
Cloudant
   
427        headers={
            
"Accept"
: 
"application/json"
        }
    )
    
if
 token_response.status_code == 
200
:
        
print
 
"Got access token from IAM"
        
return
 token_response.json()[
'access_token'
]
    
else
:
        
print
 token_response.status_code, token_response.json()
        
return
 
None
def
 
main
(
api_key, account
):
    access_token = 
None
    
while
 
True
:
        
if
 
not
 access_token:
            access_token = get_access_token(api_key)
        
if
 access_token:
            response = requests.get(
                
"https://{0}.cloudant.com/_all_dbs"
.
format
(account),
                headers={
                    
"Accept"
: 
"application/json"
,
                    
"Authorization"
: 
"Bearer {0}"
.
format
(access_token)
                }
            )
            
print
 
"Got Cloudant response, status code"
, response.status_code
            
if
 response.status_code == 
401
:
                
print
 
"Token has expired."
                access_token = 
None
        time.sleep(
1
)
if
 __name__ == 
"__main__"
:
    main(API_KEY, ACCOUNT)
Using IAM IP allowlisting with Cloudant
You can enable IAM IP address access restrictions when you're using IBM Cloudant.
To enable IAM IP address access restrictions, you must ensure that the Cloud Identity and Access Management (IAM) 
IP allowlist
 is configured so
that the IBM Cloudant 
service can still function. IAM is used by IBM Cloudant when authenticating requests to the IBM Cloudant API that pass IAM
credentials, and when running 
replications
 
that are configured to authenticate using IAM API keys.
Creating a Network Zone
To add IBM Cloudant to your 
IAM access list
, you must first create a 
Network Zone
 that includes the IBM Cloudant service.
To create a network zone, complete the following steps.
a
. 
In the IBM Cloud console, click 
Manage
 > 
Context-based restrictions
, and select 
Network zones
.
b
. 
Click 
Create
.
c
. 
Enter a unique name (e.g. 
cloudant-network
) and, optionally, a description.
d
. 
Under 
Reference a service
, select service type 
IAM Services
 and service 
IBM Cloudant
. Click 
Add
 to associate the 
IBM Cloudant
 IP
addresses with your network zone.
e
. 
Click 
Next
 to review your network zone.
f
. 
Click 
Create
.
Referencing the Network Zone in the IAM IP allowlist
The 
Network Zone
 created above, called 
cloudant-network
, can now be used in your 
IAM IP allowlist
.
a
. 
In the IBM Cloud console, click 
Manage
 > 
Access (IAM)
, and select 
Settings
.
 Note: 
IAM tokens can be valid for 
up to 60 minutes
. This means that changes to IAM IP allowlisting may not fully take effect until this
validation period has expired, 
as allowlisting is only enforced at token creation time.
Cloudant
   
428b
. 
From the Account section, enable the 
IP address access
 setting.
c
. 
In the 
Allowed IP addresses
 field, add the name of the Network Zone you created above (e.g. 
cloudant-network
).
d
. 
Click 
Save
.
Roles and actions
The following tables include a complete list of IBM Cloudant's IAM roles and actions, and a mapping of what actions are allowed for each IAM system
role.
IBM Cloudant roles
The following table lists the available IAM service roles for IBM Cloudant and a brief description of each.
Table 1. IAM service roles for IBM Cloudant
Role
Description
Manager
Includes the ability to access all endpoints and perform all administrative functions on an instance, such as creating
databases, changing capacity, reading and writing data and indexes, and accessing the Dashboard.
Writer
Includes the ability to read and write to all databases and documents, but not able to create indexes.
Reader
Includes the ability to read all databases and documents, but not able to write new documents or create indexes.
Monitor
Includes the ability to read monitoring endpoints, such as 
_active_tasks
 and replication 
_scheduler
 endpoints.
Checkpointer
Includes the ability to write replication 
checkpointer
 
_local
 documents. Required on source databases during replication.
Manager is inclusive of all actions of Reader and Writer, and Writer is inclusive of all actions of Reader.
IBM Cloudant actions
The following table describes the available IAM actions and roles. For fine-grained authorization, you can use the roles of 
Manager
, 
Reader
,
Writer
, 
Monitor
, or 
Checkpointer
.
Method
Endpoint
Action name
GET/PUT
/_api/v2/db/<path:db>/_security
cloudantnosqldb.sapi.db-security
GET
/_api/v2/user/capacity/throughput
cloudantnosqldb.capacity-
throughput.read
PUT
/_api/v2/user/capacity/throughput
cloudantnosqldb.capacity-
throughput.write
GET
/_api/v2/user/current/throughput
cloudantnosqldb.current-throughput.read
GET
/_api/v2/user/activity_tracker/events
cloudantnosqldb.activity-tracker-event-
types.read
POST
/_api/v2/user/activity_tracker/events
cloudantnosqldb.activity-tracker-event-
types.write
POST
/_api/v2/api_keys
cloudantnosqldb.sapi.apikeys
GET/POST
/_api/v2/user/config/cors/
cloudantnosqldb.sapi.usercors
 Important: 
When you use IAM roles other than 
Manager
, such as 
Reader
, 
Writer
, 
Monitor
, or 
Checkpointer
, you 
must
 use 
Use only
IAM
 to avoid supplying users with 
legacy credentials that include greater access permissions.
Cloudant
   
429GET/PUT
/_api/v2/user/plan
cloudantnosqldb.sapi.userplan
GET
/_api/v2/user/ccm_diagnostics
cloudantnosqldb.sapi.userccmdiagnostics
GET
/_api/v2/user/last_activity
cloudantnosqldb.sapi.lastactivity
GET
/_api/v2/support/tickets/$CASEID/files/$ATTACHMENTID
cloudantnosqldb.sapi.supportattachments
GET/POST
/_api/v2/support/tickets
cloudantnosqldb.sapi.supporttickets
GET/PUT/DELETE
/_api/v2/support/tickets/$CASEID
cloudantnosqldb.sapi.supporttickets
GET
/_api/v2/user
cloudantnosqldb.sapi.userinfo
GET
/_api/v2/usage/data_volume
 and 
/_api/v2/usage/$YEAR/$MONTH
cloudantnosqldb.sapi.usage-data-volume
GET/HEAD
/
cloudantnosqldb.account-meta-info.read
GET/HEAD
/_active_tasks
cloudantnosqldb.account-active-
tasks.read
GET/HEAD
/_replicator
cloudantnosqldb.replicator-database-
info.read
GET/HEAD
/_replicator/$DOCUMENT
cloudantnosqldb.replication.read
GET/HEAD
/_scheduler/jobs
cloudantnosqldb.replication-
scheduler.read
GET/HEAD
/_scheduler/docs
cloudantnosqldb.replication-
scheduler.read
POST
/_replicate
cloudantnosqldb.replication.write
PUT/DELETE
/_replicator
cloudantnosqldb.replicator-
database.create
PUT/DELETE
/_replicator/$DOCUMENT
cloudantnosqldb.replication.write
GET/HEAD
/_up
cloudantnosqldb.account-up.read
PUT
/$DATABASE/
cloudantnosqldb.database.create
DELETE
/$DATABASE
cloudantnosqldb.database.delete
POST
/$DATABASE/_design_docs/queries
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/_geo_info
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/_info/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET
/$DATABASE/_design/$DOCUMENT_ID/_search_disk_size/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET
/$DATABASE/_design/$DOCUMENT_ID/_search_info/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_index/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
Cloudant
   
430GET
/$DATABASE/_design_docs
cloudantnosqldb.any-document.read
GET
/$DATABASE/_design/$DOCUMENT_ID
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.any-document.read
PUT
/$DATABASE/_design/$DOCUMENT_ID
cloudantnosqldb.design-document.write
COPY
/$DATABASE/_design/$DOCUMENT_ID
cloudantnosqldb.design-document.write
DELETE
/$DATABASE/_design/$DOCUMENT_ID
cloudantnosqldb.design-document.write
PUT
/$DATABASE/_design/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.design-document.write
DELETE
/$DATABASE/_design/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.design-document.write
POST/DELETE
/$DATABASE/_index/$FURTHER_PATH_PARTS
cloudantnosqldb.design-document.write
GET/HEAD
/$DATABASE/_security
cloudantnosqldb.database-security.read
PUT
/$DATABASE/_security
cloudantnosqldb.database-security.write
GET/HEAD
/$DATABASE/_shards
cloudantnosqldb.database-shards.read
COPY
 (Depends
on write
document type.)
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.any-document.read
 +
cloudantnosqldb.design-document.write
either or both 
cloudantnosqldb.local-
document.write
 either or both
cloudantnosqldb.data-document.write
GET
/_membership
cloudantnosqldb.cluster-membership.read
POST
/$DATABASE/_ensure_full_commit
cloudantnosqldb.database-ensure-full-
commit.execute
PUT
/_users
cloudantnosqldb.users-database.create
GET/HEAD
/_users
cloudantnosqldb.users-database-
info.read
DELETE
/_users
cloudantnosqldb.users-database.delete
GET/HEAD
/_users/$DOCUMENT
cloudantnosqldb.users.read
GET/POST
/_users/_all_docs
cloudantnosqldb.users.read
GET/POST
/_users/_changes
cloudantnosqldb.users.read
POST
/_users/_missing_revs
cloudantnosqldb.users.read
POST
/_users/_revs_diff
cloudantnosqldb.users.read
POST
/_users/_bulk_get
cloudantnosqldb.users.read
PUT/DELETE
/_users/$DOCUMENT
cloudantnosqldb.users.write
POST
/_users/_bulk_docs
cloudantnosqldb.users.write
Cloudant
   
431POST
/_users/
cloudantnosqldb.users.write
GET/HEAD
/_uuids
cloudantnosqldb.cluster-uuids.execute
POST
/$DATABASE/
cloudantnosqldb.data-document.write
 or
cloudantnosqldb.design-document.write
or 
cloudantnosqldb.local-document.write
POST
/$DATABASE/_bulk_docs
cloudantnosqldb.data-document.write
either or both 
cloudantnosqldb.design-
document.write
 either or both
cloudantnosqldb.local-document.write
PUT
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.data-document.write
DELETE
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.data-document.write
PUT
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.data-document.write
DELETE
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.data-document.write
PUT/DELETE
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.local-document.write
COPY
 (Depends
on write
document type.)
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.any-document.read
 +
cloudantnosqldb.design-document.write
either or both 
cloudantnosqldb.local-
document.write
 either or both
cloudantnosqldb.data-document.write
GET/HEAD
/_iam_session
cloudantnosqldb.iam-session.read
POST
/_iam_session
cloudantnosqldb.iam-session.write
DELETE
/_iam_session
cloudantnosqldb.iam-session.delete
GET/HEAD
/_session
cloudantnosqldb.session.read
POST
/_session
cloudantnosqldb.session.write
DELETE
/_session
cloudantnosqldb.session.delete
GET/HEAD
/_all_dbs
cloudantnosqldb.account-all-dbs.read
POST
/_dbs_info
cloudantnosqldb.account-dbs-info.read
GET
/$DATABASE/
cloudantnosqldb.database-info.read
GET/POST
/$DATABASE/_all_docs
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_changes
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.any-document.read
POST
/$DATABASE/_bulk_get
cloudantnosqldb.any-document.read
Cloudant
   
432Table 2. Actions and mapping for the Manager role
GET/POST
/_search_analyze
cloudantnosqldb.account-search-
analyze.execute
POST
/$DATABASE/_all_docs/queries
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/_geo/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_search/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$VIEW/queries
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_explain/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_find/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.any-document.read
POST
/$DATABASE/_missing_revs
cloudantnosqldb.any-document.read
POST
/$DATABASE/_revs_diff
cloudantnosqldb.any-document.read
Method
Endpoint
Action name
GET
/_api/v2/user/activity_tracker/events
cloudantnosqldb.activity-tracker-event-
types.read
GET/HEAD
/_uuids
cloudantnosqldb.cluster-uuids.execute
POST
/$DATABASE/
cloudantnosqldb.data-document.write
 or
cloudantnosqldb.design-document.write
 or
cloudantnosqldb.local-document.write
POST
/$DATABASE/_bulk_docs
cloudantnosqldb.data-document.write
 either or
both 
cloudantnosqldb.design-document.write
either or both 
cloudantnosqldb.local-
document.write
PUT
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.data-document.write
DELETE
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.data-document.write
PUT
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.data-document.write
DELETE
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.data-document.write
PUT/DELETE
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.local-document.write
GET/HEAD
/_iam_session
cloudantnosqldb.iam-session.read
POST
/_iam_session
cloudantnosqldb.iam-session.write
DELETE
/_iam_session
cloudantnosqldb.iam-session.delete
GET/HEAD
/_session
cloudantnosqldb.session.read
Cloudant
   
433Table 2. Actions and mapping for the Writer role
POST
/_session
cloudantnosqldb.session.write
DELETE
/_session
cloudantnosqldb.session.delete
GET/HEAD
/_all_dbs
cloudantnosqldb.account-all-dbs.read
POST
/_dbs_info
cloudantnosqldb.account-dbs-info.read
GET
/$DATABASE/
cloudantnosqldb.database-info.read
GET/POST
/$DATABASE/_all_docs
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_changes
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.any-document.read
POST
/$DATABASE/_bulk_get
cloudantnosqldb.any-document.read
GET/POST
/_search_analyze
cloudantnosqldb.account-search-
analyze.execute
POST
/$DATABASE/_all_docs/queries
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/_geo/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_search/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$VIEW/queries
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_explain/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_find/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.any-document.read
POST
/$DATABASE/_missing_revs
cloudantnosqldb.any-document.read
POST
/$DATABASE/_revs_diff
cloudantnosqldb.any-document.read
GET/HEAD
/
cloudantnosqldb.account-meta-info.read
POST
/$DATABASE/_ensure_full_commit
cloudantnosqldb.database-ensure-full-
commit.execute
Method
Endpoint
Action name
GET
/_api/v2/user/activity_tracker/events
cloudantnosqldb.activity-tracker-event-
types.read
GET/HEAD
/_iam_session
cloudantnosqldb.iam-session.read
POST
/_iam_session
cloudantnosqldb.iam-session.write
Cloudant
   
434Table 2. Actions and mapping for the Reader role
DELETE
/_iam_session
cloudantnosqldb.iam-session.delete
GET/HEAD
/_session
cloudantnosqldb.session.read
POST
/_session
cloudantnosqldb.session.write
DELETE
/_session
cloudantnosqldb.session.delete
GET/HEAD
/_all_dbs
cloudantnosqldb.account-all-dbs.read
POST
/_dbs_info
cloudantnosqldb.account-dbs-info.read
GET
/$DATABASE/
cloudantnosqldb.database-info.read
GET/POST
/$DATABASE/_all_docs
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_changes
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/$DOCUMENT_ID/$ATTACHMENT
cloudantnosqldb.any-document.read
POST
/$DATABASE/_bulk_get
cloudantnosqldb.any-document.read
GET/POST
/_search_analyze
cloudantnosqldb.account-search-analyze.execute
POST
/$DATABASE/_all_docs/queries
cloudantnosqldb.any-document.read
GET/HEAD
/$DATABASE/_design/$DOCUMENT_ID/_geo/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_search/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$VIEW/queries
cloudantnosqldb.any-document.read
GET/POST
/$DATABASE/_design/$DOCUMENT_ID/_view/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_explain/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
POST
/$DATABASE/_find/$FURTHER_PATH_PARTS
cloudantnosqldb.any-document.read
GET
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.any-document.read
POST
/$DATABASE/_missing_revs
cloudantnosqldb.any-document.read
POST
/$DATABASE/_revs_diff
cloudantnosqldb.any-document.read
GET/HEAD
/
cloudantnosqldb.account-meta-info.read
Method
Endpoint
Action name
GET
/_api/v2/usage/data_volume
 and 
/_api/v2/usage/$YEAR/$MONTH
cloudantnosqldb.sapi.usage-data-volume
GET
/_api/v2/user/capacity/throughput
cloudantnosqldb.capacity-throughput.read
GET
/_api/v2/user/current/throughput
cloudantnosqldb.current-throughput.read
Cloudant
   
435Table 2. Actions and mapping for the Monitor role
GET/HEAD
/
cloudantnosqldb.account-meta-info.read
GET/HEAD
/_active_tasks
cloudantnosqldb.account-active-tasks.read
GET/HEAD
/_scheduler/jobs
cloudantnosqldb.replication-scheduler.read
GET/HEAD
/_scheduler/docs
cloudantnosqldb.replication-scheduler.read
GET/HEAD
/_up
cloudantnosqldb.account-up.read
GET/HEAD
/$DATABASE/_shards
cloudantnosqldb.database-shards.read
PUT/DELETE
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.local-document.write
POST
/_dbs_info
cloudantnosqldb.account-dbs-info.read
GET
/$DATABASE/
cloudantnosqldb.database-info.read
Table 2. Actions and mapping for the Checkpointer role
Method
Endpoint
Action name
PUT/DELETE
/$DATABASE/_local/$DOCUMENT_ID
cloudantnosqldb.local-document.write
Unavailable endpoints
The following endpoints are not available to requests authorized with IAM:
HTTP rewrite handlers - 
/db/_design/design-doc/_rewrite/path
.
While design documents can contain rewrite handlers, users cannot call them.
Update handlers - 
POST /db/_design/ddoc/_update/func
.
While design documents can contain update functions, users cannot call them.
Troubleshooting
If you can't use IAM to authenticate when you make requests to your IBM Cloudant service instance, verify your account as shown in the next
section.
Ensure that your account is IAM enabled
On the Overview portion of the IBM Cloudant Dashboard, "authentication method" is listed under deployment details. Your available authentication
methods are listed there.
Learning about IBM Cloudant architecture and workload isolation
Review the following sample architecture for IBM® Cloudant® for IBM Cloud®, and learn more about different isolation levels. After that, you can
choose the solution that best meets the requirements of the workloads that you want to run in the 
cloud.
IBM Cloudant isolation models and architecture
IBM Cloudant is a multi-tenant-capable database system with mechanisms in place to distribute any shared resources like CPU or I/O fairly among
the active tenants. IBM Cloudant implements isolation in the database layer itself, and not by relying 
on containers. Instances are isolated from each
other for access control, meaning that it is not possible to read or write data in one instance from another.
Workload isolation is an important consideration for many customers. To select the best IBM Cloudant plan choice for your workload isolation
requirements, see the following architectural information:
a
. 
Standard and Lite plans on Multi-Tenant Hardware, which offer excellent isolation.
Cloudant
   
436b
. 
Standard plan provisioned on a Dedicated Hardware plan instance, which offers improved isolation over Standard on Multi-Tenant Hardware.
Standard and Lite
Standard and Lite plans are provisioned onto large, shared IBM Cloudant database deployments where customers share compute and storage
resource. Standard and Lite plans apply provisioned throughput rate-limiting, along with other resource 
and access isolation mechanisms within the
database layer itself. Together, these provide strong security guarantees alongside robust resource separation within the shared environment.
Figure 1. Data isolation on IBM Cloudant Standard plan
Disk encryption is used to provide encryption at rest by using an IBM owned and managed encryption key. Customer data resides in different files on
disk.
Standard on Dedicated Hardware
A Dedicated Hardware instance offers improved storage and compute isolation for your most valuable data, including use of BYOK. After a Dedicated
Hardware instance is provisioned, you can provision many Standard plan instances onto this Dedicated 
Hardware instance to store your data. While
these Standard plan instances share the Dedicated Hardware's compute and storage, the instances do not share Dedicated Hardware's compute and
storage with other customers.
Figure 2. Data isolation on IBM Cloudant Dedicated Hardware plan
Disk encryption is used to provide encryption at rest. In the Dedicated Hardware plan, customers can use their own keys by using IBM Cloud® Key
Protect's BYOK to further secure their data.
Cloudant
   
437Dedicated Hardware instances provide IP allowlisting and private network utilization to secure network access.
Data and resource isolation between the Standard plan instances on a Dedicated Hardware instance is provided by using the same robust
mechanisms that are used within the multi-tenant deployment option.
Using service endpoints to privately connect to IBM Cloudant
To ensure that you enhance control and security over your data when you use IBM® Cloudant® for IBM Cloud®, you have the option of using private
routes to IBM Cloud® service endpoints. Private routes are not accessible or reachable over the internet. 
By using the IBM Cloud Private service
endpoints feature, you can protect your data from threats from the public network and logically extend your private network.
IBM Cloudant sends customer logs to LogDNA by using a private service endpoint.
Before you begin
You must first enable virtual routing and forwarding in your account, and then you can enable the use of IBM Cloud Private service endpoints. For
more information about setting up your account to support the private connectivity option, see 
Enabling VRF and service endpoints
.
Only IBM Cloudant users with the dedicated hardware plan can have a cloud service endpoint (CSE). All new dedicated hardware clusters have a CSE.
If you are an existing user, and you do not have a CSE, contact the 
IBM Cloud Support Center
.
Setting up service endpoints for IBM Cloudant
Cloud service endpoints are ready to use when an instance is deployed. Therefore, there is no set up.
You can verify connectivity to your private service endpoint by getting the Cloudant server information from the URL of the private endpoint.
Curl
curl https://
$ACCOUNT
-bluemix.private.cloudantnosqldb.appdomain.cloud
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ServerInformation;
Cloudant
 
service
 
=
 Cloudant.newInstance();
service.setServiceUrl(
"https://$ACCOUNT-bluemix.private.cloudantnosqldb.appdomain.cloud"
);
...
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
setServiceUrl
(
'https://$ACCOUNT-bluemix.private.cloudantnosqldb.appdomain.cloud'
);
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
service.set_service_url(
'https://$ACCOUNT-bluemix.private.cloudantnosqldb.appdomain.cloud'
)
Go
import
 (
  
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
 Tip: 
Multi-tenant users cannot use CSE.
Cloudant
   
438service, _ := cloudantv1.NewCloudantV1UsingExternalConfig(
  &cloudantv1.CloudantV1Options{},
)
service.SetServiceURL(
"https://$ACCOUNT-bluemix.private.cloudantnosqldb.appdomain.cloud"
)
if
 err != 
nil
 {
  
panic
(err)
}
If it succeeds, you are ready to go. Otherwise, you might want to check a few things:
Are your CSEs correctly enabled?
Can you reach the CSE endpoints from where you're running the command?
Do other CSE endpoints in the same account work correctly?
Do your firewall rules block access?
If none of these tasks fix the problem, you can talk to our 
IBM Cloud Support Center
 team.
Disabling public service endpoints for IBM Cloudant
The public service endpoint cannot be disabled however, if you use the dedicated hardware plan, you can deny access from the public network to
user traffic. To accomplish this task, make a request to update the firewall rules for your clusters 
to the 
IBM Cloud Support Center
.
Securing your connection
IBM® Cloudant® for IBM Cloud® is accessed through an HTTP API. This document describes the different parts that you use to connect to IBM
Cloudant:
Endpoints (Public and Private)
Service credentials
Authentication
Accessing the IBM Cloudant Dashboard
Programmatically accessing IBM Cloudant through 
curl
 or client libraries
Endpoints (Public and Private)
IBM Cloudant is accessed through HTTP API endpoints. The endpoints for an instance are shown in both the URL field of the Service Credentials that
are generated for the instance, and in 
Account
 > 
Settings
 
of the IBM Cloudant Dashboard.
Therefore, all IBM Cloudant HTTP endpoints must be accessed over TLS and prefaced by 
https://
.
Public Endpoints
The publicly facing external endpoint is shown in the following example:
https://$ACCOUNT.cloudant.com
All instances created after 1 January 2019 include an 
appdomain.cloud
 domain endpoint. The publicly facing external endpoint is shown in the
following example:
https://$ACCOUNT.cloudantnosqldb.appdomain.cloud
In this example, ACCOUNT is the service name of the service instance user in the URL. An example ACCOUNT is de810d0e-763f-46a6-ae88-
50823dc85581-bluemix, and resulting example public endpoint would be de810d0e-763f-46a6-ae88-50823dc85581-
bluemix.cloudantnosqldb.appdomain.cloud.
Private Endpoints
Private (internal) endpoints are added to all instances deployed on Dedicated Hardware plan environments. The IBM Cloud internal network
endpoint is shown in the following example:
 Tip: 
This option is not available to multi-tenant users.
Cloudant
   
439https://$ACCOUNT.private.cloudantnosqldb.appdomain.cloud
In this example, ACCOUNT is the service name of the service instance user in the URL. An example ACCOUNT is de810d0e-763f-46a6-ae88-
50823dc85581-bluemix, and resulting example private endpoint would be de810d0e-763f-46a6-ae88-50823dc85581-
bluemix.private.cloudantnosqldb.appdomain.cloud.
For more information on Private endpoints, see the 
Service Endpoints
 documentation.
For more information about how to block public network connectivity by using IP allowlisting, see 
Secure access control
.
Service credentials
To generate service credentials for IBM Cloudant by using the IBM Cloud Dashboard, see 
Creating an IBM Cloudant instance on IBM Cloud
. To
generate service credentials 
from the IBM Cloud CLI, see 
Creating credentials for your IBM Cloudant service
.
The following example shows service credentials for an IBM Cloudant instance:
{
  
"apikey"
:
 
"MxVp86XHkU82Wc97tdvDF8qM8B0Xdit2RqR1mGfVXPWz"
,
  
"host"
:
 
"76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"iam_apikey_description"
:
 
"Auto generated apikey during resource-key [...]"
,
  
"iam_apikey_name"
:
 
"auto-generated-apikey-050d21b5-5f[...]"
,
  
"iam_role_crn"
:
 
"crn:v1:bluemix:public:iam::::serviceRole:Manager"
,
  
"iam_serviceid_crn"
:
 
"crn:v1:staging:public:iam-identity::[...]"
,
  
"password"
:
 
"8fb6a16b48903e87b769e7f4968521e85c2394ed8f0e69b2769e56dcb27d2e76"
,
  
"port"
:
 
443
,
  
"url"
:
 
"https://<username>:<password>@76838001-b883-444d-90d0-46f89e942a15-bluemix.cloudant.com"
,
  
"username"
:
 
"apikey-v2-58B528DF5397465BB6673E1B79482A8C"
}
The service credentials include the following fields:
Table 1. Service credential fields
Field
Purpose
username
The username that is required for applications to access the service instance.
password
The legacy credentials password that is required for applications to access the service instance. This field
displays only if the 
Use both legacy credentials and IAM
 option is chosen.
host
The hostname that is used by applications to locate the service instance. This field displays only if the 
Use both
legacy credentials and IAM
 option is chosen.
port
The HTTPS port number for accessing the service instance on the host. It's 443 as only HTTPS access is allowed
by IBM Cloudant. This field displays only if the 
Use both legacy credentials and IAM
 option is chosen.
url
The HTTPS URL to access the IBM Cloudant instance. If the 
Use both legacy credentials and IAM
 option is
chosen, it also includes the embedded legacy username and password.
apikey
The IAM API key.
iam_apikey_description
Description of the IAM API key.
iam_apikey_name
ID of the IAM API key.
iam_role_crn
The IAM role that the IAM API key has.
iam_serviceid_crn
The CRN of the service ID.
Authentication
IBM Cloudant has two authentication methods available at provisioning time, either 
Use only IAM
 or 
Use both legacy credentials and IAM
.
Cloudant
   
440You can see the details about your legacy credentials in the service credentials only if the 
Use both legacy credentials and IAM
 authentication
method 
is chosen. The credentials display on the Service credentials tab for your instance. For more information, see the 
IAM guide
 and 
legacy
authentication
 document for details about using either style of 
authentication.
IBM Cloudant Dashboard
You can open the IBM Cloudant Dashboard for your instance by going to the Manage tab of the IBM Cloud Dashboard instance details page. You can
use either 
Launch
 or 
Launch Cloudant Dashboard
 to open the dashboard in 
a new browser tab. You can do the following tasks by using the IBM
Cloudant Dashboard:
Monitor your current consumption of the instance.
Perform create, read, update, and delete on IBM Cloudant databases, documents, and indexes.
Set up and view replication jobs.
View active tasks.
View and update account information like provisioned throughput capacity, announcements, CORS, and settings.
Programmatic access
Command line (curl)
You can leverage the curl command-line utility to access the IBM Cloudant HTTPS API.
For more information about IBM Cloudant legacy authentication, see the 
API & SDK reference
. In the API reference examples, you find details on
supplying a username and password to access the IBM Cloudant 
API with curl.
If you use IBM Cloud IAM authentication, you must first get an IBM Cloud IAM token by using an API key. Then, you pass the IAM token to the IBM
Cloudant instance to authenticate. For more information, see 
Passing an IBM Cloud IAM token to authenticate with a service's API
 tutorial.
Client libraries
IBM Cloudant has official client libraries for Java™, Node.js, Python, Swift, and Mobile. For more information, see the 
client libraries documentation
 to
access 
the libraries, and see examples for connecting to an IBM Cloudant instance from each.
Managing security and compliance with IBM Cloudant
IBM® Cloudant® for IBM Cloud® is integrated with the Security and Compliance Center to help you manage security and compliance for your
organization.
With the Security and Compliance Center, you can:
Monitor controls and goals that pertain to IBM Cloudant.
Define rules that standardize resource configuration for IBM Cloudant.
Monitoring security and compliance posture with IBM Cloudant
As a security or compliance focal, you can use the IBM Cloudant goals to help ensure that your organization is adhering to the external and internal
standards for your industry. By using the Security and Compliance Center to validate the resource 
configurations in your account against a 
 profile
,
you can identify potential issues as they arise.
To start monitoring your resources, check out 
Getting started with Security and Compliance Center
.
Available goals for IBM Cloudant
Check whether Cloudant is accessible only through HTTPS.
 Important: 
The IBM Cloudant team recommends you use IAM access controls for authentication whenever possible. If you're using IBM
Cloudant legacy authentication, you must use 
API keys
 
rather than account-level credentials for programmatic access and replication jobs.
 Note: 
You can't use an IAM API key directly to authenticate against IBM Cloudant.
 Note: 
IBM Cloudant goals are added to the IBM Cloud Control Library but can also be mapped to other profiles.
Cloudant
   
441Check whether Cloudant is accessible only through HTTPS.
Check whether Cloudant is enabled with encryption.
Check whether Cloudant is enabled with customer-managed encryption and Bring Your Own Key (BYOK).
Securing your data in IBM Cloudant
IBM Cloudant DBaaS data protection and security
Protecting application data for large-scale web and mobile apps can be complex, especially with distributed and NoSQL databases.
Just as it reduces the effort of maintaining your databases to keep them running and growing nonstop, IBM® Cloudant® for IBM Cloud® also ensures
that your data stays secure and protected.
Tier one physical platforms
The IBM Cloudant DBaaS is physically hosted on Tier-1 cloud infrastructure providers such as IBM Cloud® and Amazon. Therefore, your data is
protected by the network and physical security measures that are employed by those providers, including 
(but not limited to):
Certifications - Compliance with SSAE16, SOC2 Type 1, ISAE 3402, ISO 27001, CSA, and other standards.
Access and identity management.
General physical security of data centers and network operations center monitoring.
Server hardening.
IBM Cloudant gives you the flexibility to choose or switch among the different providers as your SLA and cost requirements change.
Secure access control
IBM Cloudant has a multitude of built-in security features, for you to control access to data:
Feature
Description
Authentication
IBM Cloudant is accessed by using an HTTPS API. Where the API endpoint requires it, the user is authenticated for every
HTTPS request IBM Cloudant receives. IBM Cloudant supports both legacy and IAM access controls. For more information,
see the 
IAM guide
 or the legacy 
Authentication document
.
Authorization
IBM Cloudant supports both legacy and IAM access controls. The IBM Cloudant team recommends that you use IAM access
controls for authentication whenever possible. If you're using IBM Cloudant legacy authentication, it is recommended that
you use 
API keys
 rather than account-level credentials for programmatic access and replication jobs. For more information,
see the 
IAM guide
 
or the legacy 
Authentication document
 and the legacy 
Authorization document
.
At-rest
encryption
All data that is stored in an IBM Cloudant instance is encrypted at rest by using LUKS1 with 256-bit Advanced Encryption
Standard (AES-256). By default, IBM Cloudant manages the encryption keys for all environments. If you require bring-your-
own-key 
(BYOK) encryption for encryption-at-rest, you enable it by using your encryption key that is stored in an IBM Cloud
Key Protect instance. IBM Cloudant supports the BYOK feature for new IBM Cloudant Dedicated Hardware plan instances
that 
are deployed in all regions. For more information, see the 
Creating an IBM Cloudant Dedicated Hardware plan instance
tutorial for details on how to choose BYOK at provisioning time.
In-flight
encryption
All access to IBM Cloudant is encrypted by using HTTPS.
Client-side
encryption
Customers can use client-side encryption to ensure that the data protection is controlled by the data owner and the data is
never visible to the service provider.
TLS
IBM Cloudant requires the use of TLS 1.2+. IBM Cloudant strongly recommends that you do not pin certificates in your
application. Certificates renew regularly, at least annually, and intermediate and root certificates could change when 
they do.
IBM Cloudant does not send out notifications before certificate renewals. We recommend that you keep your certificate
truststore up to date with the latest root certificates. IBM Cloudant acquires its certificates from DigiCert. 
You can find their
root certificates on the 
DigiCert Trusted Root Authority Certificates
 page. IBM Cloudant sends a notification 
if we move to a
different certificate authority.
 Tip: 
More details about the certifications are available in the 
Compliance information
.
Cloudant
   
442Table 1. IBM Cloudant security features
Endpoints
All IBM Cloudant instances are provided with external endpoints that are publicly accessible. Dedicated Hardware
environments created after 1 January 2019 outside of the EU-managed cloud also add internal endpoints for all Standard
plan 
instances deployed on them. Using internal endpoints allows customers to connect to an IBM Cloudant instance
through the internal IBM Cloud® network to avoid upstream application traffic from going over the public network and
incurring 
bandwidth charges. For more information, see 
Service Endpoint documentation
 for more details on enabling
Service Endpoints for your 
IBM Cloud® account.
IP allowlisting
IBM Cloudant customers, who have a dedicated IBM Cloudant environment, can allowlist IP addresses to restrict access to
only specified servers and users. IP allowlisting isn't available for any IBM Cloud Public Lite or Standard plans that 
are
deployed on multi-tenant environments. Open a support ticket to request IP allowlists for a specified set of IP or IP ranges. IP
allowlists apply to both the IBM Cloudant API and Dashboard, so be mindful to include any administrator 
IP that needs to
access the IBM Cloudant Dashboard directly.
CORS
Enable CORS support for specific domains by using the IBM Cloudant Dashboard or API. For more information, see the 
CORS
documentation
.
Protection against data loss or corruption
IBM Cloudant has a number of features to help you maintain data quality and availability:
Table 2. IBM Cloudant data quality and availability features
Feature
Description
Redundant
and durable
data storage
By default, IBM Cloudant saves to disk three copies of every document to three different nodes in a cluster. Saving the copies
ensures that a working failover copy of your data is always available, regardless of failures.
Data
Replication
and export
You can replicate your databases continuously between clusters in different data centers or Apache CouchDB. Another
option is to export data from IBM Cloudant (in JSON format) to other locations or sources (such as your own data center) 
for
added data redundancy.
Deleting your data in IBM Cloudant
You can delete individual documents in the IBM Cloudant Dashboard or by using an API. Documents are not technically deleted but instead are
compacted.
For more information, see 
Deletion of data
.
To delete a document, follow these steps:
a
. 
Go to IBM Cloudant Dashboard.
b
. 
On the Databases page, click the database that contains the documents that you want to delete.
c
. 
Click the checkbox next to the documents that you want to delete.
d
. 
Click 
Delete
.
The document is selected for compaction.
For more information, see 
Delete a document
 in the API Reference documentation.
Deleting IBM Cloudant instances
You can delete a database instance in the IBM Cloudant Dashboard or by using an API.
Once an instance is deleted, all data within the database, as well as the account-level information, such as authentication data, is deleted
automatically after the 7-day grace period ends. IBM Cloudant doesn’t hold any contact details for 
the instances that are created by using the
platform. If you have support tickets with IBM Cloudant where you shared information, such as email addresses, that information isn’t removed by
this process.
To delete a database, follow these steps:
a
. 
Go to IBM Cloudant Dashboard.
b
. 
On the Databases page, click 
Delete
 next to the database you want to delete.
Cloudant
   
443c
. 
Type in the name of the database you want to delete.
d
. 
Click 
Delete Database
.
The database is removed from the list of databases.
For more information, see 
Delete a database
 in the API Reference documentation.
The IBM Cloudant data retention policy describes how long your data is stored after you delete the service. The data retention policy is included in
the IBM Cloudant service description, which you can find in the IBM Cloud Terms and Notices.
Restoring deleted data for IBM Cloudant
If you delete your account, you have a 7-day grace period during which you can cancel the request to delete it.
Auditing events
As a security officer, auditor, or manager, you can use the IBM Cloud® Activity Tracker service to track how users and applications interact with the
IBM® Cloudant® for IBM Cloud® service in IBM Cloud®.
IBM Cloud Activity Tracker records user-initiated activities that change the state of a service in IBM Cloud. You can use this service to investigate
abnormal activity and critical actions and to comply with regulatory audit requirements. You 
can also be alerted about actions as they happen. The
events that are collected comply with the Cloud Auditing Data Federation (CADF) standard. For more information, see the 
Getting started tutorial for
IBM Cloud Activity Tracker
.
Types of events
IBM Cloudant forwards two types of events to IBM Cloud Activity Tracker:
Management Events
 are administrative events that impact the state of an IBM Cloudant instance, such as the following management events:
Creating or deleting a database.
Updating security settings.
Creating a replication job.
Creating an index.
Data Events
 are all the other events that are involved with interacting with IBM Cloudant, such as the following events:
Reading or writing JSON documents.
Reading a list of databases.
Viewing monitoring endpoints.
Authenticating against the service.
Configuring data events for an IBM Cloudant instance
The following instructions demonstrate how to configure data events for an IBM Cloudant instance.
Configuring data events through the IBM Cloud UI
You can change what types of events are sent to IBM Cloud Activity Tracker in the IBM Cloud Dashboard by following these steps:
a
. 
Go to the Resource list, and select an IBM Cloudant instance.
The Manage page opens.
 Important: 
A database deletion cannot be undone.
 Important: 
A database deletion cannot be undone.
 Note: 
By default, only management events are automatically collected and sent to the IBM Cloud Activity Tracker service.
 Important: 
You must configure each IBM Cloudant instance to collect and send data events to the IBM Cloud Activity Tracker service.
Cloudant
   
444b
. 
Click 
Overview
. The Deployment Details pane opens.
c
. 
Find 
Activity Tracker event types
 in the list.
d
. 
Select the appropriate type, either 
Management
 or 
Management & Data
, from the drop-down menu.
e
. 
Click 
Save
.
Configuring data events by using the IBM Cloudant API
You can use the IBM Cloudant API to manage the configuration of Activity Tracker events.
Check what event types are configured for an IBM Cloudant instance
The 
/_api/v2/user/activity_tracker/events
 endpoint returns a 
types
 field in the response that includes an array of event types that are being
sent to IBM Cloud Activity Tracker for the IBM Cloudant instance.
See the following example request to retrieve information about configured event types by using HTTP:
GET $SERVICE_URL/_api/v2/user/activity_tracker/events
See the following example request to retrieve information about event types:
Curl
curl -H 
"Authorization: Bearer 
$JWT
"
 -X GET 
"
$SERVICE_URL
/_api/v2/user/activity_tracker/events"
Java
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.ActivityTrackerEvents;
Cloudant
 
service
 
=
 Cloudant.newInstance();
ActivityTrackerEvents
 
response
 
=
    service.getActivityTrackerEvents().execute().getResult();
System.out.println(response)
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
getActivityTrackerEvents
().
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.get_activity_tracker_events().get_result()
print
(response)
 Important: 
The API to view and change the event types requires IBM Identity and Access Management (IAM) authentication. The use of IBM
Cloudant legacy authentication isn't supported for this API endpoint. See 
Managing access
 
for details on using IAM authentication for IBM
Cloudant.
 Note: 
Before you run a 
curl
 request, run the following command from the command line to acquire a JWT token: 
ibmcloud iam oauth-
tokens | awk '{print $4}'
Cloudant
   
445Go
getActivityTrackerEventsOptions := service.NewGetActivityTrackerEventsOptions()
activityTrackerEvents, response, err := service.GetActivityTrackerEvents(getActivityTrackerEventsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(activityTrackerEvents, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
When you check what events are enabled, you get one of the following responses.
Response when both management and data event types are sent:
{
"types"
:
 
[
"management"
,
 
"data"
]
}
Response when only management events are sent:
{
"types"
:
 
[
"management"
]
}
Configure data events for an IBM Cloudant instance
You can configure data events by sending a 
POST
 to the 
/_api/v2/user/activity_tracker/events
 endpoint and passing a JSON object with a
types
 field.
See the following example request to configure event types by using HTTP:
POST $SERVICE_URL/_api/v2/user/activity_tracker/events
See the following example request to configure event types:
Curl
curl -H 
"Authorization: Bearer 
$JWT
"
 -X POST 
"
$SERVICE_URL
/_api/v2/user/activity_tracker/events"
 --data 
'{"types":
 
["management", "data"]}'
Java
import
 java.util.Arrays;
import
 com.ibm.cloud.cloudant.v1.Cloudant;
import
 com.ibm.cloud.cloudant.v1.model.Ok;
import
 com.ibm.cloud.cloudant.v1.model.PostActivityTrackerEventsOptions;
Cloudant
 
service
 
=
 Cloudant.newInstance();
PostActivityTrackerEventsOptions
 
options
 
=
    
new
 
PostActivityTrackerEventsOptions
.Builder()
        .types(Arrays.asList(
"management"
, 
"data"
))
        .build();
Ok
 
response
 
=
Cloudant
   
446    service.postActivityTrackerEvents(options).execute().getResult();
System.out.println(response);
Node
const
 { 
Cloudant
V1 } = 
require
(
'@ibm-cloud/cloudant'
);
const
 service = 
Cloudant
V1.
newInstance
({});
service.
postActivityTrackerEvents
({
  
types
: [
'management'
, 
'data'
],
}).
then
(
response
 =>
 {
  
console
.
log
(response.
result
);
});
Python
from
 ibmcloudant.cloudant_v1 
import
 CloudantV1
service = CloudantV1.new_instance()
response = service.post_activity_tracker_events(
  types=[
'management'
, 
'data'
]
).get_result()
print
(response)
Go
postActivityTrackerEventsOptions := service.NewPostActivityTrackerEventsOptions(
  []
string
{
"management"
, 
"data"
},
)
activityTrackerEvents, response, err := service.PostActivityTrackerEvents(postActivityTrackerEventsOptions)
if
 err != 
nil
 {
  
panic
(err)
}
b, _ := json.MarshalIndent(activityTrackerEvents, 
""
, 
"  "
)
fmt.Println(
string
(b))
The previous Go example requires the following import block:
Go
import
 (
   
"encoding/json"
   
"fmt"
   
"github.com/IBM/cloudant-go-sdk/cloudantv1"
)
All Go examples require the 
service
 object to be initialized. For more information, see the API documentation's 
Authentication section
 
for
examples.
The following example response shows that the update was accepted:
{
  
"ok"
:
true
}
If the 
types
 field includes invalid event types, then a response similar to the following one is returned:
{
  
"code"
:
400
,
  
"error"
:
"Unknown event types: <unrecognized events>"
}
Cloudant
   
447If the 
types
 field is missing, then a similar response to the following one is returned:
{
  
"code"
:
400
,
  
"error"
:
"Missing required events: \"management\""
}
List of events
Management events
Action
Description
cloudantnosqldb.account-status.configure
Set the status of an instance.
cloudantnosqldb.account-status.read
Get the status of an instance.
cloudantnosqldb.activity-tracker-event-
types.read
Get the configured event types of an instance.
cloudantnosqldb.activity-tracker-event-
types.write
Configure the event types for an instance.
cloudantnosqldb.capacity-throughput.read
Get the current provisioned throughput capacity settings for an instance.
cloudantnosqldb.capacity-throughput.write
Set the provisioned throughput capacity settings for an instance.
cloudantnosqldb.csp.capture
Indicates a Content Security Policy failure when you access the Cloudant Dashboard.
cloudantnosqldb.database.create
Create a database.
cloudantnosqldb.database.delete
Delete a database.
cloudantnosqldb.ibm-cloud-account-
status.configure
Set the status of an instance.
cloudantnosqldb.ibm-cloud-account-
status.read
Get the status of an instance.
cloudantnosqldb.legacy-credentials.revoke
Revoke all legacy credentials and make IAM the only authentication method of an
instance.
cloudantnosqldb.legacy-root-
credential.revoke
Revoke the url style credential for a Cloudant instance.
cloudantnosqldb.replicator-
database.create
Create 
_replicator
 database.
cloudantnosqldb.replicator-
database.delete
Delete 
_replicator
 database.
cloudantnosqldb.users-database.create
Create 
_users
 database.
cloudantnosqldb.users-database.delete
Delete 
_users
 database.
cloudantnosqldb.database-security.read
Read a security document.
 Note: 
It can take up to 5 minutes for the change to be reflected in the events seen in IBM Cloud Activity Tracker.
Cloudant
   
448Table 1. Management actions
cloudantnosqldb.database-security.write
A create, update, or delete of a security document.
cloudantnosqldb.design-document.write
A create, update, or delete of a 
_design
 document.
cloudantnosqldb.replication.read
Read a replication document.
cloudantnosqldb.replication.write
A create, update, or delete of a replication document.
cloudantnosqldb.sapi.apikeys
Create a legacy Cloudant API key for an instance.
cloudantnosqldb.sapi.db-security
Read or write a database's security document.
cloudantnosqldb.sapi.usercors
Set and get the CORS settings for an instance.
cloudantnosqldb.sapi.userplan
Get or set plan and plan settings of an instance.
cloudantnosqldb.users.write
Create, update, or delete a 
_users
 document.
cloudantnosqldb.volumes.update
A change in state of the IBM® Key Protect for IBM Cloud® key protecting dedicated
hardware environment.
Data events
Action
Description
cloudantnosqldb.any-document.read
Read a JSON document.
cloudantnosqldb.account-all-dbs.read
Read a list of all databases.
cloudantnosqldb.account-dbs-info.read
Read metadata about a database.
cloudantnosqldb.account-search-analyze.execute
Read search index statistics and size.
cloudantnosqldb.account-uuids.read
Read 
_uuids
 endpoint.
cloudantnosqldb.account-active-tasks.read
Read 
_active_tasks
.
cloudantnosqldb.current-throughput.read
Get the current consumption of the provisioned throughput capacity for an
instance.
cloudantnosqldb.database-ensure-full-
commit.execute
Post to 
_ensure_full_commit
 endpoint.
cloudantnosqldb.database-info.read
Read database metadata.
cloudantnosqldb.data-document.write
Write a JSON document.
cloudantnosqldb.iam-session.read
Read IAM session.
cloudantnosqldb.iam-session.write
Write IAM session.
cloudantnosqldb.iam-session.delete
Delete IAM session.
cloudantnosqldb.ibmid-login.authenticate
Complete IAM authentication on the Cloudant Dashboard.
Cloudant
   
449Table 2. Data actions
cloudantnosqldb.ibmid-login.receive
Part of the Cloudant Dashboard login with IAM authentication.
cloudantnosqldb.ibmid-login.start
Initiate Cloudant Dashboard login with IAM authentication.
cloudantnosqldb.local-document.write
Write a 
_local
 document.
cloudantnosqldb.replicator-database-info.read
Read 
_replicator
 database information.
cloudantnosqldb,replicator-design-document.write
Write a 
_design
 document to the 
_replicator
 database.
cloudantnosqldb.replicator-local-document.write
Write a 
_local
 document to the 
_replicator
 database.
cloudantnosqldb.sapi.lastactivity
Get the last active time of an instance. Used internally by the IBM Cloud platform.
cloudantnosqldb.sapi.supportattachments
Attach file to support ticket.
cloudantnosqldb.sapi.supporttickets
Create, read, and delete support tickets.
cloudantnosqldb.sapi.usage-data-volume
Get the data usage of an instance.
cloudantnosqldb.sapi.userccmdiagnostics
Get history of throughput consumption and 429 requests for the past 5 seconds.
cloudantnosqldb.sapi.userinfo
Get metadata of an instance.
cloudantnosqldb.session.delete
Delete IBM Cloudant legacy auth session.
cloudantnosqldb.session.read
Read IBM Cloudant legacy auth session.
cloudantnosqldb.session.write
Write IBM Cloudant legacy auth session.
cloudantnosqldb.users.read
Read 
_users
 database documents.
cloudantnosqldb.users-database-info.read
Read 
_users
 database information.
cloudantnosqldb.users-design-document.write
Write a 
_design
 document.
cloudantnosqldb.users-local-document.write
Write a 
_local
 document to the 
_users
 database.
Viewing events
Events are available in the Chennai, Dallas, Frankfurt, London, Osaka, São Paulo, Sydney, Tokyo, Toronto, and Washington DC locations. For more
information, see 
IBM Cloud services locations
.
Management events that are generated by an instance of the IBM Cloudant service are automatically collected and forwarded to the IBM Cloud
Activity Tracker service instance that is available in the same location.
You must enable data events for the IBM Cloudant instance to be able to view them through the IBM Cloud Activity Tracker instance that is available
in the same location as your IBM Cloudant instance.
IBM Cloud Activity Tracker can have only one instance per location. To view events, you must access the web user interface of the IBM Cloud Activity
Tracker service in the same location where your service instance is available. For more information, 
see how to 
start the web UI through the IBM
Cloud UI
.
Cloudant
   
450Understanding your responsibilities when you use IBM Cloudant
Learn about the management responsibilities, and terms and conditions, that you own when you use IBM® Cloudant® for IBM Cloud®. For a high-level
view of the service types in IBM Cloud®, and the breakdown of responsibilities between the customer 
and IBM® for each type, see 
Shared
responsibilities for using IBM Cloud offerings
.
Review the following sections to understand the specific responsibilities between you and IBM when you use IBM Cloudant. For the overall terms of
use, see 
IBM Cloud Terms and Notices
.
Incident and operations management
Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and
full state backup and recovery.
Table 1. Responsibilities for incident and operations
Task
IBM Responsibilities
Your Responsibilities
HA/DR
(multi-
zone
region)
IBM Cloudant stores all documents in triplicate on
separate servers that are spread across three
separate availability zones by default.
HA/DR
(single-
zone
region)
IBM Cloudant stores all documents in triplicate on
three separate physical servers within the
availability zone by default.
Back up
and
restore
Customer is responsible for backup and restore of data to roll back to a
previous state in the database. See 
IBM Cloudant backup and recovery
documentation for 
recommended tooling.
Change management
Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.
Table 2. Responsibilities for change management
Task
IBM Responsibilities
Your Responsibilities
Scaling
IBM scales infrastructure to meet capacity selected by the
customer.
Customer chooses the provisioned throughput capacity for their
IBM Cloudant instances.
Upgrades
IBM handles all upgrades and patches of the IBM Cloudant
service for the customer.
Security and regulation compliance
Security and regulation compliance includes tasks such as security controls implementation and compliance certification.
Task
IBM Responsibilities
Your Responsibilities
At-rest
encryption
By default, IBM
encrypts all disks by
using IBM Cloudant-
managed encryption
keys.
If the customer wants bring-your-own-key (BYOK) encryption, then the customer is required to use
Key Protect to store the customer-managed encryption key. The customer must select an appropriate
key management service instance, and select 
a disk encryption key option during provisioning of an
IBM Cloudant Dedicated Hardware plan instance.
Cloudant
   
451Table 3. Responsibilities for security and regulation compliance
Make data
unreadable
to IBM
Cloudant
Operators
None, IBM does not
render data
unreadable to IBM
Cloudant Operators.
If you intend to store sensitive information in an IBM Cloudant database, you must use client-side
encryption to render data unreadable to IBM Cloudant operators. For example, for PCI DSS
compliance, you must encrypt the Primary Account 
Number (PAN) before sending a document that
contains it to the database.
Disaster recovery
Disaster recovery includes the following tasks:
Provide dependencies on disaster recovery sites.
Provision disaster recovery environments.
Back up data and configuration.
Replicate data and configuration to the disaster recovery environment.
Fail over disaster events.
Table 4. Responsibilities for disaster recovery
Task
IBM
Responsibilities
Your Responsibilities
HA/DR
(cross-
region)
Customer is responsible for creating more IBM Cloudant instances in separate regions and configuring
replications to achieve the cross-region HA/DR architecture they want. See 
Configuring IBM Cloudant for
cross-region disaster recovery
 
for more details.
Cloudant
   
452Observability
IBM Cloud Log Analysis integration
IBM® Cloudant® for IBM Cloud® is integrated with 
IBM Cloud® Log Analysis
, so you can view database logs.
Currently, IBM Cloud Log Analysis integration is available for IBM Cloudant deployments according to the following table:
Table 1. IBM Cloud Log Analysis regions
Deployment Region
IBM Cloud Log Analysis Region
Chennai
Chennai
Dallas
Dallas
Frankfurt
Frankfurt
London
London
Osaka
Tokyo
São Paulo
São Paulo
Sydney
Sydney
Tokyo
Tokyo
Toronto
Toronto
Washington DC
Washington DC
Provisioning IBM Cloud Log Analysis
Log information from your databases is automatically forwarded to IBM Cloud Log Analysis. In order to access it, you must 
provision IBM Cloud Log
Analysis
 
in your IBM Cloud account and 
configure the service
 to receive IBM Cloud service logs.
IBM Cloud Log Analysis has a Lite plan that is free to use, but it offers only streaming events. To take advantage of the tagging, export, retention, and
other features, you need to use one of the 
paid plans
.
HIPAA
IBM Cloud Log Analysis does not currently offer a HIPAA-compliant plan for the service.
Using IBM Cloud Log Analysis
Once logs are being live-streamed, each log can be expanded to a detailed view by clicking the arrow by the timestamp.
The expanded view has some handy, color-coded fields to help you parse your logs.
Line Identifiers
Description
 Tip: 
This setting enables logs from 
all
 IBM Cloud services on your account with IBM Cloud Log Analysis integration sending logs to your IBM
Cloud Log Analysis service. For more information, see the list of 
integrated services
.
 Important: 
Use caution when you configure the platform service logs, since this setting can impact other services that require HIPAA
compliance.
Cloudant
   
453Table 2. Line identifiers
Source
The region the logs are being sent from.
App
The CRN of your database deployment that is sending the logs.
Table 3. Log lines
Log Lines
Description
accountName
The IBM Cloudant account identifier that you can use when you contact support about your environment.
httpMethod
Request method, for example, 
GET
, 
PUT
, to indicate the action to be performed for a specific resource.
httpRequest
The URL path for the HTTP request.
bytesRead
The size of the response body.
clientIp
The IP address of the originating request.
clientPort
The port address for the originating request.
statusCode
The HTTP status code returned from IBM Cloudant. For more information, see 
HTTP status codes
.
terminationState
Session termination indicator for TCP and HTTP logs. For more information, see 
Session state at disconnection
.
dbName
The IBM Cloudant database name targeted by the HTTP Request.
dbRequest
The database request endpoint.
userAgent
Software that is acting on behalf of the user, such as a browser or client library.
sslVersion
The version of Transport Layer Security that the request is using.
cipherSuite
The cipher suite used for the request.
requestClass
The class of metrics that the request is billed against. 
Unlimited
 is an unmetered event. For more information, see
Request classes
.
parsedQueryString
A parsed version that shows the breakdown of the parameters that are passed in the query string. If IBM Cloudant
cannot parse the 
rawQueryString
, this value is null.
rawQueryString
Full text of the query string as passed to the service.
logSourceCRN
The CRN of the IBM Cloudant instance emitting logs.
meta
A line reserved for additional information from IBM Cloudant.
timings
connect
 - The total time to accept TCP connection and execute handshakes for SSL protocol. This time happens only
once during the connection's lifetime, so subsequent requests that are sent over the same connection show 
0
 
for this
value.
request
 - The total time to get the client request. It's the time that is elapsed between the first bytes received and the
moment the service receives the last byte of the request body.
transfer
- The data transmission time to transfer the full response from the service to the client.
response
- The total active time for the HTTP request, between the moment the service received the first byte of the
request header and the emission of the last byte of the response body.
 Note: 
The 
request
 and 
transfer
 timings are included in 
response
.
Cloudant
   
454IBM Cloud Log Analysis offers 
searching
 and 
filtering
 to help you navigate your logs. 
Export
 and 
archive
 are available so you can customize
retention (and cost) for your use case.
IBM Cloud Activity Tracker integration
Users of IBM® Cloudant® for IBM Cloud® can use IBM Cloud® Activity Tracker to access audit logs for the service. IBM Cloud Activity Tracker records
user-initiated activities that change the state of a service in IBM Cloud®. You can use this service 
to investigate abnormal activity and critical actions
and to comply with regulatory audit requirements. You can also be alerted about actions as they happen. The events that are collected comply with
the IBM Cloud Auditing Data Federation (CADF) 
standard. For more information, see 
Auditing events
.
IBM Cloud Monitoring integration
IBM Cloud® Monitoring is a third-party, cloud-native, and container-intelligent management system that you can include as part of your IBM Cloud®
architecture. Use it to gain operational visibility into the performance and health of your applications, 
services, and platforms. It offers administrators,
DevOps teams, and developers full-stack telemetry with advanced features to monitor and troubleshoot, define alerts, and design custom
dashboards.
Currently, IBM Cloud Monitoring integration is available for IBM Cloudant deployments according to the following table:
Table 1. IBM Cloud Monitoring regions
Deployment Region
IBM Cloud Monitoring Region
Chennai
Tokyo
Dallas
Dallas
Frankfurt
Frankfurt
London
London
Osaka
Osaka
São Paulo
São Paulo
Seoul
Tokyo
Sydney
Sydney
Tokyo
Tokyo
Toronto
Toronto
Washington DC
Washington DC
Platform metrics overview
You can configure only one instance of the IBM Cloud® Monitoring service per region to collect platform metrics.
To configure the Monitoring instance, you must turn on the 
platform metrics
 configuration setting.
If a Monitoring instance in a region is already enabled to collect platform metrics, metrics from enabled-monitoring services are collected
automatically and available for monitoring through this instance. For more information about enabled-monitoring 
services, see 
IBM Cloud®
services
.
Enabling platform metrics from the IBM Cloud Dashboard
 Important: 
To monitor platform metrics, check that the Monitoring instance is provisioned in the same region where the IBM Cloud instance
is provisioned.
Cloudant
   
455Complete the following steps to configure platform metrics:
a
. 
Log in to IBM Cloud.
The IBM Cloud Dashboard opens.
b
. 
Click 
View all
 in the Resource summary section of the dashboard.
c
. 
In the 
Services
 section, click the IBM Cloud instance that you plan to monitor.
The IBM Cloud UI 
Manage
 page opens.
d
. 
Click 
Actions
 > 
Add monitoring
 to configure 
platform metrics
 in the region of your IBM Cloud instance.
Figure 1. Monitoring menu
e
. 
Provision an instance of the IBM Cloud Monitoring service.
After you provision the Monitoring instance, the 
Observability
 page opens. To continue working with IBM Cloud, go back to the IBM Cloud UI.
Viewing metrics
You can use different options to launch the IBM Cloud Monitoring web UI and monitor metrics that are described in the following section.
Launching IBM Cloud Monitoring web UI from the IBM Cloudant Dashboard
Complete the following steps to launch the IBM Cloud Monitoring web UI from the IBM Cloud Dashboard:
a
. 
Log in to IBM Cloud.
The IBM Cloud Dashboard opens.
b
. 
Click 
View all
 in the Resource summary section of the dashboard.
c
. 
In the 
Services
 section, click the IBM Cloudant instance that you plan to monitor.
The IBM Cloudant 
Manage
 page opens.
d
. 
Click 
Actions
, and select 
Monitoring
.
 Note: 
If the menu choices include the 
Monitoring
 option, then your instance is already configured for platform metrics.
 Important: 
To monitor IBM Cloudant metrics, you must launch the IBM Cloud Monitoring web UI instance that is enabled for platform
metrics in the region where your IBM Cloud instance is available.
Cloudant
   
456Figure 2. Monitoring menu
A new tab opens in your browser and shows the 
Default
 dashboard that is named 
IBM Cloudant
 within the context of your IBM Cloudant
instance.
Launching IBM Cloud Monitoring web UI from the Observability page
Complete the following steps to launch the IBM Cloud Monitoring web UI from the 
Observability
 page:
a
. 
Launch the IBM Cloud Monitoring web UI
.
b
. 
Click 
DASHBOARDS
.
c
. 
In the 
Default Dashboards
 section, expand 
IBM
.
d
. 
Choose the IBM Cloudant Dashboard from the list.
To access your deployment's IBM Cloud Monitoring Dashboard from IBM Cloud Monitoring, it's in the sidebar, under IBM.
Figure 3. IBM Cloudant Dashboard
Next, change the scope or make a copy of the 
Default
 dashboard to monitor an IBM Cloudant instance.
IBM Cloudant metrics dictionary
HTTP request count
The number of HTTP requests made against an IBM Cloudant instance:
Table 2. HTTP request count metric metadata
Metadata
Description
Metric Name
ibm_cloudant_http_requests_total
Metric Type
counter
Value Type
none
Segment By
Service instance, Service instance name
Cloudant
   
457Rate-limited operations
The number of operations that were rate-limited:
Table 3. Rate-limited operations metric metadata
Metadata
Description
Metric Name
ibm_cloudant_rate_limited_operations
Metric Type
counter
Value Type
none
Segment By
Service instance, Service instance name, Cloudant operation type
Attributes for segmentation
Global Attributes
The following attributes are available for segmenting all the metrics that are listed previously:
Table 4. Global attributes
Attribute
Name
Description
Cloud Type
ibm_ctype
The cloud type is a value of public, dedicated, or local.
Location
ibm_location
The location of the monitored resource, which can be a region, data center, or global.
Resource
ibm_resource
The resource that is measured by the service, typically an identifying name, or GUID.
Scope
ibm_scope
The scope is the account, organization, or space GUID associated with this metric.
Service name
ibm_service_name
Name of the service that generates this metric.
More Attributes
The following attributes are available for segmenting one or more attributes as described in the previous reference. See the individual metrics for
segmentation options in the following table:
Table 5. More attributes
Attribute
Name
Description
Cloudant
operation
type
ibm_cloudant_operation_type
The Cloudant billable operation type.
Service
instance
ibm_service_instance
The service instance segment identifies the instance that the metric is associated with.
Service
instance
name
ibm_service_instance_name
The service instance name provides the user-provided name of the service instance,
which isn't necessarily a unique value that depends on the name that is provided by the
user.
Resource
group name
ibm_resource_group_name
The resource group name provides the user-provided name of the resource group where
the service instance was created.
Resource
group
ibm_resource_group_id
The unique ID of the resource group where the service instance was created.
Cloudant
   
458IBM Cloudant Dashboard's dictionary
The following table outlines the pre-defined dashboards that you can use to monitor IBM Cloudant metrics:
Table 6. Pre-defined dashboard
Dashboard name
Description
IBM Cloudant
The default dashboard that opens when you launch IBM Cloud Monitoring web UI from your service instance UI.
 Important: 
The 
Default
 dashboard cannot be changed.
Cloudant
   
459High availability and disaster recovery
Understanding business continuity and disaster recovery for IBM Cloudant
Disaster recovery involves a set of policies, tools, and procedures for returning a system, an application, or an entire data center to full operation after
a catastrophic interruption. It includes procedures for copying and storing an installed 
system's essential data in a secure location, and for recovering
that data to restore normalcy of operation.
Responsibilities
For more information about your responsibilities when you use IBM Cloudant, see 
Shared responsibilities for IBM Cloudant
.
Disaster recovery strategy
IBM Cloud has business continuity plans in place to provide for the recovery of services within hours if a disaster occurs. You are responsible for your
data backup and associated recovery of your content.
IBM Cloudant provides mechanisms to restore service functions. Business continuity plans are in place to achieve targeted recovery point objective
(RPO) and recovery time objective (RTO) for the service. The following table outlines the targets 
for IBM Cloudant.
Table 1. RPO and RTO for IBM Cloudant
Disaster recovery objective
Target Value
RPO
24 hours
RTO
< 24 hours
Locations
For more information about service availability within regions and data centers, see 
Service and infrastructure availability by location
.
Understanding high availability for IBM Cloudant
High availability (HA) is a core discipline in an IT infrastructure to keep your apps up and running, even after a partial or full site failure. The main
purpose of high availability is to eliminate potential points of failures in an IT infrastructure.
To provide HA within a data center, all data is stored in triplicate across three separate physical servers in a cluster. You can provision accounts in
multiple data centers, then use continuous data replication to provide HA across data centers. 
IBM® Cloudant® for IBM Cloud® data isn't
automatically backed up, but supported tools are provided to handle backups. Review the 
Disaster recovery and backup guide
 to explore 
all HA and
backup considerations to meet your application requirements.
Responsibilities
To find out more about responsibility ownership for using IBM Cloud® products between IBM and the customer, see 
Shared responsibilities for IBM
Cloud products
.
For more information about responsibilities when you use IBM Cloudant, see 
Shared responsibilities for IBM Cloudant
.
What level of availability do I need?
You can achieve high availability on different levels in your IT infrastructure and within different components of your cluster. The level of availability
that works for you depends on several factors, such as your business requirements, the 
service level agreements (SLAs) that you have with your
customers, and the resources that you want to expend.
What level of availability does IBM Cloud offer?
The level of availability that you set up for your cluster impacts your coverage on the IBM Cloud high availability service level agreement terms.
Service level objectives (SLOs) describe the design points that the IBM Cloud services are engineered to meet. IBM Cloudant is designed to achieve
the following availability target.
Cloudant
   
460Table 1. SLA for IBM Cloudant
Availability target
Target Value
Availability %
99.99%
Refer to 
Cloud Services terms
 for commitments and credits that are issued for failure to meet any committed SLAs. For more information, 
see the
IBM Cloudant Service descriptions
.
Locations
For more information about service availability within regions and data centers, see 
Service and infrastructure availability by location
.
Cloudant
   
461Best practices for IBM Cloudant
Data modeling
The Data modeling document is the first best practice document in the series. It shows you the following best practices:
What you need to know about your APIs.
How to model your data.
What size documents you must use.
What to avoid.
How to configure your databases.
For more information, see 
Indexing and querying
 or 
IBM Cloudant in practice
.
The content in this document was originally written by Stefan Kruger as a 
Best and worst practice
 blog post on 21 November 2019.
Understand the API that you are targeting
You can use 
Java™
, 
Python
, 
Go
, or 
Node.js
 or some other use-case-specific language or platform. One of these languages most likely comes with
convenient client-side libraries that integrate IBM Cloudant access nicely, following the conventions that you expect for your tools. These languages
are great for programmer efficiency, but they also hide the API from view.
This abstraction is what you want, the whole reason for using a client library is to save yourself repeated, tedious boiler-plating. However, you must
understand the underlying API is vital when you troubleshoot and report problems. When you 
report a suspected problem to IBM Cloudant, it helps
us help you if you can provide a way for us to reproduce the problem.
This request does not mean cutting and pasting a hefty chunk of your application’s Java™ source verbatim into a support ticket, as we’re probably not
able to build it. Also, your client-side code introduces uncertainties as to where the problem 
might be, your side or our side?
Instead, IBM Cloudant’s support teams usually requests the set of API calls, ideally as a set of 
curl
 commands that they can run, that demonstrates
the issue. Adopting this approach 
to troubleshooting as a rule also makes it easier for you to pinpoint where issues are failing. If your code is
behaving unexpectedly, try to reproduce the problem by using only direct access to the API.
If you can’t, the problem isn’t with the IBM Cloudant service itself.
If you’re investigating a performance issue, do consult the logs that are provided by IBM Cloud®. If the logs show that your requests are handled
quickly by IBM Cloudant, but your application is slow, the root of that problem lies with your 
client-side application code. See the rule about 
logging
and monitoring
.
If you suspect that a problem lies with an officially supported client library, then try to construct a small, self-contained code example that
demonstrates the issue. In this self-contained code example, use as few other dependencies as possible. 
If you’re using Java™, it is helpful to us if
you can use a minimal 
test harness
 to highlight library issues.
Occasionally, IBM Cloudant receives support tickets that state that “IBM Cloudant is broken because my application is slow” without much in terms
of supporting evidence. Nearly always this case can be traced back to issues in the application 
code on the client side, or misconceptions about how
IBM Cloudant works.
Not always, but nearly always.
By understanding the API better, you also gain experience in how IBM Cloudant behaves, especially in terms of performance. If you’re using a client
library, you must aim to at least know how to find out which HTTP requests are generated by a 
specific function call. For more information, see the
following websites:
IBM Cloudant 
API docs
Logging 
integration
Blog post on 
logging
Documents must group data that mostly changes together
When you start to model your data, sooner or later, you run into the issue of how your documents might be structured. Now you know that IBM
Cloudant doesn’t enforce any normalization and that it has no transactions of the type you’re used to 
from, say, 
Postgres
. The temptation can be to
cram as much as possible into each document, which would also save on HTTP usage.
This practice is often a bad idea.
Cloudant
   
462If your model groups information that doesn’t change together, you’re more likely to suffer from update conflicts.
Consider a situation where you have users, each with a set of orders associated with them. One way might be to represent the orders as an array in
the user document:
{
 
// DON'T DO THIS
    
"customer_id"
:
 
65522389
,
    
"orders"
:
 
[
 
{
      
"order_id"
:
 
887865
,
      
"items"
:
 
[
 
{
          
"item_id"
:
 
9982
,
          
"item_name"
:
 
"Iron sprocket"
,
          
"cost"
:
 
53.0
        
}
,
 
{
          
"item_id"
:
 
2932
,
          
"item_name"
:
 
"Rubber wedge"
,
          
"cost"
:
 
3.0
        
}
      
]
    
}
  
]
}
To add an order, I need to fetch the complete document, unmarshal the JSON, add the item, marshal the new JSON, and send it back as an update. If
I’m the only one doing so, it might work for a while. If the document is being updated concurrently, 
or being replicated, we might likely see update
conflicts.
Instead, keep orders separate as their own document type, referencing the customer ID. Now the model is immutable. To add an order, I create a
new order document in the database, which cannot generate conflicts.
To be able to retrieve all orders for a specific customer, we can employ a view, which we cover later.
Avoid constructs that rely on updates to parts of existing documents, where possible. Bad data models are often hard to change after you’re in
production.
The previous pattern can be solved efficiently by using partitioned databases, which are covered in greater detailed later.
For more information, see the following documentation:
IBM Cloudant guide to 
data modeling
Database partitions
Keep documents small
IBM Cloudant imposes a max doc size of 1 MB. This limit does not mean that a close-to-1-MB document size is a good idea. On the contrary, if you
find you are creating documents that exceed single-digit KB, you probably need to revisit your model. 
Several things in IBM Cloudant become less
performant as documents grow. JSON decoding is costly, for example.
Let's look at the following sections: 
Documents must group data that mostly changes together
 and 
Keep documents small
. It’s worth stressing that
models that rely on updates have a maximum volume limit of 1 MB, the cut-off for 
document size. This size isn’t what you want.
Avoid using attachments
IBM Cloudant has support for storing attachments alongside documents, a long-standing feature it inherits from CouchDB. If you use IBM Cloudant
as a backend for a web application, you can also store small icons and other static assets such as 
CSS and JavaScript files with the data.
You must consider a few things before you use attachments in IBM Cloudant today, especially if you’re looking at larger assets such as images and
videos:
a
. 
IBM Cloudant is expensive as a block store.
b
. 
IBM Cloudant’s internal implementation is not efficient in handling large amounts of binary data.
So, slow and expensive.
IBM Cloudant is acceptable for small assets and occasional use. As a rule, if you need to store binary data alongside IBM Cloudant documents, it’s
better to use a separate solution more suited for this purpose. You need store only the attachment 
metadata
 in the IBM Cloudant document. Yes,
that means you need to write some extra code to upload the attachment to a suitable block store of your choice. Verify that it succeeded before you
store the token or URL to the attachment 
in the IBM Cloudant document.
Cloudant
   
463Your databases are smaller, cheaper, faster, and easier to replicate. For more information, see the following websites:
IBM Cloudant docs on 
attachments
Detaching IBM Cloudant attachments to 
Object Storage
Fewer databases are better than many
If you can, limit the number of databases per IBM Cloudant account to 500 or fewer. While this particular number is not magic (IBM Cloudant can
safely handle more), several use cases exist that are adversely affected by large numbers of databases 
in an account.
The replicator scheduler has a limited number of simultaneous replication jobs that it is prepared to run. As the number of databases grows, the
replication latency is likely to increase if you try to replicate everything contained in an account.
The flip side of the same coin is the operational aspect: IBM Cloudant’s operations team relies on replication, too, to move around accounts. By
keeping down the number of databases, you help us help you if you need to shift your account from 
one location to another.
So when must you use a single database and distinguish between different document types by using views, and when must you use multiple
databases to model your data? IBM Cloudant can’t federate views across multiple databases. If you have unrelated 
data that can never be “joined”
or queried together, then that data can be a candidate for splitting across multiple databases.
Avoid the 
database per user
 anti-pattern like the plague
If you’re building a multi-user service atop IBM Cloudant, it is tempting to allow each user store their data in a separate database under the
application account. That works well, mostly, if the number of users is small.
Now add the need to derive cross-user analytics. The way that you do that is to replicate all the user databases into a single analytics database. All
good. This app has suddenly become successful, and the number of users grew in the range of 
150 - 20,000. You have 20,000 replications just to
keep the analytics database current. If you also want to run in an active-active disaster recovery setup, add another 20,000 replications, and the
system stops functioning.
Instead, multiplex user data into fewer databases, or shard users into a set of databases or accounts, or both. That way, you do not need to replicate
to provide an analytics database, but authentication becomes more complicated as IBM Cloudant 
provides only authentication at the database level.
It’s worth stating that the “database-per-user” approach is tempting because IBM Cloudant permissions are “per database”, but it’s not really the
users’ fault that this pattern emerged.
Avoid writing custom JavaScript reduce functions
The MapReduce views in IBM Cloudant are awesome. However, with great power comes great responsibility. The map part of a MapReduce view is
built incrementally, so shoddy code in the map impacts only indexing time, not query time. The reduce-part, 
unfortunately, runs at query time. IBM
Cloudant provides a set of built-in reduce functions that are implemented internally in 
Erlang
. These functions are performant at 
scale while your
hand-crafted JavaScript reduces are not.
If you find yourself writing reduce functions, stop and consider whether you can reorganize your data so that writing reduce functions isn’t necessary.
Or so that you’re able to rely on the built-in reducers.
For more information, see IBM Cloudant docs on 
reduces
.
Use time boxed databases for ever-growing data sets
It’s generally 
not
 a good idea to have an ever-growing database in IBM Cloudant. Large databases can be difficult to back up, require “resharding” to
maintain good performance as they grow, and suffer from long index build times.
One way of mitigating this problem is to have several smaller databases instead, with a common pattern that is 
time-boxed databases
: a large data
set is split into smaller databases, each representing a time window, for example, a month.
orders_2019_01
 Note: 
If you have an ever-growing data set (like a log, sensor readings, or other types of time-series), it’s also not a good idea to create a
single, ever-growing, massive database. This kind of use case requires time-boxing, which we cover in more 
detail later.
 Note: 
Views on partitioned databases do not support custom reduces, which is one factor that contributes to the significant speed-up
queries only such views can offer.
Cloudant
   
464orders_2019_02
orders_2019_02
New data is written to this month’s database and queries for historical data can be directed to previous months’ databases. When a month’s data is
no longer of interest, it can be archived to Object Storage, the monthly IBM Cloudant database 
is deleted, and the disk space recovered. For more
information, see the following website.
Time-series Data Storage blog
Indexing and querying
The Index and querying document is the second best practice document in the series. It shows you the following best practices:
How to understand the different results between emitting data into a view or not.
Why you must never rely on IBM Cloudant Query's ability to query without creating explicit indexes.
Why you must limit the number of fields with IBM Cloudant Search (or IBM Cloudant Query indexes of type text).
How to manage design documents.
Why partitioned queries are faster and cheaper.
How to use the primary index as a free search index.
For more information, see 
Data modeling
 or 
IBM Cloudant in practice
.
The content in this document was originally written by Stefan Kruger as a 
Best and worst practice
 blog post on 21 November 2019.
Understand the tradeoffs in emitting data or not into a view
As the document that is referenced by a view is always available by using 
include_docs=true
, it is possible to do something like the following
example to allow lookups on 
indexed_field
:
emit(doc.indexed_field, null);
This example has the following advantages and disadvantages:
The index is compact. This index size is good, since index size contributes to storage costs.
The index is robust. Since the index does not store the document, you can access any field without thinking ahead about what to store in the
index.
The disadvantage is that getting the document back is more costly than the alternative of emitting data into the index itself. First, the database
has to look up the requested key in the index and then read the associated document. Also, if 
you’re reading the whole document, but need
only a single field, you’re making the database read and transmit data that you don’t need.
This example also means that a potential race condition exists here. The document might change, or be deleted, between the index and document
read (although unlikely in practice).
Emitting data into the index (a so-called “projection” in relational algebra terms) means that you can fine-tune the exact subset of the document that
you need. In other words, you don’t need to emit the whole document. Emit a value that represents 
only the data you need in the app that is a cut-
down object with minimal details, for example:
emit(doc.indexed_field, {name: doc.name, dob: doc.dob});
If you change your mind on what fields you want to emit, the index needs rebuilding.
IBM Cloudant Query’s JSON indexes use views this way under the hood. IBM Cloudant Query can be a convenient replacement for some types of
view queries, but not all. Do take the time to understand when to use one or the other.
IBM Cloudant Query 
docs
IBM Cloudant guide to using 
views
Performance implications of using 
include_docs
Never rely on the default behavior of IBM Cloudant Query’s no-indexing
It’s tempting to rely on IBM Cloudant Query's ability to query without creating explicit indexes. This practice is costly in terms of performance, as
every lookup is a full scan of the database rather than an indexed lookup. If your data is 
small, this full-scan lookup doesn’t matter, but as the data
set grows, performance becomes a problem for you, and for the cluster as a whole. It is likely that we will limit this facility soon. The IBM Cloudant
Cloudant
   
465Dashboard provides a method 
for creating indexes in an easy way.
Creating indexes and crafting IBM Cloudant Queries that take advantage of them requires some flair. To identify which index is being used by a
particular query, send a POST to the 
_explain
 endpoint for the database, with the query 
as data.
For more information, see 
IBM Cloudant Query docs
.
In IBM Cloudant Search (or IBM Cloudant Query indexes of type text), limit the number of fields
IBM Cloudant Search and IBM Cloudant Query indexes of type 
text
 (both of which are Apache Lucene under the hood) provide you with a way to
index any number of fields into the index. Some examples exist where this type of indexing 
is abused either deliberately, or mostly by mistake. Plan
your indexing to comprise only the fields required by your actual queries. Indexes take up space and can be costly to rebuild if the number of indexed
fields are large.
We also have the issue of which fields that you store in an IBM Cloudant Search. Stored fields are retrieved in the query without doing
include_docs=true
 so the tradeoff is similar to the 
Understand the tradeoffs in emitting data or not into a view
 
section. For more information, see
IBM Cloudant Search 
docs
.
Design document management requires some flair
As your data set grows, and your number of views goes up, sooner or later you want to ponder how you organize your views across design
documents. A single design document can be used to form a so-called 
view group
: a set of views 
that belong together by some metric that makes
sense for your use case. If your views are static, that makes your view query URLs semantically similar for related queries. It’s also more performant
at index time because the index loads the 
document once and generates multiple indexes from it.
Design documents themselves are read and written by using the same read/write endpoints as any other document. With these endpoints, you can
create, inspect, modify, and delete design documents from within your application. However, even small 
changes to design documents can have
significant effects on your database. When you update a design document, 
all
 views in it become unavailable until indexing is complete. This lag can
be problematic in production. To avoid it, you 
have to do a crazy design document-swapping dance (see 
couchmigrate
).
In most cases, this process is probably not what you want to have to deal with. As you start out, it is most likely more convenient to have a one-view-
per-design document policy.
Also, in case it isn’t obvious, views are code. Views must be subject to the same processes you use in terms of source code version management for
the rest of your application code. How to achieve this standard might not be immediately obvious. 
You could increase the version number for the
JavaScript snippets. Then, you could cut and paste the code into the IBM Cloudant Dashboard to deploy whenever a change occurs. Yes, we all resort
to this practice from time to time.
Better ways to do this exist, and we have one reason to use some of the tools that surround the 
couchapp
 concept. A 
couchapp
 is 
a self-contained
CouchDB web application that nowadays doesn’t see much use. Several 
couchapp
 tools exist that are there to make the deployment of a
couchapp
, including its views, crucially, easier.
Using a 
couchapp
 tool means that you can automate deployment of views as needed, even when not using the 
couchapp
 concept itself.
See, for example, 
couchapp
 and 
situp
.
IBM Cloudant guide to 
design document management
.
Partitioned queries are faster and cheaper
Yes, partitioned queries are faster and cheaper. Opting to create a 
partitioned database
 (as opposed to an unpartitioned database) means that IBM
Cloudant uses a 
partition key
 to decide on which shard each of your documents 
resides. Documents with the same 
partition key
 are on the same
database shard. Requests for 
_all_docs
, MapReduce views, IBM Cloudant Query 
_find
 queries, and IBM Cloudant Search operations can be
directed 
to a single partition instead of having to interrogate all shards in a “scatter and gather” pattern, which is the case for 
global queries
.
These 
partitioned queries
 exercise only one shard of the database. This practice makes them faster to execute than global queries. For billing
purposes, they are classified as “read” requests instead of the more expensive “query” requests, 
which provides you with more usable capacity from
the same IBM Cloudant plan.
Not all data designs lend themselves to a partitioned design, but if your data can be molded into a 
<partition key>:<document key>
 pattern, then
your application can benefit in terms of performance and cost.
Partitioned Databases documentation
Partitioned Databases - Introduction blog
Treat the primary index as a free search index
Cloudant
   
466A default IBM Cloudant document 
_id
 is a 32-character string, encoding 128 bits of random data. The 
_id
 attribute is used to construct the
database’s primary index, which is used by IBM Cloudant to retrieve documents 
by 
_id
 or ranges of keys when the user supplies a
startkey/endkey
 pair. We can leverage this fact to pack our data into the 
_id
 field and use it as a “free” index that can query for ranges of values.
See some examples in the following list:
Use time-sortable document IDs so that your documents are sorted into rough date and time order. This sorting makes it easy to retrieve
recent additions to the database. For more information, see 
Time-sortable -IDs
.
Pack searchable data into your 
_id
 field, for example, 
<customerid>~<date>~<orderid>
 can be used to retrieve data by 
customer
,
customer/date
, or 
customer/date/orderid
.
In a partitioned database, the judicious choice of 
partition key
 allows an entire database to be winnowed down to a handful of documents for a
known partition key. Make sure that your partitioning schema solves your most common use 
case.
In a partitioned database, the two parts of the key have to contain your user-supplied data (no auto-generated 
_ids
 exist) so it’s best to use it
optimally. For example, in an IoT application, 
<sensorid>:<time-sortable-id>
 
allows data to be sorted by sensor and time without a
secondary index. Implement this schema with 
time-boxed databases
 for best results.
IBM Cloudant in practice
The IBM Cloudant in practice document is the third best practice document in the series. It shows you the following best practices:
How to avoid conflicts.
How deleting documents works.
What to watch out for with updates.
How to work in an eventually consistent environment.
How to set up replication.
How to use the bulk API.
Why you must not change Q, R, and N.
How rate limits work.
What logging tracks.
How to compress your HTTP traffic.
For more information, see 
Data modeling
 or 
Indexing and querying
.
The content in this document was originally written by Stefan Kruger as a 
Best and worst practice
 blog post on 21 November 2019.
Avoid conflicts
IBM Cloudant is designed to treat conflicts as a natural state of data in a distributed system. This feature is a powerful feature that helps an IBM
Cloudant cluster always maintain high availability. However, the assumption is that conflicts 
are still reasonably rare. Tracking conflicts in IBM
Cloudant’s core has significant cost that is associated with it.
It is perfectly possible (but a bad idea!) to ignore conflicts. The database merrily carries on operating by choosing a random, but deterministic
revision of conflicted documents. However, as the number of unresolved conflicts grows, the performance 
of the database goes down a black hole,
especially when you replicate.
As a developer, it’s your responsibility to check for, and to resolve, conflicts, or even better, employ data models that make conflicts impossible.
If you routinely create conflicts, you must really consider model changes: even if you resolve your conflicts diligently, the conflict branches in the
revision tree remain with no easy way to tidy that up. For more information, see the following 
websites:
IBM Cloudant guide to 
conflicts
IBM Cloudant guide to versions and 
MVCC
Three-part blog series on 
conflicts
Deleting documents doesn't delete them
Deleting a document from an IBM Cloudant database doesn’t purge it. Deletion is implemented by writing a new revision of the document under
deletion, with an added field 
_deleted: true
. This special revision is called a 
tombstone
. 
Tombstones still take up space and are also passed
around by the replicator.
Models that rely on frequent deletions of documents are not suitable for IBM Cloudant. For more information, see IBM Cloudant tombstone 
docs
.
Cloudant
   
467Be careful with updates
It is more expensive in the end to mutate existing documents than to create new ones. IBM Cloudant always needs to keep the document tree
structure around
. This rule applies even if internal nodes in the tree are stripped of their payloads. 
If you find that you create long revision trees, your
replication performance suffers. Moreover, if your update frequency is higher than, say, once or twice every few seconds, you’re more likely to
produce update conflicts.
Prefer models that are immutable.
When you read the following sections, 
Deleting documents doesn't delete them
 and 
Be careful with updates
, they provoke an obvious question. That
is, does the data set grow unbounded if my model is immutable? If you accept that 
deletes don’t completely purge the deleted data and that updates
are not updating in place in terms of data volume growth, not much difference exists. Managing data volume over time requires different techniques.
The only way to truly reclaim space is to delete databases, rather than documents. You can replicate only winning revisions to a new database and
delete the old to get rid of lingering deletes and conflicts. Or perhaps you can build it into 
your model to regularly start new databases (say ‘annual
data’) and archive off (or remove) outdated data, if your use case allows.
natural to most people.
a
. 
b
. 
c