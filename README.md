# Portfolio
Welcome to Ravikant Hudda's portfolio for know about me.

## Getting started
There are a few prerequisites that need to be installed in order to run Portfolio in a local environment

- [.NET 4.6.1 Framework](https://www.microsoft.com/en-us/download/details.aspx?id=49981) or newer.
- [Visual Studio](https://visualstudio.microsoft.com/).

We also recommend you install your favorite flavor of SQL Server database IDE.

If you are planning on testing against local data, you may download a copy of the database from [here] (#) (though migrations may need to be applied if develping against new functionality). If you are planning on connecting to a remote enviroment for database connections, you will more-than-likely need to use a VPN tunnel. Please contact your friendly TechOps staff for that.

A copy of the Portfolio may also come in handy when comparing client data vs. API data. See [this page] (#) for links to other downloads.

## Installing dependencies

You may install dependencies via Visual Studio (_Restore Nuget Packages_) or via Cake by running `./build.ps1 -target Build`, which will perform an install of all libraries.

You will need to add the credentials for the Hangfire Nuget repo in order to download its libraries. You can find the credentials for it [in this page](#). In order to run it locally, you can follow [this tutorial](#).

## Running the app

When running the app, you will be required to provide a bearer token for all your authenticated requests, as it will provide the client context under which operations will take place. To that effect, the first order of business after launching the application is to make a request to `https://localhost:{your_port}/token` with a payload.
