

# 📘 Advanced Git Workflow & Version Control Assignment

## 🎯 Objective

This project demonstrates advanced Git concepts used in real-world development:

* Git branching strategy
* Merge vs Rebase workflow
* Commit history management
* Interactive rebase (squash & reword)

---

## 📁 Repository Structure

advanced-git-workflow-assignment/
├── README.md
├── src/
└── screenshots/

---

## 🌿 Branches Used

* main → Production-ready code
* develop → Integration branch
* feature/login
* feature/payment
* feature/profile
* bugfix/login-error

---

## 🛠️ Commands Used

### 🔹 Repository Initialization

git init
git branch -M main
git checkout -b develop
git checkout -b feature/login

---

### 🔹 Feature Branch Example

git checkout -b feature/payment
mkdir src
echo "Payment feature v1" > src/payment.txt
git add .
git commit -m "feat(payment): add payment module"

---

### 🔹 Merge Strategy

git checkout develop
git merge --no-ff feature/payment -m "merge: integrate feature/payment"

---

### 🔹 Rebase Strategy

git checkout feature/profile
git rebase develop
git checkout develop
git merge feature/profile

---

### 🔹 Bugfix Branch

git checkout -b bugfix/login-error
echo "Fix login error" >> src/login.txt
git add .
git commit -m "fix(login): resolve login error"
git checkout develop
git merge --no-ff bugfix/login-error

---

### 🔹 Interactive Rebase (Squash & Reword)

git rebase -i HEAD~5

Example:

reword commit1 feat(login): add login UI
squash commit2 feat(login): add email validation
squash commit3 feat(login): add password validation
squash commit4 feat(login): add remember me
pick commit5 feat(login): add submit handler

---

## 📊 Merge vs Rebase

### 🔹 Merge

* Combines histories of two branches
* Creates a merge commit
* Preserves full branch history

Example:
git merge --no-ff feature/payment

---

### 🔹 Rebase

* Moves commits on top of another branch
* Creates a clean, linear history
* Rewrites commit history

Example:
git rebase develop

---

### 🔸 Key Difference

Merge:

* Keeps history structure
* Adds merge commit

Rebase:

* Creates linear history
* No extra commit

---

## ✂️ Squash & Reword

### 🔹 Squash

* Combines multiple commits into one
* Cleans messy commit history

### 🔹 Reword

* Edits commit message
* Improves readability and professionalism

---

## 📸 Screenshots
branch
<img width="1920" height="1080" alt="branch" src="https://github.com/user-attachments/assets/e8d0819b-8596-443b-b48a-f1dbb0789821" />

before merge

<img width="744" height="598" alt="beforemerge" src="https://github.com/user-attachments/assets/c3877a86-c795-470e-9b20-74b22e0b84af" />

after merge

<img width="739" height="599" alt="aftermerge" src="https://github.com/user-attachments/assets/7b8dd548-bb57-47cc-a60c-b9f235e08685" />

before rebase

<img width="745" height="600" alt="beforerebase" src="https://github.com/user-attachments/assets/96cf565d-61a0-4b89-94fa-9b9a08bdef48" />

afterrebase

<img width="724" height="557" alt="afterrebase" src="https://github.com/user-attachments/assets/572c2e84-fc09-49dc-9af5-ef66b5eff202" />

befor emerge bugfix

<img width="739" height="604" alt="beforemergebugfix" src="https://github.com/user-attachments/assets/b1d58365-c42a-45d4-a871-5328bdf8b8e8" />

after merge bugfix

<img width="739" height="597" alt="aftermergebugfix" src="https://github.com/user-attachments/assets/a2542a2c-eea7-4b81-bf1e-5d043214c691" />

marge main

<img width="742" height="598" alt="margetomain" src="https://github.com/user-attachments/assets/3006783f-46eb-41dc-8371-0b7d7f7fdc9b" />

Before interactive rebaseon featurelogin

<img width="714" height="594" alt="Beforeinteractiverebaseonfeaturelogin" src="https://github.com/user-attachments/assets/5760deb4-cce8-4b64-8015-26cde0a71951" />

After rebase completes

<img width="743" height="594" alt="Afterrebasecompletes" src="https://github.com/user-attachments/assets/632263ae-e807-47df-aa99-898fa0768de4" />





















---

## 🔄 Workflow Summary

1. Created develop from main
2. Built features in separate branches
3. Integrated:

   * feature/payment using merge
   * feature/profile using rebase
4. Fixed bugs using bugfix/login-error
5. Cleaned history using interactive rebase
6. Merged develop into main

---


---

## 🔗 GitHub Repository

(https://github.com/nuhu78/advanced-git-workflow-assignment.git)

