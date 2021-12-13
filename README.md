![android-chrome-192x192](https://user-images.githubusercontent.com/73549208/145884819-716fc1fc-0639-4f3c-98ca-c1989edf0ef0.png)
# MiniThorGodsHammer Verified Smart Contract On
https://ipfs.io/ipfs/QmcKCnKKagzZSwg2E7U4s2sHwyhFGjE7Npgw2Ch2Y7CJA3

MiniThorGodsHammer

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.2;

import "@openzeppelin/contracts@4.4.0/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@4.4.0/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts@4.4.0/token/ERC20/extensions/ERC20Snapshot.sol";
import "@openzeppelin/contracts@4.4.0/access/Ownable.sol";
import "@openzeppelin/contracts@4.4.0/security/Pausable.sol";
import "@openzeppelin/contracts@4.4.0/token/ERC20/extensions/draft-ERC20Permit.sol";
import "@openzeppelin/contracts@4.4.0/token/ERC20/extensions/ERC20FlashMint.sol";

contract MiniThorGodsHammer is ERC20, ERC20Burnable, ERC20Snapshot, Ownable, Pausable, ERC20Permit, ERC20FlashMint {
    constructor()
        ERC20("MiniThorGodsHammer", "MTGH")
        ERC20Permit("MiniThorGodsHammer")
    {
        _mint(msg.sender, 21000000000000000000000000000000000000000 * 10 ** decimals());
    }

    function snapshot() public onlyOwner {
        _snapshot();
    }

    function pause() public onlyOwner {
        _pause();
    }

    function unpause() public onlyOwner {
        _unpause();
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function _beforeTokenTransfer(address from, address to, uint256 amount)
        internal
        whenNotPaused
        override(ERC20, ERC20Snapshot)
    {
        super._beforeTokenTransfer(from, to, amount);
    }
}
