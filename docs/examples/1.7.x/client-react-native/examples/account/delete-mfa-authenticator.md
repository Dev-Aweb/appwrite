import { Client, Account, AuthenticatorType } from "react-native-appwrite";

const client = new Client()
    .setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

const account = new Account(client);

const result = await account.deleteMfaAuthenticator(
    AuthenticatorType.Totp // type
);

console.log(result);
