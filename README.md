# Voiceoftaade — MoneyPrinterTurbo Colab Launcher

This repository contains a self-contained Google Colab notebook for the Voiceoftaade AI Studio workflow.

## Open the notebook

[Open Voiceoftaade_MoneyPrinterTurbo_Colab.ipynb in Google Colab](https://colab.research.google.com/github/Gafogaranto/08548221/blob/main/Voiceoftaade_MoneyPrinterTurbo_Colab.ipynb)

## How to use it

1. Open the notebook in Google Colab.
2. Run **1. Install MoneyPrinterTurbo** and wait for installation to finish.
3. Run **2. Launch the protected dashboard**.
4. Enter the email address that should be allowed to access the dashboard when prompted.
5. Open the generated URL. Cloudflare will send that email a one-time PIN.

## What it does

- Installs MoneyPrinterTurbo in the current Colab runtime.
- Starts Streamlit on port 8501.
- Creates a temporary Cloudflare Quick Tunnel protected by an allowed email address.
- Leaves Streamlit's CORS and XSRF protections enabled.
- Does not use ngrok or require an ngrok token.

## Important

Cloudflare Quick Tunnels are temporary development tunnels, not production hosting. Keep the URL private and stop the tunnel when finished. The URL changes when the tunnel is restarted, and the Colab runtime is temporary.

See the [Cloudflare Quick Tunnel documentation](https://developers.cloudflare.com/tunnel/get-started/quick-tunnels/) for current limitations.
