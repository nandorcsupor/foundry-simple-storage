# Run Anvil 
- anvil

# Run deploy script on local anvil chain
- forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545 --broadcast --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80

or forge create SimpleStorage --interactive

or since I'm using .env:
forge script script/DeploySimpleStorage.s.sol --rpc-url $RPC_URL --broadcast --private-key $PRIVATE_KEY

# Cast gas fee to normal value
cast --to-base 0x6b7e3 dec
cast --help for more

# Interact with a smart contract locally (call functions etc):

- cast send <contract_address> "store(uint256)" 123 --rpc-url $RPC_URL --private-key $PRIVATE_KEY


- cast call --help
- cast call <contract_address> "retrieve()"
    - cast value to normal: cast --to-base 0x00000000000007b dec

# Deploy to Sepolia
forge script script/DeploySimpleStorage.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $SEPOLIA_PRIVATE_KEY --broadcast

# Verify on Sepolia - manual way
- Deploy contract - say Verify and Publish, fill out stuff, optimization yes, paste code, publish.  --> Go back to contract and its more interactive!!

# Verify on Sepolia - programmatic way


# Format code
- forge fmt

# Create foundry project
- forge --init
# start local blockchain:
    - anvil







