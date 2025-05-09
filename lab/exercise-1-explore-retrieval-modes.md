# Exercise 1: Run the App Locally and Explore Retrieval Modes

In this exercise, you will run the app locally and explore the different retrieval modes available in the app. Let's begin by exploring how different search configurations change the quality of answers.

## Step 1: Start the App Locally

1. In the terminal in VS Code, run the following commands to start the app locally:

    +++*cd app*+++

    +++*./start.ps1*+++

    This will take approximately 7 minutes to complete. You will see a message in the terminal when the app is ready.

1. From your, taskbar open the **Microsoft Edge** browser and open the following URL:

    +++*http://localhost:50505*+++

## Step 2: Explore the Retrieval Modes

1. From the homepage, select **Developer Settings**, this opens a panel that allows you to experiment with different search and answer generation parameters.

1. In this panel, scroll down to the **Retrieval Mode** dropdown. Select **Vectors** from the dropdown. Close the panel ask the following question:

    +++*What’s included in the Business plan?*+++

    By applying the **Vectors** retrieval mode, the app will retrieve documents purely on semantic similarity. Note the quality of the answer and the relevance of the citations.

1. Next, switch the **Retrieval Mode** back to **Vectors + Text(Hybrid)**. Close the panel and ask the same question again:

    +++*What’s included in the Business plan?*+++

    By applying the **Hybrid** retrieval mode, the app will retrieve documents based on both semantic similarity (vector search) and keyword matching.
  
    Compare the two answers and note the differences. You will notice that the results have a stronger relevance and coverage.

## Next Step

> Select **Next >** to go to the next exercise on exploring semantic ranking in Azure AI Search.
