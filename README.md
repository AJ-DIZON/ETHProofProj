# ETHProofProj

This is a simple program that burns and mint NFTS.

## Description

This program allows the user to mint and burn NFTs. This is a project for MetaCrafters

## Getting Started

### Executing program

First download project_2.sol.
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Next, upload the file you downloaded into the website and compile. Once compiled, you can deploy the contract and start minting and burning NFTs

```
contract MyToken {

    // public variables here
    string public token_name = "Project-FT";
    string public token_abv = "P-UT";
    uint public total = 100;

    bool public b_check = true;
    // mapping variable here

    mapping(address => uint) balance;

    // mint function
    function minting(address minter, uint val) external
    {
       total += val;
       balance[minter] += val;
    }
    // burn function

    function burning(address minter, uint val) external
    {
        if(balance[minter] >= val)
        {
            balance[minter] -= val;
            total -= val;
            b_check = true;
        }else{
            b_check = false;
        }    
    }
}
```
## Authors
Albert Josh B. Dizon
