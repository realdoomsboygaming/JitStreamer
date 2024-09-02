# SideJITServer Installation Guide

This guide will walk you through the process of installing and running SideJITServer on your host computer and iPhone.

# Computer Setup

## Prerequisites

-   Python 3.6 or higher
-   Git
-   Tailscale account

## General Steps

1. Install Tailscale on both your host computer and iPhone
2. Create and activate a Python virtual environment
3. Install SideJITServer
4. Run SideJITServer

Here's the documentation for your project with the requested structure:

### Linux/macOS Instructions

1. Install Tailscale

    - Visit the [Tailscale download page](https://tailscale.com/download)
    - Follow the instructions for your specific Linux distribution or macOS

2. Create and activate a virtual environment

    ```
    python3 -m venv sidejit_env
    source sidejit_env/bin/activate
    ```

3. Install SideJITServer

    ```
    pip install git+https://github.com/jawshoeadan/SideJITServer#egg=SideJITServer
    ```

4. Run SideJITServer
    ```
    sudo SideJITServer
    ```

### Windows Instructions

1. Install Tailscale

    - Visit the [Tailscale download page](https://tailscale.com/download)
    - Download and run the Windows installer

2. Create and activate a virtual environment

    ```
    python -m venv sidejit_env
    sidejit_env\Scripts\activate
    ```

3. Install SideJITServer

    ```
    pip install git+https://github.com/jawshoeadan/SideJITServer#egg=SideJITServer
    ```

4. Run SideJITServer (as administrator)
    - Open Command Prompt as administrator
    ```
    SideJITServer
    ```

## Phone Setup

1. Install Tailscale on your iPhone

    - Open the App Store on your iPhone
    - Search for "Tailscale"
    - Download and install the Tailscale app

2. Configure Tailscale
    - Open the Tailscale app
    - Follow the in-app instructions to connect to your Tailscale network
3. Install [this shortcut](https://www.icloud.com/shortcuts/ed312725980f4bbfab7e6fe939a470df) and follow the setup questions. After you connect both of your devices to Tailscale, you can view each device's IP address from the dashboard. Use the same pairing file you used to setup SideStore. If you don't know the UDID of your device, it is typically the file name of your pairing file

## Troubleshooting

If you encounter any issues during the installation or running of SideJITServer, please check the following:

1. Ensure Tailscale is properly installed and connected on both your host computer and iPhone.
2. Verify that you're using the correct version of Python (3.6 or higher).
3. Make sure your virtual environment is activated before installing and running SideJITServer.
4. If you get a "command not found" error, try using the full path to the SideJITServer executable.

For further assistance, please refer to the project's GitHub repository or reach out to the project maintainers.
