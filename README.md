# Browser Traffic Inference Dataset

This repository contains AI-enhanced browser traffic classification datasets with detailed explanations.

## Files

### Browser/
- **train_inference.json** (84MB, 355,982 entries) - Training dataset with AI-generated explanations
- **test_inference.json** (9.3MB, 39,602 entries) - Test dataset with AI-generated explanations

## Dataset Features

- **AI-Enhanced Outputs**: Each entry contains detailed technical analysis explaining the traffic classification
- **Browser Types**: samsung_firefox_1000, samsung_chrome_1000, samsung_internet_1000, samsung_uc_1000, samsung_edge_1000
- **Format**: Standard instruction-input-output format for machine learning
- **Technical Details**: Includes TLS handshake analysis, packet size patterns, domain analysis, and protocol identification

## Usage

```python
import json

# Load training data
with open('Browser/train_inference.json', 'r') as f:
    train_data = json.load(f)

# Load test data  
with open('Browser/test_inference.json', 'r') as f:
    test_data = json.load(f)
```

## Data Format

Each entry contains:
- `instruction`: Task description
- `input`: Network traffic details (protocol, duration, packet sizes, TLS logs)
- `output`: AI-generated classification with detailed technical explanation

## Download Links

- [train_inference.json](https://raw.githubusercontent.com/fdcgh/browser-traffic-inference/main/Browser/train_inference.json)
- [test_inference.json](https://raw.githubusercontent.com/fdcgh/browser-traffic-inference/main/Browser/test_inference.json)
