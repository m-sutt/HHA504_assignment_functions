##  Serverless computing and cron jobs in Azure, GCP, and GitHub

### Step 1: Deploy a Serverless Function in Azure
  - From Function App: Click **Create**. Choose **Subscription** and create a new **Resource Group**. Set **Function App name**. Choose Runtime stack as  **Python**. Select **Region**. Click  **Review + Create** then **Create**.

![Azure1](https://github.com/user-attachments/assets/f27687c8-1457-429a-8fd9-35ed68a39a60)

![Azure2](https://github.com/user-attachments/assets/7f441910-b82a-43e2-9d3f-479d3305b590)



### Step 2: Deploy a Serverless Function in GGP
- From Cloud Functions: Click **Create Function**. Choose **HTTP Trigger**.
- Write function code: **Runtime Enviroment** = **Python**.





### Step 3: Create a Cron Job Using GitHub Actions
  - Set up GitHub action workflow. Commit and Push.

### Reflecction on Functions as a Service (FaaS):
 - Use cases:
    - Event-driven workflow: workflow can be triggered from a variety of actions such as a user uploading a file to the a cloud storage, a change that occurs within a DB.
    - Automation or scheduled tasks: moving files when certain conditions are met, or sending a email or notifications.
    - Real-time data processing: can be use to transform data when new records are created in DB such as analyzing data when it is entered.
 - Benefits:
    - No infrastructure management: you don't need to maintain servers or VMs yourself. Cloud providers takes of scaling.
    - Auto-scaling: functions automatically scale depending on workload.
    - Cost: only pay for actual compute time, rather than running a server.
    - Event-driven: functions are triggered by events, like HTTP requests or file uploads, therefore, can response to real world trigger and be very versatile.
 - Limitations:
     - Latency: may take a while for first request or a request that has not be used in some time
     - Execution time limit, therefore, not suitable for long-running tasks
     - Limit configuration since vendor controls allocation of resources.
