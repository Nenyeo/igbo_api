# Firebase Configuration Guide

This project relies on Firebase Cloud Functions to execute the Igbo API business logic.

Individual contributors need to integrate their own Firebase project config to be able to run the project locally and merge forked changes.

## Step 1: Create a Firebase Project

Please follow this [Firebase Getting Started Guide](https://firebase.google.com/docs/web/setup) to create your own Firebase project.

## Step 2: Replace the `default` Firebase Project Name

Within [.firebaserc](https://github.com/nkowaokwu/igbo_api/blob/master/.firebaserc), replace the project name `igbo-api-bb22d` with your new Firebase project name

## Step 3: Replace the Firebase Config file

Within [firebase.js](https://github.com/nkowaokwu/igbo_api/blob/master/src/services/firebase.js#L5-L13), replace the `FIREBASE_CONFIG` object with your firebase project config object

## Step 4: Merging forked changes into main repo

Congrats 🎉 You have a change you want to merge into the main repo. You will need to complete a few extra steps to ensure your branch builds pass.

1. In your terminal, run `firebase login`. After following the instructions on screen, you will see a token pasted in your terminal. Save this for later
2. Navigate to the "Settings" tab at the top of your forked repo on GitHub
3. In the sidebar, click on the "Secrets and variables" dropdown
4. Select "Actions"
5. Click the green "New repository secret" button
6. Create a new variable with the name `FIREBASE_TOKEN`
7. Paste in the token you received from running `firebase login`
8. Click the green "Add secret" button
9. Submit your PR to get reviewed and merged 🚀