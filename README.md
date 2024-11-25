# Hello World Deployment with GitHub Actions to AWS EC2

This repository demonstrates how to host a simple "Hello World" webpage on an AWS EC2 instance. It also includes a GitHub Actions workflow to automatically deploy changes to the EC2 instance whenever code is pushed to the `main` branch.

---

## Project Structure

### Files and Folders
- `index.html`: The main HTML file containing the "Hello World" page.
- `.github/workflows/github-actions-ec2.yml`: The GitHub Actions workflow file to automate deployment.
- `README.md`: This documentation file.
- `sources/execution_video.mkv`: It´s a video demostration of the practice.

---

## Prerequisites

1. **AWS EC2 Instance**:
   - An EC2 instance with an appropriate Ubuntu-based OS.
   - SSH access enabled (using a private key).

2. **GitHub Secrets**:
   Add the following secrets in your repository:
   - `EC2_SSH_KEY`: Your private SSH key for accessing the EC2 instance.
   - `HOST_DNS`: The public DNS or IP of your EC2 instance.
   - `USERNAME`: The username for SSH (e.g., `ubuntu` for Ubuntu instances).
   - `TARGET_DIR`: The directory on the EC2 instance where files will be deployed (e.g., `/var/www/home`).

---

## How It Works

1. **Write Your HTML**:
   - Update the `index.html` file with your desired content. By default, it displays "Hello, World!".

2. **Push Changes**:
   - Push changes to the `main` branch. The workflow in `.github/workflows/github-actions-ec2.yml` will be triggered automatically.

3. **Deploy via GitHub Actions**:
   - The workflow connects to the EC2 instance via SSH and uploads the updated files.
   - The web server on the EC2 instance serves the updated content.

---

## Additional Information

  - An image of the execution is attached
    ![image](https://github.com/user-attachments/assets/ceba9751-2987-4d22-9c80-23d6fda94a14)

    
  - An video of the execution is attached
    [View video](sources/execution_video.mkv)
  
  
  - Watch the Tutorial Video

   Learn how to deploy your project to AWS EC2 by watching this video:

   [![Execution_Video](https://img.youtube.com/vi/OwbJuIfShNo/0.jpg)](https://www.youtube.com/watch?v=OwbJuIfShNo&ab_channel=AntonySebasti%C3%A1nP%C3%A9rezGaona)

   Click the image above or [watch the video here](https://www.youtube.com/watch?v=OwbJuIfShNo&ab_channel=AntonySebasti%C3%A1nP%C3%A9rezGaona).
