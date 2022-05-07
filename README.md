# Restaurant Point-of-Sale (CST-323)
> This project was created using PHP Laravel and MySQL to create a Restaurant Point-of-Sale software program to streamline the restaurant management experience. 
> Live demo [_here_](https://restaurantapp-pos.herokuapp.com). <!-- If you have the project hosted somewhere, include the link here. -->

## Table of Contents
<!-- * [General Info](#general-information) -->
* [Technologies Used](#technologies-used)
* [Features](#features)
* [Deployment Links](#deployment-links)
* [Screenshots](#screenshots)
<!-- * [Demo Videos](#demo-videos) -->
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [How to run project locally](#local-testing)
* [Heroku Cloud Deployment Intructions](#deployment-instructions)
* [How to host a Laravel project on Heroku](#deployment-instructions-quick)
* [Contact](#contact)
* [License](#license)


<!-- ## General Information -->
<!-- - What problem does it (intend to) solve?
- What is the purpose of your project?
- Why did you undertake it? -->


## Technologies Used
- PHP - version 7.4.1
- PHP Laravel Framework - version 5.8.38
- MAMP - version 5.0.2.3860
- MySQL - version 5.7.24
- Bootstrap - version 4.1
- Jquery - version 3.2
- Font-Awesome - version 6.0.0
- Axios - version 0.21
- Popper.js - version 1.12
- Sass - version 1.15.2
- Vue - 2.5.17


## Features
- 

## Deployment Links
- Local Deployment: http://localhost:8000
- Heroku Cloud: https://restaurantapp-pos.herokuapp.com

## Screenshots

Go to `https://restaurantapp-pos.herokuapp.com` to view the Welcome page of the Restaurant POS system.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/157993273-6328b463-15db-4adc-8b94-b9f3e9ea7f43.png" width=100% height=100%>
</p>

Go to `https://restaurantapp-pos.herokuapp.com/register` to view the Registration page of the Restaurant POS system.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/157993352-53530bed-5dfd-498e-9a8c-a423e3d39982.png" width=100% height=100%>
</p>

Go to `https://restaurantapp-pos.herokuapp.com/login` to view the Login page of the Restaurant POS system. Enter email=`root@gmail.com` & password=`Rootroot` for valid admin credentials.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/157993391-de50410a-5ffb-4fa5-8fbf-2a4c065858b5.png" width=100% height=100%>
</p>

Go to `https://restaurantapp-pos.herokuapp.com/management` to view the Restaurant Dashboard page of the Restaurant POS system. Click `Management` to go to the management page and a left menu will appear.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/157993429-5d7e9390-363e-401c-b92e-bb00b07b17f6.png" width=100% height=100%>
</p>

Go to `https://restaurantapp-pos.herokuapp.com/management/category` to view the Restaurant Categories page of the Restaurant POS system along with a list of food categories.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/157993536-133cfd0c-4d6a-4e72-b65c-fcd9bf7f70df.png" width=100% height=100%>
</p>

Go to `loggly.com` to and use the `tag:cst323_logging` for access the Cloud logs.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/161477710-1f010782-ee1f-4d89-a9dd-5788cba6993e.png" width=100% height=100%>
</p>

Go to `uptimerobot.com` to setup monitoring for the RestaurantPOS web app.

<p align="center">
  <img src="https://user-images.githubusercontent.com/40038829/161477951-717e4707-b11d-4b01-b311-31df20adb00a.png" width=100% height=100%>
</p>

<!--## Demo Videos
- Final Application Video: 
    <p align="center">
      [LOOM URL LINK GOES HERE]
    </p>
-->

## Project Status
Project development is: _in-progress_ - This project is in progress of being built up. All Bootstrap UI designs are complete.

Project deployment is: _complete_ - Project is successfully deployed to the cloud and connected to a MySQL database.


## Room for Improvement

Room for improvement:
- Time Management

To do:
- Fix logging in the Heroku Cloud.
- Refactor Cashier section with to fix the User menu option.
- Add the Report section to the dashboard.
- Add Table & User pages for the management section.

## How to run project locally
1. Make sure you download regular version of MAMP locally. 
2. Go to file explorer and go to `MAMP--> htdocs --> RestaurantPOS`
3. Left click in the directory and click open in `GIT Bash`.
4. In 'Git Bash' run `php artisan serve` to run the PHP project locally.
5. Go to your web browser and enter `http://localhost:8000`.
6. The welcome page will be displayed along with the ability to login or register.

## Heroku Cloud Deployment Intructions
1. Create app in Heroku:
    - Click Create App button from the main page. Give your application a name. Click the Create App button.
    - On the Project page, select the Deploy Tab, and link your application to your GitHub repository (BitBucket is not supported on Heroku). If you are not using GiHub, you can either copy your BitBucket repository to GitHub or use the Heroku CLI, as documented below.
    - On the Project page, select the Settings Tab, click the Add Buildpack button, for PHP click the PHP button, click the Save Changes button.
    - On the Project page, select the Resources Tab, under the Add-ons search for JawsDB MySQL, select JawsDB MySQL from the search list, select the Free plan, click the Provision button. NOTE: If you fail to connect too many times to the database Heroku may lock you out from connecting to your database. If you repeatedly cannot connect to your database and are sure your configuration is correct, then delete your current JawsDB MySQL database Add-on and add a new JawsDB MySQL database.
2. Update your App Configuration as necessary:
    - Update the database configuration parameters in your code.
    - For non-Laravel apps add an empty file (one with just { } as contents) named composer.json to your GitHub repository.
    - You can set the version of PHP using the following entry in your composer.json file: "require": { "php": "^7.1.0" }
    - See Heroku PHP Support located at https://devcenter.heroku.com/articles/php-support
3. Connect MySQL Workbench to the instance of MySQL Database. Run your DDL Script to configure the database.
4. You can deploy your application either thru the Heroku GIT Repository or by using your own GitHub or Bitbucket GIT repository. Follow either steps 5 or 6 below. NOTE: make sure to include all of the hidden files and the vendor folder in your GIT repository (you might need to modify the .gitignore file) and ensure the .env file is included as this is a required file to run a Laravel application. This should also be tested by cloning your GIT repository as a zip file, then deploying the clone files to your local MAMP, and validating that the application functions properly from the cloned repository.
5. To deploy using the Heroku GIT repository use the following steps:
    - Clone the Heroku GIT repository provided by Heroku (go to your App Settings to get the URL).
    - Update your App Configuration as noted above.
    - Push your code from your local repository to the Heroku GIT repository.
    - Test the app: https://[APP NAME].herokuapp.com.
6. To deploy using your GitHub repository and a Build Pipeline use the following steps:
    - Update your App Configuration as noted above and push the changes to your GitHub repository.
    - Create Heroku Pipeline and add your PHP app to it.
    - Go to your Heroku Pipeline and click on your PHP app, select the Deploy menu option, and make sure the Enable Automatic Deploys is enabled from your master branch.
    - Start a Build and fix any errors that may occur. Should receive a build success message.
7. Go to your Heroku Pipeline and click on your PHP app, select the Deploy menu option, and then click the Deploy Branch button.
8. Push a code change to your GitHub repository.
    - Test your app at: https://[APP NAME].herokuapp.com.
9. Your project is now deployed on the Heroku Cloud. 

## How to host a Laravel project on Heroku
1. After pushing your laravel project to GitHub, deploy the app in Heroku and click your Heroku URL website link. You should see a "Forbidden" error screen which is a good sign.
2. Now we need to create a file named "Procfile in the root directory of your project with "web: vendor/bin/heroku-php-apache2 public/" and make sure it has been pushed to GitHub.
3. If you go to your Heroku website again you should receive a "500 | Server Error" which is a Laravel error page which also means your project has been deployed successfully.
4. Heroku doesn't work with the Laravel .env file so you need to manually add your variables to Heroku by going to "Deploy" --> Click "Reveal Config Vars". 
5. Add the neccessary variables then try again and you should see your Laravel Home page displayed.  
    - https://just1and0.medium.com/how-to-host-your-laravel-application-for-free-on-heroku-4789688d444b

## Contact
Created by [Micah Miller](https://github.com/mmiller2321) and [Mann Jaiswal](https://github.com/MannJaiswal786) - feel free to contact us via the email listed below our GitHub profile details!

## License
This project is open source and available under the [GNU General Public License v3.0](https://github.com/mmiller2321/RestaurantPOS/blob/main/LICENSE).

