# Tweet with Xero

![Tweet with Xero - Screenshot](TweetWithXero.png "Tweet with Xero - Screenshot")

Keep `master` branch working at all times. This is where the latest working
version of the app lives. When doing the live coding sessions, switch to the
appropriate `live-coding*` branch, which removes everything but app skeleton code.

Keep the `live-coding*` branches rebased off the latest `master` as follows:

    master <--- live-coding-front-ender <--- live-coding

## Projects

| Project                         | URL                                            | Script                      | Start Branch                  |
| ------------------------------- | ---------------------------------------------- | --------------------------- | ----------------------------- |
| Back-End (ASP.NET Core Web API) | http://localhost:5000/api/tweets?handle=wendys | [link](./BACKEND-STEPS.md)  | **`live-coding`**             |
| Front-End (React App)           | http://localhost:8080/                         | [link](./FRONTEND-STEPS.md) | **`live-coding-front-ender`** |

# Live-Coding Setup

A couple of days (at least) before the event do these steps:

1. **IMPORTANT:** make sure you're on the `master` branch.
1. [Apply for access](https://developer.twitter.com/en/apply-for-access) to the
   Twitter API. Select the **Standard API** access a.k.a. **Developer Account**.
   You will need a normal Twitter account if you don't already have one. Personal
   account is fine.
1. Create a placeholder app in your Twitter API Developer account. Take copies
   of these values and set as environment variables on your system:

   | Value               | Env Var                       |
   | ------------------- | ----------------------------- |
   | API Key             | `TWITTER_CONSUMER_KEY`        |
   | API Secret Key      | `TWITTER_CONSUMER_SECRET`     |
   | Access Token        | `TWITTER_ACCESS_TOKEN`        |
   | Access Token Secret | `TWITTER_ACCESS_TOKEN_SECRET` |

   ![Set up environment variables](env_vars.png "Set up environment variables")

1. Download and install the latest version of the [ASP.NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)
   for your system.
1. Make sure you have `npm` installed.

## Verify App

In a terminal run the following:

```bash
$ cd api/TopTweets
$ dotnet build
...
$ dotnet run
...
```

You should be able to hit the API now (use test URL listed in table above) and
get back JSON responses.

In a separate terminal run the following:

```bash
$ cd ui
$ npm install
...
$ npm start
...
```

The front-end site will pop-up and should display a list of Tweets from Wendys (see screenshot above).
Make sure there are no errors in the developer console.

## Prepare for Demo

1. Print out the scripts (easier than looking at screen) or just wing it.
1. Change to the `live-coding` or `live-coding-front-ender` branch and verify
   it works. Check API returns `200 OK` and front-end just prints "Tweet with Xero".
