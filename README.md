🎙️ AI Voice Assistant for Financial Operations

A proof-of-concept prototype demonstrating a secure, conversational AI assistant that allows users to perform core financial operations through natural voice commands. This project tackles the challenge of providing accessible, hands-free banking while ensuring robust security during transactions.

🌟 Key Features

The prototype simulates a fully functional voice banking flow, focusing on efficiency and security.

Balance Inquiry: Instant, real-time retrieval and verbal announcement of the user's primary account balance.

Example Command: "What is my balance?"

Fund Transfer & Dialogue Management: Handles multi-step transfers. The assistant prompts the user for missing information (amount, recipient) and maintains conversational context.

Example Flow: User says "Transfer money." Assistant asks: "How much?"

Transaction History: Provides a summary of recent account activities upon request.

Example Command: "View my last three transactions."

Secure Transaction Authorization: Implements a simulated Two-Factor Authentication (2FA) step. For high-value transactions (mocked at over ₹10,000), the system automatically triggers a PIN/OTP modal, ensuring secure execution.

🏗️ Simulated Architecture & Technology Stack

The prototype is built as a single-page application to demonstrate end-to-end functionality, simulating a modern microservices architecture using browser APIs and JavaScript.

Technology Stack

Component

Technology Used

Role

Frontend/UI

HTML5, Tailwind CSS

Responsive, modern banking interface design.

Speech Recognition (STT)

Browser Native SpeechRecognition API

Converts user voice to text transcript.

Speech Output (TTS)

Browser Native SpeechSynthesis API

Converts assistant response text to spoken audio.

AI/Logic

Vanilla JavaScript

Simulated NLU/Dialogue Manager and Mock Banking Logic.

Mock Database

JavaScript Objects/Arrays

Stores mock balance, transactions, and pin data.

Architecture Overview

The system follows a standard conversational AI flow:

Voice Input: Captured by the browser's STT API.

NLU Simulation: JavaScript logic processes the transcript using string matching to identify the Intent (goal) and extract Entities (variables like amount/recipient).

Dialogue Manager: Manages the multi-turn conversation (transactionState) until all data and security checks are complete.

Mock Banking API: Executes the final operation (e.g., updates the local balance) and returns the confirmation status.

🚀 How to Run the Prototype

Since this project is contained within a single HTML file, setup is minimal.

Clone the Repository: Download or clone the project files.

Open the File: Locate and open the index.html file in a modern web browser (Google Chrome or Microsoft Edge recommended for best Speech Recognition API support).

Start Interaction: Click the Microphone Button and speak your command.

Example Commands to Try:

"What is my balance?"

"Transfer five hundred rupees to Jane."

"Send ten thousand rupees to John." (This will trigger the PIN security modal.)

"View transactions history."

🔒 Security Focus

Security is paramount for financial operations. The prototype demonstrates compliance through:

Contextual Security: High-risk transactions trigger a mandatory PIN verification step, simulating MFA.

Data Isolation: All financial and transactional logic is separated from the UI logic (even in this single-file prototype, data handling is isolated in the script).

Real-World Standard: In a production environment, all communication would be secured with TLS/SSL, and sensitive data would be protected using hashing and AES-256 encryption.

🔗 Submission Details

Code Repository: https://github.com/souravguptacom/AI-Voice-Assistant-Prototype/blob/main/AI%20Final.html

Demo Video: https://www.youtube.com/watch?v=FTuVEzxLyMA
