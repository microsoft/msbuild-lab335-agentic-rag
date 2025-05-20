# Exercise 1: Explore Retrieval Modes

In this exercise, you’ll explore the core retrieval modes that power your RAG app: vector and hybrid search. By switching between these modes and asking the same question, you’ll compare how each method affects the quality and relevance of answers.

## Step 1: Open the App in your Browser

In this exercise, you’ll test how different retrieval modes (Vectors and Hybrid) affect the quality and grounding of AI-generated answers in your deployed app.

1. If you successfully completed the previous setup and deployment using the *azd up* command, you should see a deployment URL printed in the terminal.

1. Use **Ctrl + Click** to open the URL in your browser, or copy and paste it into a new browser tab. Make sure the app loads and you're able to see the chat interface.

    ![Screenshot 2025-05-14 at 6 12 33 PM](https://github.com/user-attachments/assets/57104952-2e55-434d-a38a-869ede36cb54)

## Step 2: Explore the Retrieval Modes

1. From the homepage, select **Developer Settings**, this opens a panel that allows you to experiment with different search and answer generation parameters.

    ![Developer Settings](media/developer-settings.png)

1. In this panel, scroll down to the **Retrieval Mode** dropdown. Select **Vectors** from the dropdown. Close the panel and ask the following question:

    +++*What is included in my Northwind Health Plus plan that is not in standard?*+++

    By applying the **Vectors** retrieval mode, the app will retrieve documents purely on semantic similarity. Note the quality of the answer and the relevance of the citations.

1. Next, switch the **Retrieval Mode** back to **Vectors + Text(Hybrid)**. Close the panel and ask the same question again:

    +++*What is included in my Northwind Health Plus plan that is not in standard?*+++

    By applying the **Hybrid** retrieval mode, the app will retrieve documents based on both semantic similarity (vector search) and keyword matching.
  
    Compare the two answers and note the differences. You will notice that the results have a stronger relevance and coverage.

## Next Step

> Select **Next >** to go to the next exercise on exploring semantic ranking in Azure AI Search.
