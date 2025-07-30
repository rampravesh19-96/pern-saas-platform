# How to Setup & Run this Project

## 🛠️ Prerequisites

### ❖ Install Node.js (Skip if already installed)
1. Visit the official Node.js website.
2. Download the Node.js installer.
3. Run the installer and follow the setup instructions.

> **Note**: Always start the **Server** before running the **Client**.

---

## ⚙️ Server Setup

1. Open the project folder in **VS Code**.
2. Setup **Neon** (PostgreSQL hosting).
3. Create the required database table using the Neon SQL Editor with the following query:

```sql
CREATE TABLE creations (
  id SERIAL PRIMARY KEY,
  user_id TEXT NOT NULL,
  prompt TEXT NOT NULL,
  content TEXT NOT NULL,
  type TEXT NOT NULL,
  publish BOOLEAN DEFAULT FALSE,
  likes TEXT[] DEFAULT '{}',
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
);
