
# Simple Blockchain in Java

This project demonstrates a simple implementation of a blockchain in Java. Each block in the blockchain is linked by its hash, and the chain validates itself based on the hash values. This example includes a mining process based on a set difficulty, with a proof-of-work mechanism.

## Features

- **Blockchain Structure**: Blocks are linked via cryptographic hashes.
- **Proof-of-Work Mining**: Blocks are mined by solving a cryptographic puzzle based on the specified difficulty.
- **Chain Validation**: The blockchain can verify its integrity by ensuring each block's hash and previous hash match correctly.
- **JSON Representation**: Uses the Gson library to print the blockchain in JSON format.

## Files

1. **Chain.java**: Manages the blockchain's structure, adding blocks, mining them, and validating the chain.
2. **Block.java**: Defines the block structure, including hashing and mining functionality.
3. **StringUtil.java**: Contains utility methods, such as the SHA-256 hashing function.

## Prerequisites

- **Java Development Kit (JDK)**: Ensure JDK is installed to compile and run the Java files.
- **Gson Library**: This project requires the Gson library to convert the blockchain into JSON format.

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/alexsantelli/blockChain_Java.git
   cd blockChain_java
   ```

2. **Compile the Code**

   Use the following command to compile the Java files:

   ```bash
   javac -cp gson-2.8.8.jar:. *.java
   ```

   (Ensure `gson-2.8.8.jar` is in the project directory or specify the correct path.)

3. **Run the Blockchain**

   ```bash
   java -cp gson-2.8.8.jar:. Chain
   ```

   This will initialize the blockchain, add blocks, mine them, and display the blockchain in JSON format.

## Classes Overview

- **Chain**: Handles blockchain creation, adding and mining blocks, and validating chain integrity.
- **Block**: Represents each individual block, storing data, timestamp, and hash values. Includes methods for calculating hash and mining.
- **StringUtil**: Utility class for applying SHA-256 hashing to strings.

## How It Works

1. **Mining and Adding Blocks**: Blocks are added to the blockchain with a mining process to achieve a certain hash difficulty. The block's hash is recalculated until it meets the difficulty target.
2. **Chain Validation**: The `isChainValid()` method checks if each block's hash is correct and if each block links properly to the previous one.

## Example Usage

The example in `Chain.java` creates a simple blockchain with three blocks. Each block is mined based on a defined difficulty and then linked to the previous block.

