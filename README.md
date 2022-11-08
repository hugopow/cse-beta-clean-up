# cse-beta-clean-up

https://vmwire.com/2022/11/08/cleaning-up-cse-4-0-beta/

CSE 4.0 will GA this quarter. For those partners that have been testing the beta, you’ll need to remove all traces of it before you can install the GA version. VMware does not support upgrading or migrating from beta builds to GA builds.

If you don’t clean up, when you try to configure CSE again with the CSE Management wizard, you’ll see the message below:

“Server configuration entity already exists.”

1. Import this collection into Postman.
2. Create an environment for your VCD environment variable using vcd_public_address
3. Run through each API call in the collection.


4. Change pending cluster's serviceDomain - this is not required for the clean-up but you can use this for the beta.


-Power off CSE beta appliance

-Deploy CSE cluster

-Use this API to change the serviceDomain from the default k8s.test to cluster.local by editing the body of the PUT call

-Power on CSE beta appliance

-CSE will then deploy the new cluster with the changed serviceDomain.

-Note that you cannot change the serviceDomain on an already deployed cluster.

