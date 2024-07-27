# RAG Pipeline: Evaluating Metrics and Guardrailing Efficiency

* Video Walkthrough - 

## Overview

This notebook demonstrates how to build, evaluate, and optimize a Retrieval-Augmented Generation (RAG) model from scratch. It includes steps for logging performance, obtaining feedback on LLM responses, and applying optimization techniques to enhance the model's efficiency.

## Assignment Details

- **Name:** Krishnakanth Naik Jarapala
- **NUID:** 002724795

## Key Objectives

1. **Build a RAG Model:**
   - Learn to create a custom RAG model from scratch.
   - Integrate data sources, design retrieval mechanisms, and connect with a generative model.

2. **Log Model Performance:**
   - Utilize TruLens for advanced logging and performance monitoring.

3. **Obtain Feedback:**
   - Evaluate model responses using the "hallucination triad" focusing on:
     - Groundedness
     - Context Relevance
     - Answer Relevance

4. **Optimize Efficiency:**
   - Improve the RAG model’s efficiency using feedback results as guardrails.
   - Apply context filtering to reduce hallucinations and enhance response relevance.

## Installation

```bash
pip install trulens_eval chromadb openai llama-index
```

## Data Preparation

- **Sample Data Initialization:**
  - Added text samples related to universities and landmarks to simulate query results.

## Building the RAG Model

1. **Create a Custom RAG Model:**
   - Set up data sources and retrieval mechanisms.
   - Connect with a generative language model for response generation.

2. **Integrate TruLens Instrumentation:**
   - Use TruLens to log key metrics and monitor performance.
   - Set up alerts and dashboards for continuous evaluation.

## Feedback Functions

- **Groundedness:** Measures if responses are based on verifiable information.
- **Answer Relevance:** Assesses how well responses address the input queries.
- **Context Relevance:** Evaluates the coherence of responses within the given context.

## Constructing the App

1. **Wrap the Custom RAG:**
   - Integrate the RAG model using TruCustomApp.

2. **Add Feedback Mechanisms:**
   - Implement feedback functions to enhance model evaluation.

3. **Set Up Evaluation:**
   - Configure TruCustomApp to use feedback functions for continuous improvement.

## Inference

- Use `TruCustomApp` as a context manager to run queries and record results.
- View results on the leaderboard for performance metrics.

## Optimization: Implementing Guardrails

- Apply context relevance scores to filter out irrelevant contexts before they reach the LLM.
- Rebuild the RAG model with the `@context-filter` decorator to enhance efficiency and reduce hallucinations.

## Results

**Filtered Context RAG Model:** Achieved improved context relevance and performance metrics compared to the baseline RAG model.

- Before Applying the Feedbacks:

  <img width="464" alt="image" src="https://github.com/user-attachments/assets/397cc61a-0b7f-4c8a-ae23-a8775d5e9906">

- After Applying the Feedback and Filtering the Context:
  
  <img width="521" alt="image" src="https://github.com/user-attachments/assets/139f3dbf-f70c-4c6e-8c3d-700c0e756158">

- Overall Performance of the Model:
  ![4658](https://github.com/user-attachments/assets/0daa3173-a56a-4d13-877e-b4ca3a1b24ed)


## Conclusion

The notebook illustrates the process of building a RAG model, integrating performance logging, obtaining feedback, and optimizing efficiency through advanced techniques like filtering. For further insights, view detailed results and feedback in the provided outputs.

## Future Work

- Experiment with different feedback functions and thresholds.
- Explore additional optimization techniques and model improvements.

Feel free to explore and modify the notebook to fit your specific use case and data requirements.
