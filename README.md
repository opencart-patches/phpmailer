# OpenCart Patch PHPMailer

Override system/library/mail with PHPMailer

## Install on Opencart

> composer require opencart-patches/phpmailer

## Development Setup

 1. Clone the git repository
 2. Copy the `.env.sample` file to `.env` and set the configuration parameters respectively
 3. Run `bin/robo opencart:setup` and afterwards `bin/robo opencart:run` on command line (`bin/robo opencart:run &` to run in background)
 4. Run `bin/robo project:deploy` to mirror src/ into www/
 5. Open `http://localhost:8000` in your browser

## Testing

 - Install Mailcatcher (https://mailcatcher.me/) and run the service locally
 - Configure Opencart SMTP settings accordingly
    - Mail Protocol: SMTP
    - SMTP Hostname: 127.0.0.1
    - SMTP Port: 1025
    - no username/password required
 - Trigger a mail event manually (e.g. registering a customer) and check mailcatcher on http://127.0.0.1:1080

## Robo Commands

 * `bin/robo opencart:setup` : Install OpenCart with configuration set in `.env` file
 * `bin/robo opencart:run`   : Run OpenCart on a php build-in web server on port 8000
 * `bin/robo project:deploy` : Mirror contents of the src folder to the OpenCart test environment
 * `bin/robo project:watch`  : Redeploy after changes inside the src/ folder or the composer.json file
 * `bin/robo project:package`: Package a `build.ocmod.zip` inside the target/ folder







