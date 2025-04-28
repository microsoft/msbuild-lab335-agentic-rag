# Exercise 4: Enable Agentic Features

In this exercise, you will turn on features that allow the system to reason across multiple steps and refine its answers.

## Step 1: Enable Agentic Retrieval and Reflection

Run the following command in the terminal to redeploy the app with agentic features enabled:

+++*azd env set USE_AGENTIC_RETRIEVAL true*+++

+++*azd env set USE_AGENTIC_REFLECTION true*+++

+++*azd up*+++

This will take a few minutes to complete. You can monitor the progress in the terminal window.

## Step 2: Test the App with Agentic Features

Use the same 5 questions you used in the previous exercise to test the app. You can ask the questions in any order.

- +++Can you explain the eligibility criteria for the Northwind Standard plan offered to Contoso employees?+++
- +++What are the financial implications of choosing an out-of-network provider under the Northwind Standard Benefits plans?+++
- +++How does Northwind Health Plus manage coinsurance for virtual care services?+++
- +++What's the impact of choosing in-network versus non-participating providers on your healthcare costs, and what are the exceptions to prior authorization that do not require prior approval?+++
- +++What are the limitations of the Right of Recovery provision in the Northwind Health Plus plan?+++
- +++What are the financial responsibilities of a Northwind Standard plan holder when using out-of-network providers?+++
- +++Does Northwind Health cover full costs?+++

For each answer, observe the difference in the process used to generate the answer in the **Thought process** tab.

Take note of the following:

- Do the search results look different?
- Does the RAG process take more steps than before?
- Does the answer improve after reflection?

## Step 3: (Optional) Re-Run Automated Evaluation with Agentic Features

Compare your answers before and after enabling agentic features manually first. You can log scores or just discuss with others what has changed.

If you enabled evaluation in Exercise 1, you can now re-run the evaluator to compare how the system performs with agentic capabilities turned on.

1. Make sure the app is deployed with agentic features:

    +++*azd env set USE_AGENTIC_RETRIEVAL true*+++

    +++*azd env set USE_AGENTIC_REFLECTION true*+++

    +++*azd up*+++

1. Run the evaluator on your app by running the following command in the terminal:

    +++*python evals/evaluate.py --numquestions=5 --resultsdir=firstfive-agentic*+++

    This will create a new results folder in **firstfive-agentic** with an evaluation of the first five answers.

1. Compare the new results with the baseline:

    +++*python -m evaltools diff evals/results/firstfive evals/results/firstdive-agentic*+++

    >[!TIP]
    > You don’t need to regenerate ground truth unless your documents or questions changed. The goal here is to measure how reasoning quality and citation accuracy evolve with agentic logic.
    