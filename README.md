# InterBlockCV

InterBlockCV is a blockchain-based platform that aims to achieve seamless resume sharing and data interoperability across different blockchain networks. It leverages the power of blockchain technology to provide a secure and decentralized solution for managing and sharing resumes.

## Features

- **Resume Sharing:** Users can securely upload and share their resumes on the InterBlockCV platform.
- **Blockchain Interoperability:** InterBlockCV allows for seamless resume data exchange between different blockchain networks, enabling users to access and verify resumes across multiple platforms.
- **Decentralized Storage:** Resumes and related data are stored on decentralized storage networks, ensuring data integrity and availability.
- **Data Privacy:** InterBlockCV prioritizes data privacy by implementing encryption and user-controlled access permissions.
- **Resume Verification:** Resumes can be verified using smart contract-based verification mechanisms, providing employers and recruiters with confidence in the authenticity of the shared resumes.
- **User-Friendly Interface:** The platform provides an intuitive and user-friendly interface for easy resume management and interaction.

## Installation Guide

*Clone the repository*

```
git clone https://github.com/Tejesh18/InterBlockCV.git
```

### Prerequisites for Hyperledger Fabric:

*Install docker:*

[Docker installation guide](https://docs.docker.com/engine/install/)

*Install Hyperledger Fabric 2.0 binaries:*
```
curl -sSL https://bit.ly/2ysbOFE | bash -s -- 2.0.0
```

*Install Go*

[Go installation guide](https://go.dev/dl/)

*Install npm and node.js:*

```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo apt-get install build-essential
```

*Install node dependencies from the package.json*

```
cd resume_chain/website
npm install
npm audit fix
```

### Prerequisites for Ethereum:

*Install truffle*
```
npm install truffle (If fails, try sudo install -g truffle)
```

*Install Ganache*

[Ganache installation guide](https://github.com/trufflesuite/ganache-ui/releases)   

*Set up Ganache*
 
 Create a new workplace and import resume_chain/eth/truffle/truffle-config.js
 
 ```
 cd resume_chain/eth/truffle

 truffle migrate
 ```
Copy the generated contract address and replace the contract address in resume_chain/website/employee.html and resume_chain/website/employer.html
```
var mycontract = new web3.eth.Contract(abi, <-replace your contract address here->);
```

### To run the code
```
cd resume_chain
./start_Network.sh
```

## Demostration

View employee page at: http://localhost:8000/employee

![employee page](employee_page.png)   

View employer page at: http://localhost:8000/employer

![employer page](employer_page.png)  

## Contact

For any inquiries or support, please contact the project maintainer: [Tejesh Annavarapu](tejeshannavarapu1804@gmail.com).

