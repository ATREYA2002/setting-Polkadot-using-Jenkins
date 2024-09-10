# **Setting up True Node PolkaDot**


## For Windows:
Installing WSL and Ubuntu: Begin with installing the Windows Subsystem for Linux (WSL) and Ubuntu on your system.
Downloading the Polkadot Binary: After that, ensure you have the latest Polkadot binary. Use this command, replacing VERSION with the latest version number:
curl -sL https://github.com/paritytech/polkadot/releases/download/*VERSION*/polkadot -o polkadot

Giving Executable Permission: Then, give the downloaded binary executable permissions with this command:
sudo chmod +x polkadot

Running the Polkadot node: Now, start your Polkadot node. Replace “Your Node’s Name” with the name you prefer for your node:
./target/release/Polkadot –name “Your Node’s Name”

Checking Your Node on Telemetry: Visit Telemetry to check out your newly launched node.
Installing Substrate: Substrate is a blockchain framework that Polkadot utilizes. The installation can be tricky on Windows, so using a virtual machine is recommended. Verify your installation by checking the version of cargo, a component of Substrate:
cargo –version

Cloning the Polkadot Repository and Building the Node: Use these commands to clone the Polkadot repository, navigate into the directory, initialize the build, and compile it:
git clone https://github.com/paritytech/polkadot Polkadot

cd Polkadot

./scripts/init.sh

cargo build –release

Running an Archive Node (optional): If you want to retain the full history of the blockchain state, you can run an archive node with this command:
./target/release/Polkadot –name “Your Node’s Name” –pruning archive

## For macOS:
Installing Homebrew: Open the terminal and enter this command to install Homebrew:
/bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)”

Installing Required Packages: Install OpenSSL, cmake, and llvm with this command:
brew install OpenSSL cmake llvm

Installing Rust: Now, you need to install Rust:
curl –proto ‘=https’ –tlsv1.2 -sSf https://sh.rustup.rs | sh

Cloning the Polkadot repository and Building the Node: Once Rust is installed, clone the Polkadot repository and build the node:
git clone GitHub – paritytech/Polkadot: Polkadot Node Implementation Polkadot

cd Polkadot

./scripts/init.sh

cargo build –release

Running the Node: Start your node using this command:
./target/release/Polkadot –name “Your Node’s Name”

Running an Archive Node (optional): If you wish, you can run an archive node:
./target/release/Polkadot –name “Your Node’s Name” –pruning archive

## For Linux:
Downloading the Polkadot Binary: Make sure you have the latest Polkadot binary. Download it with this command:
curl -sL https://github.com/paritytech/polkadot/releases/download/*VERSION*/polkadot -o polkadot

Giving Executable Permission: Then, give the downloaded binary executable permissions:
sudo chmod +x polkadot

Running the Polkadot Node: Now, start your Polkadot node:
./target/release/Polkadot –name “Your Node’s Name”

Checking Your Node on Telemetry: Visit Telemetry to check out your node.
Installing Substrate: Similar to Windows, install Substrate and verify the installation by checking the version of cargo:
cargo –version

Cloning the Polkadot Repository and Building the Node: Use these commands to clone the Polkadot repository and build the node:
git clone https://github.com/paritytech/polkadot Polkadot

cd Polkadot

./scripts/init.sh

cargo build –release

Running an Archive Node (optional): If desired, run an archive node:
./target/release/Polkadot –name “Your Node’s Name” –pruning archive
