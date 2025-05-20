# Session folder

This folder contains the public facing files for the Microsoft Build 2025 lab 335 `Build Your First Agentic RAG Solution with Azure AI Search`.

## Before you start

In this lab, you'll deploy and enhance a Retrieval-Augmented Generation (RAG) app using Azure AI Search and Azure OpenAI. You'll begin by exploring different retrieval strategies (like vector, hybrid, and semantic ranking), then progressively add agentic capabilities like dynamic retrieval planning and self-reflection. By the end, you'll evaluate how each version performs on tricky questions-giving you a hands-on understanding of what makes AI search intelligent, adaptable, and useful in real-world scenarios.

> [!TIP]
> As you follow the instructions in this pane, whenever you see a +++icon+++ to copy code or text directly into the virtual machine. This is especially helpful for CLI commands or config blocks but double-check formatting or indentation after pasting!

## Sign into Windows

In the virtual machine, sign into Windows using the following credentials:

- **User name**: +++@lab.VirtualMachine(Win11-Pro-Base).Username+++
- **Password**: +++@lab.VirtualMachine(Win11-Pro-Base).Password+++

## Access and set up the lab repository

Once signed in to the Skillable environment, you'll find the lab repo pre-cloned on the desktop under the folder **Desktop > azure-search-openai-demo**. This folder contains all the code and resources you'll need.

## Open the project folder in your dev environment

Right-click to the **azure-search-openai-demo** folder on your Desktop and select **Open in Terminal**.

Run the following command to open the project in Visual Studio Code:

+++code .+++

When prompted whether to trust the authors of the files, select **Yes, I trust the authors**.

> [!TIP]
> You may see pop-up message in VS Code **Dev Container prompt**. This appears when you first open the app folder. Select **Don’t Show Again** or close it, as you won’t be using a container in this lab.
> 
> <img width="447" alt="Screenshot 2025-05-20 at 7 38 10 AM" src="https://github.com/user-attachments/assets/177fdb8f-c4e9-4963-bbfe-e45d209b9caa" />


## Authenticate and Deploy Resources to Azure

Next you need to complete the following setup steps to authenticate to Azure and deploy the resources:

1. Open the **.azure/Lab335.../.env** file and only continue with the next steps if the file contains 60 environment variables.

1. In VS Code, open the terminal by selecting **Terminal** > **New Terminal** from the menu bar.

1. In the terminal window run the following command to to authenticate to Azure:
	
   +++*azd env set GITHUB_ACTIONS ""*+++
   
   +++*azd auth login*+++

   This will open a new browser window where you can sign in to your Azure account. Use the following credentials to sign in:
      - **Email**: +++@lab.CloudPortalCredential(User1).Username+++
      - **Password**: +++@lab.CloudPortalCredential(User1).Password+++

   Once you sign in, close the browser window and return to the terminal in VS Code and confirm that you were successfully authenticated.

1. Next, provision and deploy azure resources by running the following command in the terminal:

   +++*azd up*+++

    The deployment process will take a few minutes. You can monitor the progress in the terminal window.

    Once completed, you'll see a URL in the terminal where your app is deployed. Open it in your browser and ask a sample question to confirm it works.

## Exercises in this lab

Now you're ready to complete the exercises in this lab. The lab includes multiple exercises, so when you finish one, just move onto the next one. The exercises in this lab are:

- Exercise 1: Explore Retrieval Modes
- Exercise 2: Explore Semantic Ranking in Azure AI Search
- Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes
- Exercise 4: Enable Agentic Features

The exercises are designed to be completed in order because they build on the data and resources created in the previous exercises, so make sure you complete each exercise before moving on to the next one.

Don't worry if you run out of time to complete the entire lab. All of these exercises available on [our repo](https://aka.ms/msbuild-lab335).

Select **Next >** to go to the first exercise.

===

!INSTRUCTIONS [Exercise 1: Explore Retrieval Modes](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-1-explore-retrieval-modes.md)

===

!INSTRUCTIONS [Exercise 2: Explore Semantic Ranking in Azure AI Search](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-2-adjust-semantic-ranker.md)

===

!INSTRUCTIONS [Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-3-optional-automated-evaluation.md)

===

!INSTRUCTIONS [Exercise 4: Enable Agentic Features](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-4-enable-agentic-features.md)

===

!INSTRUCTIONS [Wrap-Up](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/wrap-up.md)
