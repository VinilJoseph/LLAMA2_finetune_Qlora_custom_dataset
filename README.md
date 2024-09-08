# 🦙 Llama 2 Fine-Tuning for Medical Chat Application

This repository contains a fine-tuned version of the Llama 2 model, specifically designed for generating responses in medical-related queries. The model has been fine-tuned using a medical dataset to enhance its performance in understanding and generating relevant medical information.

## 📄 Project Overview

The **Llama 2 Fine-Tuning for Medical Chat** project aims to build an AI-powered assistant capable of answering general medical queries. The model can provide responses on various medical topics but is intended for informational purposes only and should not replace professional medical advice.

The project is implemented using **Hugging Face Transformers**, with a focus on fine-tuning the Llama 2 architecture to generate concise, informative, and medically relevant responses.

## 🚀 Features

- **Medical Expertise**: Fine-tuned on medical data to enhance the model's ability to understand and respond to health-related queries.
- **Interactive Chat Interface**: Built using **Streamlit** for easy interaction with the model.
- **Advanced NLP**: Leverages transformer-based architecture to deliver accurate and coherent responses.
- **Real-Time Text Generation**: The model processes user queries and generates real-time answers.

## 🧠 Model Information

- **Model**: [Llama 2](https://huggingface.co/meta-llama/Llama-2-7b)
- **Fine-tuning Method**: QLoRA (Quantized Low-Rank Adaptation)
- **Pre-trained Weights**: Meta’s Llama 2-7B model
- **Dataset**: Fine-tuned on a medical QA dataset (e.g., PubMed or similar datasets)
- **Training Platform**: Hugging Face

## ⚙️ Setup and Usage

To use the fine-tuned Llama 2 model, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/viniljpk/llama2-finetuned-medical-chat.git
cd llama2-finetuned-medical-chat
```

### 2. Install Dependencies

Ensure you have Python 3.7+ installed, then install the required dependencies:

```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit App

```bash
streamlit run app.py
```

### 4. Chat with the Model

Once the app is running, you can interact with the medical chatbot by typing in your queries and receiving real-time responses from the fine-tuned Llama 2 model.

## 📦 Model Loading

You can also load and interact with the fine-tuned model programmatically:

```python
from transformers import pipeline

# Load the fine-tuned Llama 2 model
pipe = pipeline("text-generation", model="viniljpk/llama2_finetuned_medical")

# Generate a response
response = pipe("What are the symptoms of diabetes?")
print(response[0]['generated_text'])
```

## 🎯 Model Performance

During fine-tuning, the model was evaluated on various performance metrics, including:

- **Accuracy**: Improved understanding of medical terminologies.
- **Relevance**: Contextual understanding and relevant information generation.
- **Conciseness**: Ability to provide brief and accurate answers.

## 🛠️ Technologies Used

- **Model**: Llama 2 by Meta
- **Fine-tuning**: QLoRA for parameter-efficient training
- **Frameworks**: Hugging Face Transformers, Streamlit for the user interface
- **Programming Languages**: Python

## 💡 Use Cases

This fine-tuned Llama 2 model can be used in various medical applications, such as:

- **Medical Chatbots**: Assisting users in getting general medical information.
- **Healthcare Support**: Providing relevant information on diseases, symptoms, treatments, etc.
- **Medical Education**: Assisting students and professionals in learning about medical topics.

## ⚠️ Disclaimer

This model is intended for educational and informational purposes only. It should **not** be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with a qualified healthcare provider for personalized medical guidance.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ✨ Acknowledgements

- **Meta AI** for developing the Llama 2 architecture.
- **Hugging Face** for providing an open-source ecosystem for NLP models.
- **PubMed** for providing an open medical dataset.
