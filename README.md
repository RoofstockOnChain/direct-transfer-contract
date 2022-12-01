# Direct Transfer Contract
This smart contract is used to transfer any ERC720 or ERC721 token from the current owner to a new owner and the new owner will have to approve the request

## Prerequisites
- In order to initiate a transfer the current smart contract address should be set as an approved address for the token being transfered.

## Functions
#### initiateTransfer
- This is called by the owner of the token that is being transfered
- This function call requires that the token is an ERC721 or ERC720 - or that it has all of the following call(s):
    - ownerOf(tokenId)
    
#### approveTransfer
- This is called by new owner of the token to accept the transfer
- This function call requires that the token is an ERC721 or ERC720 - or that it has all of the following call(s):
    - safeTransferFrom(fromAddress, toAddress, tokenId)