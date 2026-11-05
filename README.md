# Week 11 – Prompt Templates and LangChain Chains

## Overview
This experiment demonstrates how to use prompt templates and LangChain chains with Groq. It takes information about Retrieval-Augmented Generation (RAG) and generates a summary using a predefined prompt template.

## Objective
To understand reusable prompt templates, connecting an LLM to a prompt-processing chain, and converting model responses into plain text using an output parser.

## Technologies Used
- Python
- LangChain
- LangChain Groq
- Groq API
- Google Colab (if using Colab Secrets)

## Experiment Description

### 1. Input Data
The experiment uses a short passage explaining Retrieval-Augmented Generation (RAG).

### 2. Prompt Template
`ChatPromptTemplate.from_template()` creates a reusable prompt with a `{data}` placeholder.

The instruction asks the model to summarize the supplied content in exactly 10 sentences.

### 3. LangChain Pipeline
The experiment connects three components using the LangChain pipe operator:

- `ChatPromptTemplate` – Formats the prompt.
- `ChatGroq` – Generates the summary using the Groq model.
- `StrOutputParser` – Extracts the response as plain text.

### 4. Chain Execution
The chain is executed using `chain.invoke()` with the input data supplied through the `data` variable.

## Model Configuration
- Provider: Groq
- Model: Configured through the `MODEL` variable in the uploaded code
- Temperature: `0.2`

## API Key Configuration
The code retrieves `GROQ_API_KEY` using `userdata.get()`. Configure the key securely through Google Colab Secrets if using the Colab environment.

Never upload API keys or secret credentials to GitHub.

## How to Run
1. Open the experiment in Google Colab or your Python environment.
2. Configure the required Groq API key securely.
3. Set the model name in the `MODEL` variable.
4. Install the required dependencies.
5. Execute the prompt template and LangChain chain.
6. Review the generated RAG summary.

## Expected Learning Outcome
- Understand reusable prompt templates.
- Learn how LangChain chains connect multiple components.
- Understand the role of output parsers.
- Generate summaries using an LLM.
- Learn how to pass dynamic input into a prompt template.

## Output
The experiment generates a summary of the supplied RAG explanation, with an instruction to produce exactly 10 sentences.

Save an output screenshot in the `outputs/` directory.

## Conclusion
This experiment demonstrates how prompt templates and LangChain chains simplify LLM workflows by separating prompt construction, model execution, and output parsing into reusable components.