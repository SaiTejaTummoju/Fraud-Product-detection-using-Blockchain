# Fraud Product Detection Using Blockchain and IPFS

## Overview
This project is a decentralized application that combines **blockchain technology** with **IPFS** (InterPlanetary File System) to create a robust fraud detection and product verification system. It ensures transparency, authenticity, and crowd-sourced verification of products.

## Features
1. **Blockchain System**:
   - Implements a custom blockchain with **Proof of Stake (PoS)**.
   - Stores IPFS hashes (CIDs) on the blockchain.
   - Penalizes fraudulent stakeholders.

2. **IPFS Integration**:
   - Uploads product metadata to IPFS for decentralized storage.
   - Retrieves and verifies metadata via IPFS CIDs.

3. **Deep Learning Validation**:
   - Validates product names and IDs using a pre-trained **TensorFlow** model.

4. **Database**:
   - Uses **MongoDB** to store product details, feedback, and reports.

5. **Flask Web Interface**:
   - User-friendly interface for manufacturers and consumers.
   - Routes for registration, login, adding products, and verification.

6. **Feedback and Reporting**:
   - Allows users to provide feedback and report counterfeit products.

## Prerequisites
1. **Python 3.x**
2. **MongoDB**
3. **IPFS**
4. Libraries:
   - Flask
   - TensorFlow
   - pymongo
   - cryptography
   - requests
   - pickle

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/SaiTejaTummoju/Fraud-Product-detection-using-Blockchain.git
   cd Fraud-Product-detection-using-Blockchain
   ```

2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Start MongoDB:
   ```bash
   mongod --dbpath /path/to/your/db
   ```

4. Start IPFS daemon:
   ```bash
   ipfs daemon
   ```

5. Place your TensorFlow model (`validation2.h5`) and tokenizer (`tokenizer2.pkl`) in the project directory.

6. Run the application:
   ```bash
   python code.py
   ```

## Usage
1. Open the application in your browser:
   ```
   http://127.0.0.1:1110
   ```

2. **Manufacturer Actions**:
   - Register via `/manufacturer_register`.
   - Login via `/manufacturer_login`.
   - Add products via `/add_product`.

3. **Consumer Actions**:
   - Verify products using `/verify_product`.
   - View feedback and report counterfeit products.

4. **Admin Actions**:
   - View the blockchain using `/list_blocks`.
   - Shutdown the server via `/shutdown`.

## Project Workflow
1. **Adding a Product**:
   - Manufacturer submits product details.
   - Metadata is uploaded to IPFS, and the CID is stored in MongoDB and the blockchain.
   - PoS selects a validator, and the block is added.

2. **Verifying a Product**:
   - Consumer enters the product ID.
   - The system retrieves the metadata from IPFS and verifies its authenticity.
   - Displays feedback and reports for transparency.

3. **Feedback and Reporting**:
   - Consumers can leave feedback or report counterfeit products.
   - Data is stored in MongoDB for reference.

## File Structure
- **code.py**: Main application script.
- **validation2.h5**: Pre-trained TensorFlow model.
- **tokenizer2.pkl**: Tokenizer for product name preprocessing.
- **requirements.txt**: Python dependencies.
##How to Run


## API Endpoints
- `/manufacturer_register`: Register a new manufacturer.
- `/manufacturer_login`: Login as a manufacturer.
- `/add_product`: Add a product to the blockchain.
- `/verify_product`: Verify product authenticity.
- `/list_blocks`: View the entire blockchain.
- `/leave_feedback`: Submit feedback for a product.
- `/report_product`: Report a product as counterfeit.

## Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License. See `LICENSE` for more details.

## Author
[SaiTeja Tummoju](https://github.com/SaiTejaTummoju)

