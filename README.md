# How to Add Authentication to .NET MAUI Apps

This repo is a .NET MAUI application that uses Okta for authentication. It uses Okta's redirect model to sign in and displays your profile information.

Please read [How to Add Authentication to .NET MAUI Apps][blog] to see how it was created.

**Prerequisites:**

* Windows 11 OS build 22000.1696
* [Visual Studio 2022 Version 17.4.5](https://visualstudio.microsoft.com/vs/)
* [.NET 7](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)
* [Okta CLI](https://cli.okta.com)
* [Okta](https://developer.okta.com/) 
  > Okta has Authentication and User Management APIs that reduce development time with instant-on, scalable user infrastructure.

----

* [Getting Started](#getting-started)
* [Links](#links)
* [Help](#help)
* [License](#license)

## Getting Started

Clone or download the sample. You can download the files as a zip file. To clone the repo follow the instructions below:

```bash
git clone https://github.com/oktadev/okta-net-maui-example.git
cd okta-net-maui-example
```

Open the project in Visual Studio 2022 and restore Nuget packages.

### Create an OIDC Application in Okta

Create a free developer account with the following command using the [Okta CLI](https://cli.okta.com):

```shell
okta register
```

If you already have a developer account, use `okta login` to integrate it with the Okta CLI. 
Create a client application in Okta with the following command:

```shell
okta apps create
```

You will be prompted to select the following options:
- Application name: okta-maui-sample-app
- Type of Application: **3: Native App (mobile)**
- Callback: `myapp://callback`
- Post Logout Redirect URI: `myapp://callback`

The application configuration will be printed in the terminal. You will see output like the following when it's finished:

```console
Okta application configuration:
Issuer:    https://{yourOktaDomain}/oauth2/default
Client ID: {yourClientID}
```

Replace all instances of {yourOktaDomain} and {yourClientID} in the project.

## Run the app

In Visual Studio 2022, start an Android emulator of your choice.

> Note: This sample **only** implements the Android platform. You can go ahead and add the bits corresponding to the platform you want to try.

## Help

Please post any questions as comments on the [blog post][blog], or visit our [Okta Developer Forums](https://devforum.okta.com/).

## License

Apache 2.0, see [LICENSE](LICENSE).

[blog]: https://developer.okta.com/blog/2023/06/21/net-maui-authentication
