 ## The Twelve factors
 The twelve factors helps us to develop an application which is modular,independent, portable, scalable and observable

 #### 1. Codebase
 ###### One codebase tracked in revision control, many deploys
 
 #### 2. Dependencies
 ###### Explicitly declare and isolate dependencies
 Do not copy any dependencies to the project codebase, instead use a package manager. Always remember to use the correct versions of dependencies 
 so that all environments are in sync and reproduce the same behavior.
 
 #### 3. Config
 ###### Store config in the environment
 Store the config in Environment Variable. There should be a strict separation between config and code. The code 
 should remain the same irrespective of where the application is being deployed, but configurations can vary.
 
 #### 4. Backing services
 ###### Treat backing services as attached resources
 Treat backing services as attached resources as your services should be easily interchangeable.
  You must be able to easily swap the backing service from one provider to another without code changes.
  This will ensure good portability and help maintain your system.
  
 #### 5. Build, release, run
 ###### Strictly separate build and run stages
 A twelve-factor application requires a strict separation between Build, Release and Run stages. 
 Every release should always have a unique release ID and releases should allow rollback.
 
 #### 6. Processes
 ###### Execute the app as one or more stateless processes
 You should not be introducing state into your services, applications should execute as a single, stateless process. 
 The Twelve-factor processes are stateless and share-nothing.
 
 #### 7. Port binding
 ###### Export services via port binding
 
 Your service should be visible to others via port binding. If you built a service, make sure that other services can treat this as a resource if they wish. 
 The twelve-factor app is completely self-contained
 #### 8. Concurrency
 ###### Scale out via the process model
 Building your applications so that the scaling them in the cloud is seamless. In order to increase scalability ,you can just add more instances 
 instead of more memory or cpu on the machine
 
 #### 9. Disposability
 ###### Maximize robustness with fast startup and graceful shutdown
 
 Building disposability into application ensures that the app shutdown gracefully, it should clean up all utilized resources
and shutdown smoothly. One service failure should not effect the other services. User should be able to use the other services until the service 
that is down comes back.

 #### 10. Dev/prod parity
 ###### Keep development, staging, and production as similar as possible
 
  #### 11. Logs
 ###### Treat logs as event streams
 
 Logs should be treated as continuous streams that is captured and stored by a separate service. e.g splunk
 
 #### 12. Admin processes
 ###### Run admin/management tasks as one-off processes
 This twelve factor principle strongly suggests to keep the admin process scripts like (Scripts to fix the bad data, scripts to insert master data into database tables etc)
together with the application code base.
