# Network Traffic Inference Dataset

This repository contains AI-enhanced network traffic classification datasets with detailed explanations across multiple domains.

## Files

### Browser/
- **train_inference.json** (84MB, 355,982 entries) - Browser traffic training dataset with AI-generated explanations
- **test_inference.json** (9.3MB, 39,602 entries) - Browser traffic test dataset with AI-generated explanations

### VNAT/
- **train_inference.json** (806KB, 2,407 entries) - VPN/Non-VPN traffic training dataset with AI-generated explanations
- **test_inference.json** (91KB, 272 entries) - VPN/Non-VPN traffic test dataset with AI-generated explanations

### ISCX-VPN/
- **train_inference.json** (2.8MB, 8,662 entries) - ISCX VPN traffic training dataset with AI-generated explanations
- **test_inference.json** (318KB, 967 entries) - ISCX VPN traffic test dataset with AI-generated explanations

### DataCon-Proxy/
- **train_inference.json** (3.9MB, 19,997 entries) - DataCon Proxy traffic training dataset with AI-generated explanations
- **test_inference.json** (427KB, 2,227 entries) - DataCon Proxy traffic test dataset with AI-generated explanations

## Dataset Features

- **AI-Enhanced Outputs**: Each entry contains detailed technical analysis explaining the traffic classification
- **Multiple Domains**: 
  - **Browser Traffic**: samsung_firefox_1000, samsung_chrome_1000, samsung_internet_1000, samsung_uc_1000, samsung_edge_1000
  - **VPN/Non-VPN**: nonvpn_netflix, nonvpn_skype-chat, vpn_youtube, vpn_hangouts_audio, etc.
  - **Proxy Traffic**: Proxy 6, Proxy 10, etc.
- **Format**: Standard instruction-input-output format for machine learning
- **Technical Details**: Includes TLS handshake analysis, packet size patterns, domain analysis, and protocol identification

## Usage

```python
import json

# Load Browser traffic data
with open('Browser/train_inference.json', 'r') as f:
    browser_train = json.load(f)

# Load VNAT traffic data
with open('VNAT/train_inference.json', 'r') as f:
    vnat_train = json.load(f)

# Load ISCX-VPN traffic data
with open('ISCX-VPN/train_inference.json', 'r') as f:
    iscx_train = json.load(f)

# Load DataCon-Proxy traffic data
with open('DataCon-Proxy/train_inference.json', 'r') as f:
    proxy_train = json.load(f)
```

## Data Format

Each entry contains:
- `instruction`: Task description
- `input`: Network traffic details (protocol, duration, packet sizes, TLS logs)
- `output`: AI-generated classification with detailed technical explanation

## Download Links

### Browser Traffic
- [Browser/train_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/Browser/train_inference.json) (84MB)
- [Browser/test_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/Browser/test_inference.json) (9.3MB)

### VNAT Traffic
- [VNAT/train_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/VNAT/train_inference.json) (806KB)
- [VNAT/test_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/VNAT/test_inference.json) (91KB)

### ISCX-VPN Traffic
- [ISCX-VPN/train_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/ISCX-VPN/train_inference.json) (2.8MB)
- [ISCX-VPN/test_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/ISCX-VPN/test_inference.json) (318KB)

### DataCon-Proxy Traffic
- [DataCon-Proxy/train_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/DataCon-Proxy/train_inference.json) (3.9MB)
- [DataCon-Proxy/test_inference.json](https://raw.githubusercontent.com/fdcgh/dataset/main/DataCon-Proxy/test_inference.json) (427KB)
