# ShopAssist AI: GenAI-Based Shopping Assistant

## 1. Background

In the digital era, online shopping has become the default method for most consumers. However, the experience can often be overwhelming due to the sheer volume of options and the absence of personalized guidance.  
**ShopAssist AI** addresses this gap by combining the power of **large language models (LLMs)** and **rule-based logic** to provide reliable, accurate, and tailored laptop recommendations.

---

## 2. Problem Statement

Build a conversational chatbot that parses a structured dataset of laptops and provides personalized recommendations based on user requirements (e.g., budget, screen size, usage needs, etc.).

---

## 3. Approach

1. **Conversational Interaction**  
   The chatbot initiates a dialogue to gather the user's preferences in natural language.

2. **Information Extraction**  
   Extracts key user requirements and filters the top 3 laptops using rule-based logic.

3. **Recommendation Dialogue**  
   Engages further to refine choices and deliver a personalized recommendation.

---

## 4. System Functionalities

- **User Interface**:  
  Clean web-based interface for user interaction.

- **Conversational AI**:  
  Uses OpenAI's Chat API to process and respond.

- **Moderation**:  
  Inputs are moderated using OpenAI's Moderation API.

- **User Profile Extraction**:  
  Extracts structured user preferences (budget, specs, etc.) using OpenAI Function Calling.

> 💡 Uses `laptop_data.csv` containing detailed specs and descriptions to support natural language processing for recommendation logic.

---

## 5. System Architecture

- **Frontend**: Web interface for interaction.
- **Backend**: Flask-based server handling:
  - OpenAI API calls
  - Laptop data comparisons
  - Recommendation logic

---

## 6. Implementation Details

### 🔧 Flask Functional Highlights

- **Routing**: Directs user requests.
- **Conversation Management**: Initializes and manages session state.
- **Moderation**: Ensures safe dialogue.
- **Profile Extraction**: Parses requirements into JSON format.
- **Recommendation Logic**: Matches profile to top 3 laptops.

### 🧠 Major Functions

| Function | Purpose |
|----------|---------|
| `initialize_conversation()` | Start session with system instructions |
| `get_chat_completions()` | Generate response using OpenAI chat model |
| `moderation_check()` | Ensure safe content |
| `intent_confirmation_layer()` | Validate captured intent |
| `dictionary_present()` | Confirm proper JSON structure |
| `compare_laptops_with_user()` | Return top 3 matching laptops |
| `initialize_conv_reco()` | Start recommendation dialogue |

---

## 7. Prerequisites

- Python 3.7+
- OpenAI API Key (saved in `OpenAI_API_Key.txt`)

---
