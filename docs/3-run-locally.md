# 👨🏻‍💻 Run from your local machine

Clone this repository locally or fork to your Github account. Run all of the the steps below from the "src" directory.

1. Make sure you deploy an instance of Cosmos DB in your Azure Subscription
2. Create a new file named `.env.local` to store the environment variables add the following variables.

**Please note:**

- Do not use double-quotes and do not delete any of the variables.
- Make sure that `NEXTAUTH_URL=http://localhost:3000` has no comments in the same line.

  ```
  # Azure OpenAI configuration
  AZURE_OPENAI_API_KEY=04a9797a0191463782d34af4ab49e3cd
  AZURE_OPENAI_API_INSTANCE_NAME=
  AZURE_OPENAI_API_DEPLOYMENT_NAME=azurechatgpt
  AZURE_OPENAI_API_VERSION=

  # GitHub OAuth app configuration
  AUTH_GITHUB_ID=
  AUTH_GITHUB_SECRET=

  # Azure AD OAuth app configuration
  AZURE_AD_CLIENT_ID=
  AZURE_AD_CLIENT_SECRET=
  AZURE_AD_TENANT_ID=d827fc60-9b28-4520-af06-b2d51904fa40

  # When deploying to production,
  # set the NEXTAUTH_URL environment variable to the canonical URL of your site.
  # More information: https://next-auth.js.org/configuration/options

  NEXTAUTH_SECRET=
  NEXTAUTH_URL=http://localhost:3000

  AZURE_COSMOSDB_URI=https://atworkazurechatgpt.documents.azure.com:443/
  AZURE_COSMOSDB_KEY=cEuTRfvsQYIWPkdCSDy3IyZ8OKCx6cpFgHtKYoKABIhrOYAWWysdAPar6BwseKlZQKA7EIJoIdWZACDbLSyxYg==
  ```

4. change the active directory to be `src`
5. Install npm packages by running `npm install`
6. Start the project by running `npm run dev`

You should now be prompted to login with your chosen OAuth provider. Once successfully logged in, you can start creating new conversations.

![](/images/chat-home.png)
![](/images/chat-history.png)

[Next](/docs/4-deployto-azure.md)
