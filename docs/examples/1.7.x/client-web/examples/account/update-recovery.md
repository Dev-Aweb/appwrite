import { Client, Account } from "appwrite";

const client = new Client()
    .setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

const account = new Account(client);

const result = await account.updateRecovery(
    '<USER_ID>', // userId
    '<SECRET>', // secret
    '' // password
);

console.log(result);
