# my-cicd-app
Lets build a simple CI/CD pipeline using GitHub Actions to:

  1.  Build your app and run locally
    ![Screenshot from 2025-06-20 11-27-26](https://github.com/user-attachments/assets/3e0d1008-fba2-4a58-9921-0e32bf32a6da)

  2. Run test Tests your app automatically

   It runs your Python test file to make sure the app doesn’t crash or return wrong results.

   ✅ This helps you avoid bugs and mistakes before your app gets deployed.
  
 3. Builds a Docker image

   Your app is packaged into a Docker container — like a self-contained mini computer that has:

   Your app

   Python

   Flask

   Any libraries it needs

✅ This makes sure it runs exactly the same everywhere — your laptop, a server, or the cloud.

  4. Build and push a Docker image

      Your app’s Docker image gets uploaded there under your account:
   🔗 macaroniwdcheese/my-cicd-app:latest

  6. Trigger on main branch commits
   
  7. (Optional next step): Deploy it

   Once your image is in DockerHub, you can deploy it to a real server or cloud like:

   Azure

   AWS

   Google Cloud

   A Raspberry Pi

   Any Linux server with Docker

  8. Notify you on success/failure (via email or Slack)



