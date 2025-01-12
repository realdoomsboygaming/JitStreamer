# JitStreamer Installation Guide

This guide will walk you through the process of installing and running JitStreamer on your host computer and iPhone.

# Computer Setup

## Prerequisites

-   Python 3.10 or higher
-   Git
-   Tailscale account

## General Steps

1. Install Tailscale on both your host computer and iPhone
2. Create and activate a Python virtual environment
3. Install JitStreamer
4. Run JitStreamer

### Linux/macOS Instructions

1. Install Tailscale

    - Visit the [Tailscale download page](https://tailscale.com/download)
    - Follow the instructions for your specific Linux distribution or macOS

2. Create and activate a virtual environment

    ```
    python3 -m venv jitstreamer_env
    source jitstreamer_env/bin/activate
    ```

3. Install JitStreamer

    ```
    pip install git+https://github.com/jawshoeadan/JitStreamer#egg=JitStreamer
    ```

4. Run JitStreamer
    ```
    sudo JitStreamer
    ```

### Windows Instructions

1. Install Tailscale

    - Visit the [Tailscale download page](https://tailscale.com/download)
    - Download and run the Windows installer

2. Create and activate a virtual environment

    ```
    python -m venv jitstreamer_env
    jitstreamer_env\Scripts\activate
    ```

3. Install JitStreamer

    ```
    pip install git+https://github.com/jawshoeadan/JitStreamer#egg=JitStreamer
    ```

4. Run JitStreamer (as administrator)
    - Open Command Prompt as administrator
    ```
    JitStreamer
    ```

## Phone Setup

1. Install Tailscale on your iPhone

    - Open the App Store on your iPhone
    - Search for "Tailscale"
    - Download and install the Tailscale app

2. Configure Tailscale
    - Open the Tailscale app
    - Follow the in-app instructions to connect to your Tailscale network

3. Install [this shortcut](https://www.icloud.com/shortcuts/f34906a2792e4f4b81b639a6853af403) and follow the setup questions. After you connect both of your devices to Tailscale, you can view each device's IP address from the dashboard. Use the same pairing file you used to setup SideStore. If you don't know the UDID of your device, it is typically the file name of your pairing file
4. Before you can enable JIT, you have to run the shortcut, first sending pairing, then starting the tunnel, then refreshing devices. You only have to do all of these steps the first time. When restarting JitStreamer, it will try to connect to the last paired device again, so after restarting, you shouldn't have to run the shortcut.
5. To enable JIT on apps, go into the SideStore settings -> SideJitServer and manually set the server IP to be the IP of your server, include http:// and :8080 at the end

## Troubleshooting

If you encounter any issues during the installation or running of JitStreamer, please check the following:

1. Ensure Tailscale is properly installed and connected on both your host computer and iPhone.
2. Verify that you're using the correct version of Python (3.10 or higher).
3. Make sure your virtual environment is activated before installing and running JitStreamer.
4. If you get a "command not found" error, try using the full path to the JitStreamer executable.
5. In a web browser open http://server-ip:8080/ and you should see your device. If you don't, try running the shortcut with "refresh devices"
6. Try running clear tunnels then start tunnel again
