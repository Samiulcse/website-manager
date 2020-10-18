# Website manager

I will update description later. 

## Installation

####Prerequisites

Register and get an API Key from Whois XML API: https://main.whoisxmlapi.com/. It is FREE (500 requests per month and that is enough).

Register slack webhooks for uptime notifications. Go here: https://slack.com/apps/A0F7XDUAZ-incoming-webhooks & setup your slack. Get webhooks UR.


####Lets start

Clone the project 

`git clone https://github.com/raselupm/website-manager.git`

Go to project 

`cd website-manager`

Rename .env.example to .env & Add your WHOIS XML API key on **WHOISXML_APIKEY** variable. Also add your database info. Additionally, you can add SMTP information for get emails when website down or up. Save your slack webhook URL as well.

Install composer

`composer install`

Migrate database

`php artisan migrate`

After doing all fo these, serve the application

`php artisan serve`

**Setting up cron**

We are using laravel schedule for manage cron jobs. You can enable cron by following this:

On local: Open a new tab on terminal. Now run command below: 

`php artisan schedule:work`

On server: type command below

`crontab -e`

Add this command & save & exit. 

`* * * * * cd /path-to-your-project && php artisan schedule:run >> /dev/null 2>&1`


## Disclaimer

This application made as learning purpose. Please don't make this comment when we meet face to face **"Bhai ki sob noob code likhcen, abar vab nen apni birat programmer"**. Thank in advance.


## Contributing

Yes, you are welcome to do that. Please send me requests. Thank you. 


## Security Vulnerabilities

Bhaire, apnar server down hole amar kisu korar nai, swami bidesh. 

## License

The code is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
