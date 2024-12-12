sudo apt update
sudo apt upgrade -y
sudo apt install build-essential curl unzip git protobuf-compiler -y# nexus
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup install stable
rustup default stable
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup --version
cargo --version
rustup install stable
rustup default stable
sudo apt remove protobuf-compiler -y
wget https://github.com/protocolbuffers/protobuf/releases/download/v21.12/protoc-21.12-linux-x86_64.zip
unzip protoc-21.12-linux-x86_64.zip -d $HOME/.local
export PATH="$HOME/.local/bin:$PATH"
git clone https://github.com/nexus-xyz/nexus-zkvm.git
cd nexus-zkvm
cd /home/codespace/.nexus/network-api/clients/cli
cargo build --release
curl https://cli.nexus.xyz | sh
