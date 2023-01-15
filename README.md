# ethers-simple-storage-fcc
Requirements
git
You'll know you did it right if you can run git --version and you see a response like git version x.x.x
Nodejs
You'll know you've installed nodejs right if you can run:
node --version and get an ouput like: vx.x.x
Yarn instead of npm
You'll know you've installed yarn right if you can run:
yarn --version and get an output like: x.x.x
You might need to install it with npm
ganache
You'll know you did it right if you can run the application and see:
ganache
You can alternatively use ganache-cli or hardhat
Optional Gitpod
If you can't or don't want to run and install locally, you can work with this repo in Gitpod. If you do this, you can skip the clone this repo part.

Open in Gitpod

Setup
Clone this repo

git clone https://github.com/PatrickAlphaC/ethers-simple-storage
cd ethers-simple-storage
Then install dependencies

yarn
Note: You'll notice in our package.json we are using "solc": "0.8.7-fixed". Usually, you'll just be able to do "solc": "0.8.7" to get a specific version, but there was a bit of an issue with that one... You'll find out why we use 0.8.7

Typescript
If you like typescript, run git checkout typescript then run yarn

Usage
Run your ganache local chain, by hitting quickstart on your ganache application
Save the workspace. This way, next time you open ganache you can start the workspace you've created, otherwise you'll have to redo all the steps below.

Copy the RPC SERVER sting in your ganache CLI, and place it into your .env file similar to what's in .env.example.
ganache

.env Example:

RPC_URL=http://0.0.0.0:8545
Hit the key on one of the accounts, and copy the key you see and place it into your .env file, similar to what you see in .env.example.
ganache

ganache

.env Example:

PRIVATE_KEY=11ee3108a03081fe260ecdc106554d09d9d1209bcafd46942b10e02943effc4a

Compile your code
Run

yarn compile
You'll see files SimpleStorage_sol_SimpleStorage.abi and SimpleStorage_sol_SimpleStorage.bin be created.

Run your application
node deploy.js
For WSL users
Run
yarn add ganache
Change Server settings in Ganache
Settings > Server > Host Name

Change Host Name to vEthernet (WSL)

Run your application
node deploy.js
Deploying to a testnet
Make sure you have a metamask or other wallet, and export the private key.

IMPORTANT

USE A METAMASK THAT DOESNT HAVE ANY REAL FUNDS IN IT. Just in case you accidentally push your private key to a public place. I highly recommend you use a different metamask or wallet when developing.

Export your private key and place it in your .env file, as done above.

Go to Alchemy and create a new project on the testnet of choice (ie, Goerli)

Grab your URL associated with the testnet, and place it into your .env file.

Make sure you have testnet ETH in your account. You can get some here. You should get testnet ETH for the same testnet that you made a project in Alchemy (ie, Goerli)

Run

node deploy.js
