import { Client, Functions } from "@appwrite.io/console";

const client = new Client()
    .setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

const functions = new Functions(client);

const result = await functions.createTemplateDeployment(
    '<FUNCTION_ID>', // functionId
    '<REPOSITORY>', // repository
    '<OWNER>', // owner
    '<ROOT_DIRECTORY>', // rootDirectory
    '<VERSION>', // version
    false // activate (optional)
);

console.log(result);
