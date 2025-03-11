# **Fuse Take-Home**
## **Subscription Management API with AI Recommendations**  

## **Requirements**  
Your task is to build a **Node.js REST API** for managing user subscriptions. The API should allow users to:  
- **Create and retrieve users**.  
- **Subscribe to plans, view, and cancel subscriptions**.  
- **Receive AI-powered subscription recommendations** based on their needs.  
- **Deploy the API** to a publicly accessible environment.  

---

## **Considerations**  
- **Keep the system simple**: The only required user information is `email`, `first_name`, and `last_name`.  
- **This exercise is intentionally open-ended** we encourage you to make architectural decisions and explain your reasoning in the README.
- **Deployment is required**, and the API must be publicly accessible.  
- **A security layer is required**, but the implementation is **up to the developer** (e.g., API keys, rate-limiting, JWT, or another mechanism).  
- **AI Integration Considerations**:  
  - The AI should **handle unclear prompts** gracefully (e.g., by asking for clarification instead of failing).  
  - You can **choose any AI provider with a free tier**, such as **OpenAI, Anthropic, or Hugging Face**.  

---

## **Deliverables**  
- A **production-ready application**, deployed and accessible via a public URL.  
- A **README.md** explaining your **architectural decisions** and **technology choices**.  
- The **source code** of the service in a private repository.  
- Add the following users as collaborators:  
  - `@skaznowiecki`  
  - `@sebastian-alvarez-fuse-finance`  
  - `@danielruizr`  
  - `@felipe-machado`  

---

## **API Endpoints**  

### **1. User Management**  
#### **Endpoints:**  
- `POST /users` → Create a new user  
- `GET /users/:id` → Retrieve a user by ID  

---

### **2. Subscription Plans**  
#### **Endpoints:**  
- `POST /plans` → Create a subscription plan  
- `GET /plans` → Retrieve all available plans  

---

### **3. User Subscriptions**  
#### **Endpoints:**  
- `POST /subscriptions` → Subscribe a user to a plan  
- `GET /users/:id/subscription` → Retrieve a user's current subscription  
- `POST /subscriptions/:id/cancel` → Cancel a user's subscription  

---

### **4. AI-Powered Subscription Recommendations**  
#### **Endpoints:**  
- `POST /subscriptions/ai-recommend` → Get an AI-powered subscription recommendation  

**Example Input:**  
```json
{
  "usage": "I need a plan for a small team with frequent video calls."
}
```

**Example AI Response:**  
```json
{
  "recommended_plan": "Business Plan",
  "reason": "You mentioned a small team and video calls, which align with the Business Plan's features."
}
```
