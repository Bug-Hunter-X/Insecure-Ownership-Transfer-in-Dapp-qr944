# Insecure Ownership Transfer in Dapp

This repository demonstrates a common security vulnerability in decentralized applications (dApps) built using Solidity: insecure ownership transfer.

## The Vulnerability

The `transferOwnership` function in `insecureOwnershipTransfer.sol` lacks a check to ensure the caller has the authority to transfer ownership.  Any user can call this function, potentially leading to an unauthorized ownership change.

## The Solution

The `secureOwnershipTransfer.sol` file provides a secure implementation.  It adds a check to verify that only the current owner can transfer ownership.