# Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes

> [!TIP]
> This step is optional. If you'd prefer to skip automated evaluation and go directly to agentic features, proceed to Exercise 4: Enable Agentic Features.
 
In this exercise, you will follow a series of steps to evaluate the quality of the answers and assess the performance of each retrieval mode. You'll evaluate answer quality by comparing model-generated responses to predefined ground truth answers, helping you understand how each retrieval strategy affects output accuracy.

1. Run the app locally before running evaluation. Open the terminal in VS Code, run the following commands to start the app locally:

    +++cd app+++

    +++./start.ps1+++
   
> [!TIP]
> Keep the app running in this terminal locally. Open a new terminal for the following steps.

1. Once your app is running locally, open another terminal by selecting **Terminal** > **New Terminal** from the menu bar.

1. Enable evaluation in your environment by running the following command in the terminal:

    +++*azd env set USE_EVAL true*+++

    +++*azd env set AZURE_OPENAI_EVAL_DEPLOYMENT_CAPACITY 100*+++

    +++*azd provision*+++

    This will take a few minutes to complete. You can monitor the progress in the terminal window.

1. Start the pre-set virtual environment for evaluation by running the following command in the terminal:

    +++*.evalenv\Scripts\Activate*+++

1. Open the **evals/ground_truth.jsonl** file and look through the current ground truth answers.

    > [!TIP]
    > These question-answer pairs were previously generated based off the sample documents and will be used for evaluation.

1. Run the evaluator on your app by running the following command in the terminal:

    +++*python evals/evaluate.py --numquestions=5 --resultsdir=evals/results/firstfive*+++

    This will add a new folder called **firstfive** to the **evals/results/** directory. This folder contains the evaluation results for the first five questions in the ground truth file.

1. Review the evaluation results by running the following command in the terminal:

    +++*python -m evaltools summary evals/results*+++

    This will show you the overall evaluation metrics across evaluation runs. Since your evaluation was only done on 5 questions, it's difficult to compare fully to the other runs, but you may be interested to see the metrics for full runs.

1. Compare the questions with the baseline by running the following command in the terminal:

    +++*python -m evaltools diff evals/results/baseline evals/results/firstfive*+++

    This will show you the questions and answers from your run as compared to the baseline. They should be fairly similar, since the app configuration is the same, but there may be differences due to the non-determinism of LLMs. 

> [!TIP]
> Quit the eval tool before proceeding and close the terminals.

## Next Step

> Select **Next >** to go to the next exercise on enabling agentic features.
