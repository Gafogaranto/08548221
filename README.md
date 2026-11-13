# Voiceoftaade — MoneyPrinterTurbo Colab Launcher

This repository contains a Colab launcher for the Voiceoftaade AI Studio workflow.

## Open the notebook

[Open Voiceoftaade_MoneyPrinterTurbo_Colab.ipynb in Google Colab](https://colab.research.google.com/github/Gafogaranto/08548221/blob/main/Voiceoftaade_MoneyPrinterTurbo_Colab.ipynb)

## What it does

- Uses an existing MoneyPrinterTurbo installation in the current Colab runtime.
- Starts Streamlit on port 8501 if it is not already responding.
- Creates a temporary Cloudflare Quick Tunnel protected by an allowed email address.
- Leaves Streamlit's CORS and XSRF protections enabled.
- Does not use ngrok or require an ngrok token.

## Requirements

1. Run the installation/setup cell in the official [MoneyPrinterTurbo Colab notebook](https://colab.research.google.com/github/harry0703/MoneyPrinterTurbo/blob/main/docs/MoneyPrinterTurbo.ipynb).
2. Then run the launcher notebook above in the same Colab runtime, or ensure MoneyPrinterTurbo exists at `/content/MoneyPrinterTurbo`.
3. Enter the email address that should be permitted to access the dashboard when prompted. Cloudflare sends it a one-time PIN.

## Important

Cloudflare Quick Tunnels are temporary development tunnels. Anyone who can complete the email check for the allowed address may access the dashboard while the tunnel is active. Keep the URL private and stop the tunnel when finished. The URL changes when the tunnel is restarted. Colab runtimes are temporary.

See the [Cloudflare Quick Tunnel documentation](https://developers.cloudflare.com/tunnel/get-started/quick-tunnels/) for current limitations.
