# codebook-data-analysis-pure-python
“Pure Python project analyzing user data—data loading, cleaning, and recommendations using only core Python.”
## 📂 Project Structure
codebook-analysis-project/
│
├── data/
│ ├── codebook_data.json
│ ├── data.json
│ ├── data2.json
│ └── cleaned_data2.json
│
└── notebooks/
├── project.ipynb
├── project_data_cleaning.ipynb
├── People_you_may_know.ipynb
└── pages_you_might_like.ipynb


---

# 🚀 Project Overview

The project consists of **four major components**:

---

## 1️⃣ **Loading & Exploring the User Data**
Files involved:  
👉 `project.ipynb`  

Tasks completed:
- Loaded JSON files using pure Python (`open()`, `.read()`, `json.loads`)
- Verified data structure (users, IDs, interests, pages followed, connections)
- Detected missing or incorrectly formatted fields
- Extracted useful fields into Python lists/dictionaries

**Key Python Concepts Used:**  
file handling, loops, condition checking, dictionary access

---

## 2️⃣ **Cleaning & Structuring Data**
File:  
👉 `project_data_cleaning.ipynb`

Cleaning tasks completed:
- Removed duplicate entries  
- Fixed missing values or incorrect data types  
- Normalized lists (e.g., converting single values to lists)  
- Removed invalid or blank user profiles  
- Validated page lists and follower lists  
- Saved cleaned data into `cleaned_data2.json`

**Pure Python Concepts Used:**  
`try/except`, string operations, list/dict cleanup, writing JSON using `json.dump`

---

## 3️⃣ **People You May Know – Recommendation Algorithm**
File:  
👉 `People_you_may_know.ipynb`

### 🔍 Logic Implemented
Users with **mutual connections** are recommended to each other.

For each user:
1. Take their existing friend list  
2. Look at friends-of-friends  
3. Exclude:
   - Existing friends  
   - The user themself  
4. Count mutual connections  
5. Rank & recommend

**Example:**  
If User A is connected to B and C,  
and both B and C are connected to D →  
Then D becomes a strong recommendation for A.

**Pure Python Concepts Used:**  
sets, nested loops, dictionary lookups, sorting with custom keys

---

## 4️⃣ **Pages You Might Like – Recommendation Algorithm**
File:  
👉 `pages_you_might_like.ipynb`

### 🔍 Logic Implemented
Pages are recommended using **interest similarity + user behavior**.

For each user:
1. Extract interests  
2. Compare with interests of pages followed by similar users  
3. Count interest overlaps  
4. Recommend pages with highest similarity  
5. Exclude pages the user already follows

**Pure Python Concepts Used:**  
sets, similarity scoring, dictionary iteration, filtering, ranking

---

# 🛠 Technologies Used

| Feature | Technology |
|--------|------------|
| Language | **Python (Pure Core Python)** |
| Data Format | JSON |
| Development Environment | Jupyter Notebook |
| Libraries Allowed | `json` only |
| No Libraries | ❌ pandas • ❌ NumPy • ❌ sklearn |

---

# 📊 Sample Outputs

### ✔ Cleaned user structure example:
```json
{
  "user_id": "U102",
  "name": "Aditi",
  "age": 21,
  "connections": ["U101", "U108"],
  "pages_liked": ["P03", "P06"],
  "interests": ["python", "gaming", "web dev"]
}


#📘 What I Learned
How to think algorithmically without relying on big libraries
How to manually clean and validate real-world messy data
How to design simple recommendation systems using logic + Python
How to structure a project and maintain clean code
How to work with nested JSON and build custom data pipelines

#📎 How to Run This Project
1. Clone the repository
git clone <your-repo-link>

2. Open the project folder
cd codebook-analysis-project

3. Open notebooks
Use Jupyter Notebook:
jupyter notebook
Run these notebooks:
project.ipynb
project_data_cleaning.ipynb
People_you_may_know.ipynb
pages_you_might_like.ipynb

#🤝 Contributing

If you'd like to suggest improvements or spot bugs, feel free to open an issue or create a pull request.

#📬 Contact
If you'd like to discuss this project or collaborate:

GitHub: your-username
LinkedIn: your-link
