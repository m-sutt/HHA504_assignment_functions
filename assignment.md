##  Serverless computing and cron jobs in Azure, GCP, and GitHub

### Step 1: Deploy a Serverless Function in Azure
  - From Function App: Click **Create**. Choose **Subscription** and create a new **Resource Group**. Set **Function App name**. Choose Runtime stack as  **Python**. Select **Region**. Click  **Review + Create** then **Create**.

![Azure1](https://github.com/user-attachments/assets/f27687c8-1457-429a-8fd9-35ed68a39a60)

![Azure2](https://github.com/user-attachments/assets/7f441910-b82a-43e2-9d3f-479d3305b590)



### Step 2: Deploy a Serverless Function in GGP
- From Cloud Run functions: Click **Create function**. Trigger type **HTTPS**
- Write function code: **Runtime Enviroment** = **Python**.

![GCP1](https://github.com/user-attachments/assets/9ae33079-7031-4bee-89ed-3ff65bd5b896)

![GCP2](https://github.com/user-attachments/assets/c8fa2e16-2fae-404a-990d-7261056f0826)

![GCP3](https://github.com/user-attachments/assets/b3114de9-1cb1-47bf-8d36-edb16acd0a87)


### Step 3: Create a Cron Job Using GitHub Actions
  - Set up GitHub action workflow. Commit and Push.
  - **Problem**: Had an issue with Visual Studio Code not commiting to changes to GitHub.
    
<img width="941" alt="VSC" src="https://github.com/user-attachments/assets/c883f306-4da7-4fd2-a2f0-8037659330af">


### Reflection on Functions as a Service (FaaS):
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
