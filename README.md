# Question Answering System with BERT

This repository demonstrates how to build a Question Answering (QA) system using a pre-trained BERT model from Hugging Face Transformers. The system can extract answers to user-defined questions based on a given context. The notebook includes step-by-step instructions for setting up the model, providing inputs, and evaluating its performance.

## Features
- **Pre-trained Model**: Uses `bert-large-uncased-whole-word-masking-finetuned-squad`, a BERT model fine-tuned on the SQuAD dataset.
- **Input Handling**: Allows custom questions and context as input.
- **Answer Extraction**: Predicts the answer's start and end positions in the context and converts it back into human-readable text.
- **Evaluation Metrics**:
  - **Exact Match (EM)**: Checks if the model's answer exactly matches the true answer.
  - **F1-Score**: Measures the balance between precision and recall for partial matches.

## Code Structure
1. **Loading the Model**:
   - Initializes the BERT model and tokenizer for QA tasks.
2. **Defining Inputs**:
   - Accepts a question and context to be processed by the model.
3. **Tokenization**:
   - Converts text into token IDs for compatibility with the BERT model.
4. **Prediction**:
   - Identifies the start and end positions of the answer in the context.
5. **Evaluation**:
   - Compares the predicted answer with the true answer using EM and F1-Score.

## Example Input
```python
question = "Who is the president of the United States?"
context = """
Joe Biden, the 46th president of the United States, assumed office on January 20, 2021, following his victory 
in the 2020 presidential election. Representing the Democratic Party, Biden has prioritized policies aimed at 
uniting a divided nation, addressing climate change, and strengthening the economy.
"""
