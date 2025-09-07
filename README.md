# EX-4: Scenario-Based Report Development Utilizing Diverse Prompting Techniques

## Objective
The goal of this experiment is to design and develop an AI-powered chatbot that can handle customer inquiries, provide support, and improve customer experience in a retail environment. Create prompts using various AI prompting techniques to guide your experiment, data collection, analysis, and report creation.

---

## Aim
To implement a retail customer support chatbot using AI prompting techniques (Zero-Shot, Few-Shot, Chain-of-Thought, Instruction Fine-Tuning, and Contextual Prompting) and evaluate its performance on accuracy, response time, and user satisfaction.

---

## Algorithm

**Step 1: Data Collection**  
- Collect historical customer queries from retail chat logs.  
- Generate synthetic queries covering different scenarios (returns, tracking, recommendations, troubleshooting).

**Step 2: Data Preprocessing**  
- Normalize text (lowercase, punctuation removal).  
- Remove duplicates.  
- Categorize queries into different types.

**Step 3: Prompt Engineering**  
- **Zero-Shot:** Direct instruction to model.  
- **Few-Shot:** Provide 2–5 examples in the prompt.  
- **Chain-of-Thought:** Ask model to reason step-by-step.  
- **Instruction Fine-Tuning:** Train the model on curated query-response pairs.  
- **Contextual Prompting:** Include conversation history for multi-turn queries.

**Step 4: Chatbot Implementation**  
- Use Python & Flask to build backend.  
- Connect to OpenAI GPT API for generating responses.  
- Store conversation history in SQLite.

**Step 5: Testing & Evaluation**  
- Send sample queries for each scenario.  
- Record responses and compute metrics: accuracy, response time, user satisfaction.  
- Collect survey feedback from users.

**Step 6: Analysis & Reporting**  
- Compare performance across prompting techniques.  
- Visualize results with graphs and tables.  
- Draw conclusions and suggest improvements.

---

## Prompt Examples

**Zero-Shot:**  
Answer as a customer support agent: "How do I return a product I bought online?"

makefile
Copy code

**Few-Shot:**  
Q: How do I track my order?
A: Enter your order ID on the tracking page.

Q: How do I return an item?
A: Visit the returns page and submit the return form.

Q: How do I cancel an order?
A:

makefile
Copy code

**Chain-of-Thought:**  
Step 1: Check the order number.
Step 2: Visit the Returns Center.
Step 3: Upload product images if defective.
Step 4: Fill out and submit the return form.
Step 5: Wait for confirmation.

markdown
Copy code

**Contextual Prompting:**  
User: Where is my order #1234?
Bot: In transit.
User: When will it arrive?
Bot:

pgsql
Copy code

---

## Output

| Prompt Type               | Sample Query                         | AI Response Example                                                     |
|---------------------------|-------------------------------------|------------------------------------------------------------------------|
| Zero-Shot                 | "How do I return a product?"         | "Visit the Returns Center, fill out the return form, and follow instructions." |
| Few-Shot                  | "How do I cancel my order?"          | "Go to 'My Orders', select the order, and click 'Cancel'."             |
| Chain-of-Thought          | "I received a defective item."       | "1. Check the order number. 2. Visit Returns Center. 3. Upload images. 4. Submit form." |
| Contextual Prompting      | "When will my order #1234 arrive?"  | "Your order #1234 is expected to arrive by Sept 10."                   |

**Notes:**  
- Accuracy varies by prompting method.  
- Few-Shot and Instruction Fine-Tuning generally provide the highest accuracy.  
- Contextual prompting is ideal for multi-turn conversations.  
