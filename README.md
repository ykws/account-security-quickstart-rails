![Twilio Logo](./twilio_logo_red.png)
# Twilio Account Security Quickstart - Twilio Authy and Twilio Verify
> We are currently in the process of updating this sample template. If you are encountering any issues with the sample, please open an issue at [github.com/twilio-labs/code-exchange/issues](https://github.com/twilio-labs/code-exchange/issues) and we'll try to help you.

A simple Ruby on Rails implementation of a website that uses Twilio Authy Two-factor Authentication to protect all assets within a folder. Additionally, it shows a Twilio Verify Phone Verification implementation.

It uses four channels for delivery, SMS, Voice, Soft Tokens, and Push
Notifications. You should have the [Authy App](https://authy.com/download/)
installed to try Soft Token and Push Notification support.

This app uses [SQLite](https://www.sqlite.org/) as a data store. You will
have to install SQLite as well and make sure it is running.

Learn more about Account Security and when to use the Authy API vs the Verify API in the [Account Security documentation](https://www.twilio.com/docs/verify/authy-vs-verify).


#### Two-Factor Authentication Demo
- URL path "/protected" is protected with both user session and Twilio Authy Two-Factor Authentication
- One Time Passwords (SMS and Voice)
- SoftTokens
- Push Notifications (via polling)

#### Phone Verification
- Phone Verification
- SMS or Voice Call

### Setup
1. Clone this repo
   ```sh
   git clone https://github.com/TwilioDevEd/account-security-quickstart-rails.git
   cd account-security-quickstart-rails
   ```

1. Run `bundle install`

1. Register for a [Twilio Account](https://www.twilio.com/).

1. Setup an Account Security app via the [Twilio Console](https://twilio.com/console).

1. Create your `application.yml` file from the existing example in `config/application.example.yml`

   ```sh
   cp config/application.example.yml config/application.yml
   ```

1. Generate an Application **API KEY** from the Dashboard and paste it in `.env`

1. Check and make sure SQLite is up and running

1. Run `bin/rails db:migrate` to create the tables

1. Run `bin/rails server` to start the server

## Meta

* No warranty expressed or implied. Software is as is. Diggity.
* [MIT License](http://www.opensource.org/licenses/mit-license.html)
* Lovingly crafted by Twilio Developer Education.
