# 1Password Service Account Sandbox Container

This Dockerfile allows you to build a container image with the 1Password CLI installed. You can pass a service account token to the `OP_SERVICE_ACCOUNT_TOKEN` environment when you build the image, or set the value when you connect to the container.

⚠️ This is for sandbox and testing purposes only and should not be used with a Service Account that has access to any critical data. Ensure the token you use only accesses secrets suitable for your local/test environment and that you manage the confidentiality of that token accordingly.

## Learn more

* Learn more about the 1Password CLI: <https://developer.1password.com/docs/cli>
* Learn more about 1Password Service Accounts: <https://developer.1password.com/docs/service-accounts>
* Learn more about Secret References to remove plaintext secrets from your environment: <https://developer.1password.com/docs/cli/secret-references> 

## How to use this Dockerfile

* Generate an Service Account token using a demo 1Password account of your choosing.
* Update the Dockerfile to set the OP_SERVICE_ACCOUNT_TOKEN variable to your token.
* Build the image with `docker build -t <nameOfYourChoosing> .` in the same directory as the Dockerfile.
* Run the image and connect to the shell with `docker run -ti <nameYouChose>`.
* Check that your Service Account is correctly configured with `op user get --me`