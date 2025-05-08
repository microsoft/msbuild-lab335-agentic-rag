# Exercise 3: (Optional) Run Automated Evaluation for Retrieval Modes

In this optional exercise, you will follow a series of steps to evaluate the quality of the answers and assess the performance of each retrieval mode. This process will help you understand how different retrieval strategies impact the results.

1. Make sure the app is running locally before running evaluation. If you closed the app, you can open the terminal in VS Code, run the following commands to start the app locally:

    +++cd app+++
    
    +++./start.ps1+++
   
1. Once your app is running locally, open another terminal and enable evaluation in your environment by running the following command in the terminal:

    +++*azd env set USE_EVAL true*+++

    +++*azd env set AZURE_OPENAI_EVAL_DEPLOYMENT_CAPACITY 100*+++

    +++*azd provision*+++

    This will take a few minutes to complete. You can monitor the progress in the terminal window.

1. Set up a virtual environment for evaluation by running the following command in the terminal:

    +++*python -m venv .evalenv*+++

    +++*.evalenv\Scripts\Activate*+++

    +++*pip install -r evals/requirements.txt*+++

1. Open the **evals/ground_truth.jsonl** file and look through the current ground truth answers.

    > [!TIP]
    > These question-answer pairs were previously generated based off the sample documents and will be used for evaluation.

1. Run the evaluator on your app by running the following command in the terminal:

    +++*python evals/evaluate.py --numquestions=5 --resultsdir=evals/results/firstfive*+++

1. Review the evaluation results by running the following command in the terminal:

    +++*python -m evaltools summary evals/results*+++

    This will show you the overall evaluation metrics across evaluation runs. Since your evaluation was only done on 5 questions, it's difficult to compare fully to the other runs, but you may be interested to see the metrics for full runs.

1. Compare the questions with the baseline by running the following command in the terminal:

    +++*python -m evaltools diff evals/results/baseline evals/results/firstfive*+++

    This will show you the questions and answers from your run as compared to the baseline. They should be fairly similar, since the app configuration is the same, but there may be differences due to the non-determinism of LLMs.

## Next Step

> Select **Next >** to go to the next exercise on enabling agentic features.
