# Nexus-CLI-Node-Setup-Guide-By-Bindas-Trick

# 🚀 Nexus CLI Node Setup Guide

Set up and run a Nexus CLI node to earn points and contribute to the network.

---

## 📋 Requirements

| Resource | Minimum Specification |
|----------|------------------------|
| **CPU**  | 4 vCPU                 |
| **RAM**  | 8-10GB (for 1 node)      |
| **Disk** | 50 GB Storage          |
| **Server Location** | US-Based Server |

> ⚠️ To run **multiple CLI nodes**, you will need **more RAM**.

---

## ⚙️ Installation Steps

### 1. System Update & Install Dependencies

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install screen curl build-essential pkg-config libssl-dev git-all -y
sudo apt install protobuf-compiler -y
sudo apt update
```

---

### 2. Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

When prompted, press `1` to proceed with default installation.

Then run:

```bash
source $HOME/.cargo/env
```

---

### 3. Add Rust Target

```bash
rustup target add riscv32i-unknown-none-elf
```

---

### 4. Install & Start Screen

```bash
sudo apt install screen
screen -S nexus
```

---

### 5. Install Nexus CLI

```bash
curl https://cli.nexus.xyz/ | sh
```

Then apply changes to your shell:

```bash
source ~/.bashrc
```

---

## 🚀 Start Your Node

### 1. Get Your Node ID

- Go to [https://app.nexus.xyz/nodes](https://app.nexus.xyz/nodes)
- You need to use US vpn to access website for now 
- Click **Add Node** > **Add CLI Node**
- Copy your `node-id`

### 2. Start the Node

```bash
nexus-network start --node-id your-node-id
```

> 🔁 Replace `your-node-id` with the one you got from the website.

---

## 🧠 Run Multiple Nodes (Optional)

To run more than one node, use separate screens.

```bash
screen -S nexus2
nexus-network start --node-id your-second-node-id
```

---

## 💡 Notes

- Ensure your server meets the **CPU, RAM, and storage** requirements.
- US-based servers are preferred for network latency.
- Monitor your node performance and logs inside each screen session.

---

## 📞 Support and any query join our telegram channel ASAP - https://t.me/bindastrick
thanks
For help and community support, join the [Nexus Discord](https://discord.gg/nexusxyz)

---

## 🏆 Earn Rewards

Earn points by keeping your CLI nodes running 24/7. More RAM = More Nodes = More Points!
