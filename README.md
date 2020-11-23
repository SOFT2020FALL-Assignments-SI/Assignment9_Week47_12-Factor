## Assignment9_Week47_12-Factor
**[Assignment Link]( https://datsoftlyngby.github.io/soft2020fall/resources/80748096-A9-12-Factor-App.pdf)**  

### 1. Codebase  
Developer codebase tracked on version control – ex. Git.

### 2. Dependencies
Independent of depencies and system tools – example should dependencies could be downloaded when application is build on machine.

### 3. Config
Config should be separated from code, and be hardcoded values in the codebase. Config credentials should be stored in environment variables.

### 4. Backing services
Service consumed over network – example DB (ex. mySQL) or messaing (ex. RappidMQ). These should be treated like a resource and should be independent of service type – example local developer has MySQL, but production environment hast PostgreSQL.

### 5. Build, release, run
These 3 stages should be stricted separated. Releases should be tagged with release number and timestamp, that you could make the possibility to rollback to earlier releases.

### 6. Processes
Processes should be stateless and only use resources from a backing service. Nothing should be cached locally and used, but instead local memory could be used for downloading and then insert result of operation in backing service ex. a database.

### 7. Port binding
WEB Apps should be self-contained as a HTTP service bindings to a port number, and then use this port number listening for requests. This port number should independent on a local environment and production environment.

### 8. Concurrency
Workloads can be assigned into more processes and threads.

### 9. Disposability
Processes has minimum of start-up time and graceful shutdown. Furthermore, processes should resist of hard shutdown – ex. hardware failures.

### 10. Dev/prod parity
Continuous deployment, and the possibility that local development and production environment has same type of service, but local can be more lightweight processes – ex. SQLite on local and PostgreSQL on production.

### 11. Logs
These should be used for see behavior of a running app. Logs is one liner based on timestamp and event happened. Exception logs with stacktraces could be on more than one line.

### 12. Admin processes
These processes should be run I same type of environment for both local and production, and these is run as one-off processes.

### Source links
**https://12factor.net/**  
***

