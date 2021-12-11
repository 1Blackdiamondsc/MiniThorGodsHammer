# MiniThorGodsHammer Verified Smart Contract On
https://ipfs.io/ipfs/QmcKCnKKagzZSwg2E7U4s2sHwyhFGjE7Npgw2Ch2Y7CJA3

MiniThorGodsHammer

Functions

constructor

No parameters

Returns:

No parameters

DOMAIN_SEPARATOR

See {IERC20Permit-DOMAIN_SEPARATOR}.

No parameters

Returns:

NameTypeDescriptionbytes32allowance

See {IERC20-allowance}.

NameTypeDescriptionowneraddressspenderaddress

Returns:

NameTypeDescriptionuint256approve

See {IERC20-approve}. Requirements: - `spender` cannot be the zero address.

NameTypeDescriptionspenderaddressamountuint256

Returns:

NameTypeDescriptionboolbalanceOf

See {IERC20-balanceOf}.

NameTypeDescriptionaccountaddress

Returns:

NameTypeDescriptionuint256balanceOfAt

Retrieves the balance of `account` at the time `snapshotId` was created.

NameTypeDescriptionaccountaddresssnapshotIduint256

Returns:

NameTypeDescriptionuint256burn

Destroys `amount` tokens from the caller. See {ERC20-_burn}.

NameTypeDescriptionamountuint256

Returns:

No parameters

burnFrom

Destroys `amount` tokens from `account`, deducting from the caller's allowance. See {ERC20-_burn} and {ERC20-allowance}. Requirements: - the caller must have allowance for ``accounts``'s tokens of at least `amount`.

NameTypeDescriptionaccountaddressamountuint256

Returns:

No parameters

decimals

Returns the number of decimals used to get its user representation. For example, if `decimals` equals `2`, a balance of `505` tokens should be displayed to a user as `5.05` (`505 / 10 ** 2`). Tokens usually opt for a value of 18, imitating the relationship between Ether and Wei. This is the value {ERC20} uses, unless this function is overridden; NOTE: This information is only used for _display_ purposes: it in no way affects any of the arithmetic of the contract, including {IERC20-balanceOf} and {IERC20-transfer}.

No parameters

Returns:

NameTypeDescriptionuint8decreaseAllowance

Atomically decreases the allowance granted to `spender` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - `spender` cannot be the zero address. - `spender` must have allowance for the caller of at least `subtractedValue`.

NameTypeDescriptionspenderaddresssubtractedValueuint256

Returns:

NameTypeDescriptionboolflashFee

Returns the fee applied when doing flash loans. By default this implementation has 0 fees. This function can be overloaded to make the flash loan mechanism deflationary.

NameTypeDescriptiontokenaddressThe token to be flash loaned.amountuint256The amount of tokens to be loaned.

Returns:

NameTypeDescriptionuint256flashLoan

Performs a flash loan. New tokens are minted and sent to the `receiver`, who is required to implement the {IERC3156FlashBorrower} interface. By the end of the flash loan, the receiver is expected to own amount + fee tokens and have them approved back to the token contract itself so they can be burned.

NameTypeDescriptionreceiveraddressThe receiver of the flash loan. Should implement the {IERC3156FlashBorrower.onFlashLoan} interface.tokenaddressThe token to be flash loaned. Only `address(this)` is supported.amountuint256The amount of tokens to be loaned.databytesAn arbitrary datafield that is passed to the receiver.

Returns:

NameTypeDescriptionboolincreaseAllowance

Atomically increases the allowance granted to `spender` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - `spender` cannot be the zero address.

NameTypeDescriptionspenderaddressaddedValueuint256

Returns:

NameTypeDescriptionboolmaxFlashLoan

Returns the maximum amount of tokens available for loan.

NameTypeDescriptiontokenaddressThe address of the token that is requested.

Returns:

NameTypeDescriptionuint256mint

**Add Documentation for the method here**

NameTypeDescriptiontoaddressamountuint256

Returns:

No parameters

name

Returns the name of the token.

No parameters

Returns:

NameTypeDescriptionstringnonces

See {IERC20Permit-nonces}.

NameTypeDescriptionowneraddress

Returns:

NameTypeDescriptionuint256
