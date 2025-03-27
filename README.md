# Certificate Validation System using Blockchain

---

## 📌 Introduction

Welcome to the **Certificate Validation System**, a decentralized and secure solution for generating, storing, and verifying digital certificates using **Blockchain technology**. Traditional certificate validation methods are prone to forgery and require centralized authorities for verification. This project leverages **Ethereum Smart Contracts and IPFS (InterPlanetary File System)** to ensure certificates are **immutable, tamper-proof, and verifiable from anywhere in the world**.

### 🔍 How It Works
1. **Certificate Generation**: The institute generates certificates, which are then stored securely on **IPFS (via Pinata)**.
2. **Blockchain Storage**: The certificate details (such as UID, candidate name, course name, organization, and IPFS hash) are recorded on the Ethereum blockchain.
3. **Verification**: A verifier can authenticate certificates by either uploading the PDF or entering the certificate ID.

The system consists of two main roles:
- **Institute**: Responsible for generating, issuing, and managing certificates.
- **Verifier**: Can verify certificates using the blockchain and uploaded PDFs.

---

## 🚀 Features

- **Immutable Smart Contracts** – Certificates are stored on the **Ethereum blockchain**, preventing fraud.
- **Decentralized File Storage** – Uses **IPFS via Pinata** to store certificate PDFs securely.
- **Web Interface with Streamlit** – A user-friendly **Streamlit-powered UI** for managing certificates.
- **Firebase Authentication** – Ensures only authorized users can issue or verify certificates.
- **Tamper-Proof Validation** – Every certificate is cryptographically secured and easily verifiable.
- **Ganache Integration** – Simulates an Ethereum network for testing the smart contract locally.

---

## 📂 Getting Started

### 📥 Clone the Repository
```sh
git clone https://github.com/saranb565/BlockchainCertificateManagement.git
cd BlockchainCertificateManagement
```

### 🛠 Prerequisites
Ensure you have the following installed:

#### 1️⃣ Node.js (>= 16.0.0 recommended)
- Install Node.js from [Node.js official website](https://nodejs.org/)
```sh
node -v # To check Node.js version
```

#### 2️⃣ Python (>= 3.9.10 recommended)
- Install Python from [Python official website](https://www.python.org/)
```sh
python --version # To check Python version
```

#### 3️⃣ Truffle and Ganache-cli
```sh
npm install -g truffle
npm install -g ganache-cli
```

#### 4️⃣ Install Python Dependencies
```sh
pip install -r application/requirements.txt
```

> **Tip:** Use a **virtual environment** to avoid dependency issues:
```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r application/requirements.txt
```

---

## 🔐 Setting Up Firebase Authentication

1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project and navigate to **Authentication → Sign-in method**.
3. Enable **Email/Password authentication**.
4. Add a new web app in **Project Settings**.
5. Copy the following details into a `.env` file in the project's root directory:

```sh
FIREBASE_API_KEY = "<Your Firebase API Key>"
FIREBASE_AUTH_DOMAIN = "<Your Firebase Auth Domain>"
FIREBASE_DATABASE_URL = ""
FIREBASE_PROJECT_ID = "<Your Firebase Project ID>"
FIREBASE_STORAGE_BUCKET = "<Your Firebase Storage Bucket>"
FIREBASE_MESSAGING_SENDER_ID = "<Your Firebase Messaging Sender ID>"
FIREBASE_APP_ID = "<Your Firebase App ID>"
institute_email = "institute@gmail.com"
institute_password = "123456"
```

---

## 📦 IPFS and Pinata Setup

1. Sign up on [Pinata](https://app.pinata.cloud/).
2. Go to **API Keys** and generate a new key.
3. Add the following details to the `.env` file:

```sh
PINATA_API_KEY = "<Your Pinata API Key>"
PINATA_API_SECRET = "<Your Pinata Secret Key>"
```

---

## ⚡ Running the Project

### Step 1: Start Ganache (Ethereum Local Blockchain)
```sh
ganache-cli -h 127.0.0.1 -p 8545
```

### Step 2: Deploy Smart Contracts
```sh
truffle migrate
```

### Step 3: Launch the Streamlit App
```sh
cd application
streamlit run app.py
```

Now, open [localhost:8501](http://localhost:8501) in your browser to access the app! 🎉

---

## 📜 Usage Guide

### 📝 Generating a Certificate
1. Log in as an **Institute** using:
   - Email: `institute@gmail.com`
   - Password: `123456`
2. Enter the details of the candidate and course.
3. The certificate is generated, stored on **IPFS**, and its **hash** is recorded on the blockchain.

### 🔍 Verifying a Certificate
1. Upload the certificate PDF or enter the **Certificate ID**.
2. The system fetches the hash from the blockchain and compares it with the **IPFS** hash.
3. If the data matches, the certificate is **valid**!

---

## 🎯 Future Enhancements

- **QR Code Generation** – Embed blockchain transaction ID in the certificate.
- **Mobile App Integration** – A dedicated app for issuing and verifying certificates.
- **Layer 2 Scaling Solutions** – Reduce Ethereum gas fees using **Polygon or Optimism**.

---

## 🛠 Technologies Used

- **Frontend:** Streamlit (Python-based UI framework)
- **Backend:** Flask
- **Blockchain:** Ethereum (Ganache for local development)
- **Smart Contracts:** Solidity
- **Storage:** IPFS (via Pinata)
- **Authentication:** Firebase
- **Development Tools:** Truffle, Ganache-cli

---

## 🤝 Contribution Guidelines

Want to contribute? Follow these steps:

1. **Fork** the repo.
2. **Clone** it locally:
   ```sh
   git clone https://github.com/saranb565/BlockchainCertificateManagement.git
   ```
3. **Create a feature branch**:
   ```sh
   git checkout -b feature-new
   ```
4. **Make changes and commit**:
   ```sh
   git commit -m "Added new feature"
   ```
5. **Push and create a pull request**:
   ```sh
   git push origin feature-new
   ```

---

## 📧 Contact

For queries or suggestions, reach out at: **saranb565@gmail.com**

---

**⭐ Don't forget to star the repo if you found it useful! ⭐**

