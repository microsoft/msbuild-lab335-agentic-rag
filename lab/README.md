# Session folder

This folder contains the public facing files for the Microsoft Build 2025 lab 335 `Build Your First Agentic RAG Solution with Azure AI Search`.

## Before you start

> [!TIP]
> As you follow the instructions in this pane, whenever you see a +++icon+++, you can use it to copy text from the instruction pane into the virtual machine interface. This is particularly useful to copy code; but bear in mind you may need to modify the pasted code to fix indent levels or formatting before running it!

## Sign into Windows

In the virtual machine, sign into Windows using the following credentials:

- **User name**: +++@lab.VirtualMachine(Win11-Pro-Base-VM).Username+++
- **Password**: +++@lab.VirtualMachine(Win11-Pro-Base-VM).Password+++

## Access and set up the lab repository

In this hands-on lab, you'll deploy a RAG (Retrieval-Augmented Generation) app using Azure AI Search and Azure OpenAI. Then, you'll unlock agentic capabilities like dynamic retrieval planning and reflection to elevate the app’s intelligence. You'll also learn how to evaluate and compare results using tricky questions.

Once signed in, you should find the working repo pre-cloned to the desktop. This can be found on the folder named **azure-search-openai-demo** on the desktop. The repo contains all the code and resources you need to complete the lab.

Open the folder in the terminal by right-clicking on the folder and selecting **Open in Terminal**.

Next, open the folder in VS Code by running the command +++*code .*+++ in the terminal. This will open the folder in VS Code, where you can explore the code and resources.

>[!TIP]
> When you  open the folder in VS Code, you may see get a prompt window asking if you trust the authors of the files in the folder. This is expected and you can safely select **Yes, I trust the authors**.

Next you need to complete the following setup steps to authenticate to Azure and deploy the resources:

1. Open the **.azure/Lab335.../.env** file and only continue with the next steps if the file contains 45 environment variables.

1. In VS Code, open the terminal by selecting **Terminal** > **New Terminal** from the menu bar.

1. In the terminal window run the following command to to authenticate to azure:

   +++*azd auth login*+++

   This will open a new browser window where you can sign in to your Azure account. Use the following credentials to sign in:
      - **Email**: +++@lab.CloudPortalCredential(User1).Username+++
      - **Password**: +++@lab.CloudPortalCredential(User1).Password+++

   Once you sign in, close the browser window and return to the terminal in VS Code and confirm that you were successfully authenticated.

1. Next, provision and deploy azure resources by running the following command in the terminal:

   +++*azd up*+++

    The deployment process will take a few minutes. You can monitor the progress in the terminal window.

    Once completed, you’ll see a URL in the terminal where your app is deployed. Open it in your browser and ask a sample question to confirm it works.

## Exercises in this lab

Now you're ready to complete the exercises in this lab. The lab includes multiple exercises, so when you finish one, just move onto the next one. The exercises in this lab are:

- Exercise 1: Run Locally and Explore Retrieval Modes
- Exercise 2: Explore Semantic Ranking in Azure AI Search
- Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes
- Exercise 4: Enable Agentic Features

The exercises are designed to be completed in order because they build on the data and resources created in the previous exercises, so make sure you complete each exercise before moving on to the next one.

Don't worry if you run out of time to complete the entire lab. All of these exercises (and more) are available on [RAG Time](https://aka.ms/rag-time).

Select **Next >** to go to the first exercise.

===

!INSTRUCTIONS [Exercise 1: Run the App Locally and Explore Retrieval Modes](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-1-explore-retrieval-modes.md)

===

!INSTRUCTIONS [Exercise 2: Explore Semantic Ranking in Azure AI Search](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-2-adjust-semantic-ranker.md)

===

!INSTRUCTIONS [Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-3-optional-automated-evaluation.md)

===

!INSTRUCTIONS [Exercise 4: Enable Agentic Features](https://raw.githubusercontent.com/microsoft/msbuild-lab335-agentic-rag/refs/heads/main/lab/exercise-4-enable-agentic-features.md)