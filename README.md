# 🚀 GitHub Copilot Hackathon Guide

## 🎯 Objective

Build a **fully functional application** using **GitHub Copilot features (including agents/custom agents)** to accelerate development across:

* Code generation
* UI creation
* Unit testing
* Automation testing
* Documentation

Choose between **2 challenges** in Python, Java, or Node.js.

---

## 13-Phase Workflow

1. Requirements → 2. Plan → 3. Instructions → 4. Prompts → 5. Chat Setup → 6-7. Agents → 8-10. Code/API/UI → 11-12. Tests → 13. Docs

---

## Expected Deliverables

- ✅ Source code in `/src`
- ✅ Tests ≥80% coverage in `/src/tests`
- ✅ Docs in `/docs` (API, User Guide, Technical)
- ✅ Working app (no errors)
- ✅ All tests passing

---

## Challenges

1. **Challenge 1**: Library Book Checkout System
2. **Challenge 2**: RESTful API

See challenge files for details.

---

## Repository Setup & Submission

### Step 1: Create Your GitHub Repository

1. Go to [GitHub.com](https://github.com) and log in to your account
2. Click **New** to create a repository
3. Name your repo: `HCL-Hackathon-Challenge-[YourName]` (e.g., `HCL-Hackathon-Challenge-JohnDoe`)
4. Add description: *"HCL Hackathon Challenge Solution - [Challenge 1/2]"*
5. Choose **Public** or **Private** (you will share access with us)
6. Click **Create repository**

### Step 2: Initialize Git & Push Code Locally

```bash
# Navigate to your project folder
cd your-project-folder

# Initialize git repository
git init

# Add all your generated code files
git add .

# Create initial commit
git commit -m "Initial commit: Generated code for HCL Hackathon Challenge"

# Add remote (replace with your GitHub repo URL)
git remote add origin https://github.com/YOUR-USERNAME/HCL-Hackathon-Challenge-YourName.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Repository Structure

Ensure your repository contains:

```
HCL-Hackathon-Challenge-YourName/
├── src/                          # All source code
│   ├── models/                   # Data models
│   ├── services/                 # Business logic
│   ├── controllers/               # API routes (if applicable)
│   └── tests/                     # Unit & integration tests
├── docs/                          # Documentation
│   ├── API.md                     # API endpoints & specifications
│   ├── USER_GUIDE.md             # How to use the application
│   ├── TECHNICAL.md              # Architecture & technical details
│   └── DATABASE_SCHEMA.md        # Database design (if applicable)
├── data/                          # Sample data
│   └── sample.json               # Test/seed data
├── README.md                      # Project overview
├── .gitignore                     # Git ignore rules
└── [Build config files]           # pom.xml, package.json, requirements.txt, etc.
```

### Step 4: Continuous Updates

After generating code with each phase, keep your repo updated:

```bash
# Make changes to your code
# ... modify files ...

# Stage and commit changes
git add .
git commit -m "Phase X: Add [description of what was implemented]"

# Push to GitHub
git push origin main
```
---

### If you aleady working on a project and want to push it to GitHub:
1. **Initialize Git in your project directory**:
   ```bash
    git init
   ```
2. **Add the remote repository**:
   ```bash
    git remote add origin https://github.com/your-username/your-repository.git
   ```
3. **Stage and commit your existing code**:
   ```bash
    git add .
    git commit -m "Initial commit with existing project"
   ```
4. **Rename the default branch to main** (if necessary):
   ```bash  
   git branch -M main
    ```
5. **Push your code to GitHub**:
   ```bash
   git push -u origin main
   ```
---

### 🧪 Evaluation Criteria

| Criteria              | Description                         |
| --------------------- | ----------------------------------- |
| ✅ Application Running | App should build & run successfully |
| ✅ Tests Passing       | Unit + automation tests must pass   |
| ✅ Error Handling      | Proper exception handling           |
| ✅ Documentation       | Present in `/docs`                  |
| ✅ Code Structure      | Clean `/src` organization           |
| ✅ README              | Well-structured and meaningful      |
| ✅ Copilot Usage       | Evidence of prompts / agents        |

---



### ⚠️ Important: Share Your Repository

After completing your challenge and pushing all code to GitHub:

1. **Ensure repository is accessible** (Public or invite us as collaborators)
2. **Share the repository URL** with: `[HCL Team/Submission Portal]`
3. **Include in submission**:
   - GitHub Repository URL
   - Your name and challenge number
   - Brief summary of implementation

---

**Use GitHub Copilot throughout. Quality > Speed.** 
