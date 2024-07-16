# Protocol Name SushiSwap
## Category: Defi Project 
## Smart Contract: SushiToken

## Function Analysis

The function I am focusing on is the `SushiToken::delegateBySig` function.

The Block Explorer Link: https://etherscan.io/token/0x6B3595068778DD592e39A122f4f5a5cF09C90fE2#code 

The `abi.encodePacked` is the method of scrutiny.

## Detailed Explanation of the function, its use of encoding and the impact on the SushiToken Contract

The function `SushiToken::delegateBySig` allows users to securely delegate voting and other rights using off-chain 
signatures. `abi.encodePacked` helps the function to pack data recieved from the `abi.encode` functions - used earlier in 
the `SushiToken::delegateBySig` function -  tightly without padding, which is a format required for some specific cryptographic
operations used for recovering the signer address from the signature. This helps the SushiSwap Protocol as all SushiToken holders have a secure and convenient way to delegate their voting rights to another account without interacting with the contract or revealing their **private key** as the hash gotten from the **Encoding** functions serves as a signature to carry out the transaction.

