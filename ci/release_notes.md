# Improvements

- Blacksmith now regularly (hourly) checks the BOSH director to see
 if any deployments it has made have been deleted out-of-band,
 and removes them from the Vault index.

- In the above check Blacksmith also runs a bosh cleanup task on Blacksmith's
 inner Bosh director to remove unused stemcells, releases, etc

# New Features

- Blacksmith now has a new `/b/cleanup` endpoint for doing the above 2 checks if
 you want to run the checks/cleanups without waiting for the hourly timer

# Developer Stuff

- We have switched our vendoring tool from godeps to govendor, and have susbsequently 
 cleaned up the libraries we weren't using.