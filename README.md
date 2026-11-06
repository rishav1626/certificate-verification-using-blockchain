# E-Certify – Blockchain-Based Certificate Verification System

E-Certify is a blockchain-based certification platform designed to make academic certificate issuance, storage, and verification more secure, transparent, and reliable. The system uses Ethereum smart contracts to manage certificate records and IPFS to store certificate documents in a decentralized manner.

The platform provides separate functionalities for students, educational institutions, and administrators, helping reduce certificate forgery and simplify the verification process.

## 🚀 Key Features

- **Blockchain-Based Certificate Management:** Uses Solidity smart contracts to maintain certificate records on the blockchain.
- **Student Registration:** Supports student registration and wallet-based identification.
- **Institute Management:** Allows authorized educational institutions to manage certificate-related operations.
- **Certificate Issuance:** Institutes can issue certificates to students through smart contract transactions.
- **Certificate Requests:** Students can submit certificate requests through the platform.
- **Decentralized Storage:** Certificate documents are uploaded to IPFS using Pinata, while their IPFS hashes are recorded on the blockchain.
- **Certificate Verification:** Users can verify certificates using their unique certificate IDs.
- **QR Code Scanning:** Supports QR-based certificate verification.
- **Certificate Revocation:** Authorized institutes can revoke previously issued certificates.
- **Wallet Integration:** Supports MetaMask for blockchain interactions and transaction signing.
- **Ownership Verification:** Includes wallet-based ownership proof for certificate holders.

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS |
| Backend | Node.js, Express.js |
| Blockchain | Ethereum, Solidity |
| Smart Contract Development | Hardhat |
| Blockchain Interaction | Ethers.js, Viem |
| Decentralized Storage | IPFS, Pinata |
| Authentication & Database | Firebase |
| Wallet | MetaMask |
| QR Code | HTML5 QR Code, QRCode React |

## 🏗️ System Architecture

The application follows a decentralized architecture:

1. **Frontend:** Provides interfaces for students, institutes, administrators, and certificate verification.
2. **Backend:** Handles document upload requests and communicates with the Pinata IPFS service.
3. **IPFS Storage:** Stores certificate documents and generates unique IPFS hashes.
4. **Smart Contracts:** Manage student and institute access, certificate issuance, approval, verification, and revocation.
5. **Blockchain Network:** Stores certificate metadata and transaction records for transparent verification.

## 📂 Project Structure

```text
blockchain-based-certification/
│
├── backend/
│   ├── server.js
│   └── package.json
│
├── contracts/
│   ├── AccessControl.sol
│   ├── Certificate.sol
│   ├── Institute.sol
│   ├── Student.sol
│   └── Interfaces/
│
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   ├── components/
│   │   ├── hooks/
│   │   └── lib/
│   └── package.json
│
├── scripts/
│   ├── deploy.ts
│   ├── registerInstitute.ts
│   └── registerStudent.ts
│
├── hardhat.config.ts
├── package.json
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/rishav1626/certificate-verification-using-blockchain.git
cd certificate-verification-using-blockchain
```

### 2. Install Dependencies

Install the root dependencies:

```bash
npm install
```

Install frontend dependencies:

```bash
cd frontend
npm install
```

Install backend dependencies:

```bash
cd ../backend
npm install
```

### 3. Configure Environment Variables

Create the required `.env` files and configure the following variables.

**Root `.env` (Hardhat / blockchain configuration):**

```env
SEPOLIA_RPC_URL=your_sepolia_rpc_url
PRIVATE_KEY=your_wallet_private_key
ETHERSCAN_API_KEY=your_etherscan_api_key
```

**Frontend `.env.local`:**

```env
NEXT_PUBLIC_ACCESS_CONTROL_ADDRESS=your_access_control_contract_address
NEXT_PUBLIC_CERTIFICATE_ADDRESS=your_certificate_contract_address
NEXT_PUBLIC_SEPOLIA_RPC_URL=your_sepolia_rpc_url

NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_firebase_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_firebase_app_id

NEXT_PUBLIC_BACKEND_URL=http://localhost:5000
NEXT_PUBLIC_ADMIN_ADDRESS=your_admin_wallet_address
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

**Backend `.env`:**

```env
PINATA_JWT=your_pinata_jwt
```

Never upload private keys, API secrets, or actual `.env` files to GitHub.

### 4. Run the Application

Start the frontend:

```bash
cd frontend
npm run dev
```

Start the backend in another terminal:

```bash
cd backend
npm start
```

Frontend: `http://localhost:3000`

Backend: `http://localhost:5000`

> Note: Blockchain interaction requires correctly deployed smart contracts, configured contract addresses, a compatible wallet/network, and the required Firebase and Pinata credentials.

## 🔐 Smart Contracts

The project includes the following Solidity contracts:

- **AccessControl.sol:** Manages authorized student and institute wallet addresses.
- **Certificate.sol:** Handles certificate requests, issuance, approval, verification, and revocation.
- **Student.sol:** Maintains student profile information.
- **Institute.sol:** Maintains institute profile information.

## 🎯 Project Objectives

- Reduce the risk of academic certificate forgery.
- Provide a transparent and tamper-resistant certificate record.
- Enable faster and more accessible certificate verification.
- Use decentralized storage for certificate documents.
- Improve trust between students, institutions, and certificate verifiers.

## 🔮 Future Scope

- Integration with more blockchain networks.
- Support for multiple educational institutions.
- Improved privacy and role-based access management.
- Bulk certificate issuance.
- Enhanced analytics and verification reports.

## 👨‍💻 Author

**Rishav Raj**

GitHub: [@rishav1626](https://github.com/rishav1626)

---

*Developed as an academic project exploring blockchain technology, smart contracts, decentralized storage, and secure digital credential verification.*
