1. The main difference between `safeTransferFrom` and `transferFrom` is that, the former checks if the `to` address is that of a contract, and if it is a contract, it checks if the contract has implemented the `onERC721Received` method. If not, it throws an error. Further, the `onERC721Receieved` method needs to return `IERC721Receiver.onERC721Received.selector`
2. Additionally, `safeTransferFrom` has two method signatures: `safeTransferFrom(address from, address to, uint256 tokenId, bytes4 memory data)` and `safeTransferFrom(address from, address to, uint256 tokenId)` whereas `transferFrom` has only one signature and that is `transferFrom(address from, address to, uint256 tokenId)`