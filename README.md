# imaplink


## Description

Hackathon project for sy 2019.

The main item is an email to chat link.

### Code in kawauso.bot package

Almost all of the bot-related code was generated by the Symphony script.
Minor changes were made to put classes in packages instead of the default package,
and to read from environment variables instead of hardcoded strings.

## Disclaimer
This project is unaffiliated with Symphony and is without warranty.

## Config

You will need a bot name, address and credential files. These can be obtained when signing up for the hackathon.

To test the bot, you will need a user's email address, active on the test pod (instance).

Prepare the `config.json` file and credential files. This should look something like:

    /usr/local/hackathon/sym2019/ourbotapp
    ├── config.json
    ├── certificates
    │   └── all_symphony_certs_truststore
    └── rsa
        ├── innovatebot_xxx_privatekey.pem
        └── innovatebot_xxx_publickey.pem

Set the environment variables:

    export SY_EMAIL=test.user@testemail.com
    export SY_CONFIG=/usr/local/hackathon/sym2019/ourbotapp/config.json 

## Building

Requires java and maven.

    cd imaplink 
    mvn clean package

This creates an uberjar in the `target` directory.

# Running

Run the jar file:

    cd target/
    java -jar imaplink-1.0-SNAPSHOT.jar

Then verify that the bot sent a test message to the test user.