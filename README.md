# Laravel-CLI-Command-List

### Create a new project

```bash
composer create-project laravel/laravel example-app
```

### Run the project

```bash
php artisan serve
```

### Copy the .env.example to .env

```bash
cp .env.example .env
```

```bash
copy .env.example .env
```

### Generate the key

```bash
php artisan key:generate
```

### Controller
**Create a New Controller**:
```bash
php artisan make:controller PhotoController
```

**Create a Single Action Controller**:
```bash
php artisan make:controller ProvisionServer --invokable
```

**Create a Resource Controller**:
```bash
php artisan make:controller PhotoController --resource
```

**Create a Resource Controller with its Own Model**:
```bash
php artisan make:controller PhotoController --model=Photo --resource
```

**Create a Resource Controller with its Own Model and Custom Requests**:
```bash
php artisan make:controller PhotoController --model=Photo --resource --requests
```

**Create an API Controller**:
```bash
php artisan make:controller PhotoController --api
```

### About Application

You can get a quick overview of your application's configuration, drivers, and environment via the about Artisan command

```bash
php artisan about
```

If you're only interested in a particular section of the application overview output, you may filter for that section using the --only

```bash
php artisan about --only=environment
```

To explore a specific configuration file's values in detail, you may use the config:show Artisan command

```bash
php artisan config:show database
```

### Encryption

To encrypt an environment file, you may use the env:encrypt command

```bash
php artisan env:encrypt
```

You may encrypt a specific environment file using the --env flag

```bash
php artisan env:encrypt --env=staging
```

### Decryption

To decrypt an environment file, you may use the env:decrypt command

```bash
php artisan env:decrypt
```

You may decrypt a specific environment file using the --env flag

```bash
php artisan env:decrypt --env=staging
```

In order to overwrite an existing environment file, you may provide the --force option to the env:decrypt command

```bash
php artisan env:decrypt --force
```

### Caching

This command may be used to purge the cached configuration

```bash
php artisan config:clear
```

To cache your current configuration, you may use the config:cache Artisan command, The command should not be run during local development as configuration options will frequently need to be changed during the course of your application's development

```bash
php artisan config:cache
```

To cache your events and listeners, you may use the event:cache command

```bash
php artisan event:cache
```

To cache your application's routes, you may use the route:cache Artisan command

```bash
php artisan route:cache
```

To clear your route cache, you may use the route:clear command

```bash
php artisan route:clear
```

**To cache your Blade views, you may use the view:cache Artisan command**

```bash
php artisan view:cache
```

**To clear the view cache, you may use the view:clear command**

```bash
php artisan view:clear
```

### Debug Mode

**Enable Maintenance Mode**:

   ```bash
   php artisan down
   ```

**Enable Maintenance Mode with Auto Refresh (15 seconds)**:

   ```bash
   php artisan down --refresh=15
   ```

**Enable Maintenance Mode with Retry-After Header (60 seconds)**:

   ```bash
   php artisan down --retry=60
   ```

**Enable Maintenance Mode with Secret Token to Bypass**:

   ```bash
   php artisan down --secret="1630542a-246b-4b66-afa1-dd72a4c43515"
   ```

**Enable Maintenance Mode with Custom View**:
   ```bash
   php artisan down --render="errors::503"
   ```

**Enable Maintenance Mode with Redirect to a Different URL**:

```bash
php artisan down --redirect=/
```

**Bring the Application Out of Maintenance Mode**:

```bash
php artisan up
```

### App Directory

**View a List of All Available Commands**:

```bash
php artisan list make
```

**View a List of All Available Commands with JSON Output Format**:

```bash
php artisan list make --format=json
```


### Autoloader Optimization
**To optimize Composer's autoloader, you may use the optimize-autoloader command**
```bash
composer install --optimize-autoloader --no-dev 
```

### Service Providers
**To create a service provider, use the make:provider command**
```bash
php artisan make:provider RiakServiceProvider 
```

### Route List
**View a List of All Registered Routes for the Application**:
```bash
php artisan route:list
```

**View More Details About Each Route (Including Route Middleware)**:
```bash
php artisan route:list -v
```

**View Even More Details About Each Route (Including Route Middleware)**:
```bash
php artisan route:list -vv
```

**View a List of All Registered Routes for the Application Except Vendor Routes**:
```bash
php artisan route:list --except-vendor
```

**View a List of All Registered Vendor Routes**:
```bash
php artisan route:list --only-vendor
```

### Middleware
**Create a New Middleware**:
```bash
php artisan make:middleware EnsureTokenIsValid
```

### View
**Create a New View**:

```bash
php artisan make:view greeting
```

### Component
**Create a New Component**:
```bash
php artisan make:component Alert
```

**Create a New Component within a Subdirectory**:
```bash
php artisan make:component Forms/Input
```

**Create a New Component with a Custom View**:
```bash
php artisan make:component forms.input --view
```

**Create a New Component with an Inline View**:
```bash
php artisan make:component Alert --inline
```

### Session
**Generate a Migration that Creates the Sessions Table**:
```bash
php artisan session:table
```

### Form Request Validation
**Create a New Form Request Class**:
```bash
php artisan make:request StorePostRequest
```

**Create a New Validation Rule**:
```bash
php artisan make:rule Uppercase
```

**Create a New Implicit Validation Rule**:
```bash
php artisan make:rule Uppercase --implicit
```

### Error Handling
**Publish the Error Views Used by the Default Exception Handler**:
```bash
php artisan vendor:publish --tag=laravel-errors
```

### Logging
*Laravel Pail is a package that allows you to easily dive into your Laravel application's log files directly from the command line. Unlike the standard tail command, Pail is designed to work with any log driver, including Sentry or Flare. In addition, Pail provides a set of useful filters to help you quickly find what you're looking for.*

**Install the `laravel/pail` Composer Package**:
```bash
composer require laravel/pail
```

**Start Tailing Logs**:
```bash
php artisan pail
```

**Increase the Verbosity of the Output (Avoid Truncation)**:
```bash
php artisan pail -v
```

**Maximum Verbosity (Display Exception Stack Traces)**:
```bash
php artisan pail -vv
```

**Filter Logs by a Given String**:
```bash
php artisan pail --filter="production"
```

**Filter Logs by a Given Message**:
```bash
php artisan pail --message="User created"
```

**Filter Logs by a Given Level**:
```bash
php artisan pail --level=error
```

**Filter Logs by a Given User ID**:
```bash
php artisan pail --user=1
```

### Artisan Console
**View a List of All Available Artisan Commands**:
```bash
php artisan list
```

**View More Information About a Given Command**:
```bash
php artisan help migrate
```

### Tinker (REPL)
*Laravel Tinker is a powerful REPL for the Laravel framework, powered by the PsySH package*

**Install the `laravel/tinker` Composer Package**:
```bash
composer require laravel/tinker
```

**Enter the Tinker REPL**:
```bash
php artisan tinker
```

**Publish Tinker's Configuration File**:
```bash
php artisan vendor:publish --provider="Laravel\Tinker\TinkerServiceProvider"
```


### Writing Commands
*In addition to the commands provided with Artisan, you may build your own custom commands.*

**Create a New Command**:
```bash
php artisan make:command SendEmails
```

**Run a Command in Isolation**:
```bash
php artisan mail:send 1 --isolated
```

**Run a Command in Isolation for a Given Number of Seconds**:
```bash
php artisan mail:send 1 --isolated=12
```

**Queue a Command**:
```bash
php artisan mail:send 1 --queue
```

**Queue a Command on a Specific Queue**:
```bash
php artisan mail:send 1 --queue=default
```

**Queue a Command on a Specific Queue (Using `-Q` Flag)**:
```bash
php artisan mail:send 1 -Qdefault
```

**Run a Command on Multiple Connections or Queues (Multiple Arguments)**:
```bash
php artisan mail:send 1 2
```

**Run a Command on Multiple Connections or Queues (Using Multiple `--id` Flags)**:
```bash
php artisan mail:send --id=1 --id=2
```

### Stub Customization
**Publish All of the Package's Stubs**:
```bash
php artisan stub:publish
```

### Broadcasting
**Install the `pusher/pusher-php-server` Composer Package**:
```bash
composer require pusher/pusher-php-server
```

**Install the `ably/ably-php` Composer Package**:
```bash
composer require ably/ably-php
```

**Install the `laravel-echo` and `pusher-js` Packages**:
```bash
npm install --save-dev laravel-echo pusher-js
```

### Channels
**View a List of All Registered Channels**:
```bash
php artisan channel:list
```

**Create a New Channel**:
```bash
php artisan make:channel OrderChannel
```

### Events & Listeners
**Generate All Events and Listeners for Your Application**:
```bash
php artisan event:generate
```

**Create a New Event Class**:
```bash
php artisan make:event PodcastProcessed
```

**Create a New Event Listener**:
```bash
php artisan make:listener SendPodcastNotification --event=PodcastProcessed
```

### Storage
**Create the Symbolic Link for Storage**:
```bash
php artisan storage:link
```

**Install the `league/flysystem-aws-s3-v3` Composer Package**:
```bash
composer require league/flysystem-aws-s3-v3 "^3.0" --with-all-dependencies
```

**Install the `league/flysystem-ftp` Composer Package**:
```bash
composer require league/flysystem-ftp "^3.0"
```

**Install the `league/flysystem-sftp-v3` Composer Package**:
```bash
composer require league/flysystem-sftp-v3 "^3.0"
```

**Install the `league/flysystem-path-prefixing` Composer Package**:
```bash
composer require league/flysystem-path-prefixing "^3.0"
```

**Install the `league/flysystem-read-only` Composer Package**:
```bash
composer require league/flysystem-read-only "^3.0"
```

**Install the `spatie/flysystem-dropbox` Composer Package**:
```bash
composer require spatie/flysystem-dropbox
```

### HTTP Client
**Install the `guzzlehttp/guzzle` Composer Package**:
```bash
composer require guzzlehttp/guzzle
```

### Localization
**Publish All of the Package's Language Files**:
```bash
php artisan lang:publish
```

### Mail
**Install the `symfony/mailgun-mailer` and `symfony/http-client` Composer Packages**:
```bash
composer require symfony/mailgun-mailer symfony/http-client
```

**Install the `symfony/postmark-mailer` and `symfony/http-client` Composer Packages**:
```bash
composer require symfony/postmark-mailer symfony/http-client
```

**Install the `aws/aws-sdk-php` Composer Package**:
```bash
composer require aws/aws-sdk-php
```

**Install the `mailersend/laravel-driver` Composer Package**:
```bash
composer require mailersend/laravel-driver
```

**Create a New Mailable Class**:
```bash
php artisan make:mail OrderShipped
```

**Create a New Mailable Class with a Markdown Template**:
```bash
php artisan make:mail OrderShipped --markdown=emails.orders.shipped
```

**Publish the Mail Configuration File**:
```bash
php artisan vendor:publish --tag=laravel-mail
```

**Install the `symfony/brevo-mailer` and `symfony/http-client` Composer Packages**:
```bash
composer require symfony/brevo-mailer symfony/http-client
```

### Notifications
**Create a New Notification Class**:
```bash
php artisan make:notification InvoicePaid
```

**Publish the Notification Configuration File**:
```bash
php artisan vendor:publish --tag=laravel-notifications
```

**Create a New Notification Class with a Markdown Template**:
```bash
php artisan make:notification InvoicePaid --markdown=mail.invoice.paid
```

**Publish the Mail Configuration File**:
```bash
php artisan vendor:publish --tag=laravel-mail
```

**Generate a Migration to Create the Notifications Table**:
```bash
php artisan notifications:table
```

**Install the `laravel/slack-notification-channel` Composer Package**:
```bash
composer require laravel/slack-notification-channel
```

### Queues
**To start the worker, you may use the queue:work command**:
```bash
php artisan queue:work --queue=high,default
```

**To generate a migration that creates the jobs table, use the queue:table command**:
```bash
php artisan queue:table
```

**To create a new job class, use the make:job Artisan command**:
```bash
php artisan make:job ProcessPodcast
```

**To specify the maximum number of times a job should be attempted, you may use the --tries switch on the queue:work command**:
```bash
php artisan queue:work --tries=3
```

**To specify the maximum number of seconds a child process can run, you may use the --timeout switch on the queue:work command**:
```bash
php artisan queue:work --timeout=30
```

**To generate a migration that creates the batches table, use the queue:batches-table command**:
```bash
php artisan queue:batches-table
```

**To start the worker, you may use the queue:work command**:
```bash
php artisan queue:work
```

**To increase the verbosity of the worker's output, you may use the -v option**:
```bash
php artisan queue:work -v
```

**Start the Worker in "Listen" Mode**:
```bash
php artisan queue:listen
```

**Start the Worker for a Specific Connection (e.g., Redis)**:
```bash
php artisan queue:work redis
```

**Start the Worker for a Specific Queue (e.g., emails)**:
```bash
php artisan queue:work redis --queue=emails
```

**Process Only the Next Job on the Queue**:
```bash
php artisan queue:work --once
```

**Process a Specific Number of Jobs**:
```bash
php artisan queue:work --max-jobs=1000
```

**Stop the Worker When the Queue is Empty**:
```bash
php artisan queue:work --stop-when-empty
```

**Stop the Worker After a Specified Time**:
```bash
php artisan queue:work --max-time=3600
```

**Specify the Number of Seconds to Wait Before Polling for New Jobs**:
```bash
php artisan queue:work --sleep=3
```

**Specify Multiple Queues for the Worker to Listen On**:
```bash
php artisan queue:work --queue=high,low
```

**Restart All Queue Workers**:
```bash
php artisan queue:restart
```

**Generate a Migration to Create the Failed Jobs Table**:
```bash
php artisan queue:failed-table
```

**Specify the Maximum Number of Attempts for a Job on Redis**:
```bash
php artisan queue:work redis --tries=3
```

**Specify the Backoff Time for Retries on Redis**:
```bash
php artisan queue:work redis --tries=3 --backoff=3
```

**View All Failed Jobs**:
```bash
php artisan queue:failed
```

**Retry All Failed Jobs for a Specific Queue**:
```bash
php artisan queue:retry --queue=name
```

**Retry All Failed Jobs**:
```bash
php artisan queue:retry all
```

**Retry a Specific Failed Job**:
```bash
php artisan queue:retry 5
```

**Delete a Specific Failed Job**:
```bash
php artisan queue:forget 5
```

**Delete All Failed Jobs**:
```bash
php artisan queue:flush
```

**Prune Failed Jobs Older Than a Given Number of Days**:
```bash
php artisan queue:prune-failed
```

**Prune Failed Jobs Older Than a Given Number of Hours**:
```bash
php artisan queue:prune-failed --hours=48
```

**Run the Worker in Daemon Mode**:
```bash
php artisan queue:work --daemon
```

### Storing Failed Jobs In DynamoDB
**Install the `aws/aws-sdk-php` Composer Package**:
```bash
composer require aws/aws-sdk-php
```

### Clearing Jobs From Queues
**Delete All Jobs from a Given Queue**:
```bash
php artisan queue:clear
```

**Delete All Jobs from a Specific Queue (e.g., emails)**:
```bash
php artisan queue:clear --queue=emails
```

**Delete All Jobs from a Specific Queue (e.g., emails) on a Specific Connection (e.g., Redis)**:
```bash
php artisan queue:clear redis --queue=emails
```

### Monitoring Your Queues
```bash
php artisan queue:monitor redis:default,redis:deployments --max=100
```

### Task Scheduling
**View All Scheduled Tasks**:
```bash
php artisan schedule:list
```

**Interrupt a Scheduled Task**:
```bash
php artisan schedule:interrupt
```

**Run Your Scheduled Tasks**:
```bash
php artisan schedule:run
```

**Run the Scheduler in the Background**:
```bash
php artisan schedule:work
```

### Policies
**Create a New Policy**:
```bash
php artisan make:policy PostPolicy
```

**Create a New Policy for a Model (e.g., Post)**:
```bash
php artisan make:policy PostPolicy --model=Post
```

### Database
**Run All Outstanding Migrations**:
```bash
php artisan migrate
```

**View a List of All Available Artisan Commands**:
```bash
php artisan db
```

**View a List of Available Artisan Commands for MySQL**:
```bash
php artisan db mysql
```

**View a List of All Database Connections Configured for the Application**:
```bash
php artisan db:show
```

**Inspect a Specific Database Connection (e.g., PostgreSQL)**:
```bash
php artisan db:show --database=pgsql
```

**Include Table Row Counts and View Details in the Output**:
```bash
php artisan db:show --counts --views
```

**View the Table Definition for a Given Table (e.g., users)**:
```bash
php artisan db:table users
```

**Monitor Database Connections (e.g., MySQL, PostgreSQL)**:
```bash
php artisan db:monitor --databases=mysql,pgsql --max=100
```

**Create the Migration Repository**:
```bash
php artisan migrate:install
```

**Create a New Migration (e.g., create_flights_table)**:
```bash
php artisan make:migration create_flights_table
```

**Create a Migration to Modify an Existing Table (e.g., add_votes_to_users_table)**:
```bash
php artisan make:migration add_votes_to_users_table --table=users
```

**Dump the Database Schema**:
```bash
php artisan schema:dump
```

**Dump the Database Schema Without Comments**:
```bash
php artisan schema:dump --prune
```

**Dump the Database Schema Without Comments for a Specific Database (e.g., testing)**:
```bash
php artisan schema:dump --database=testing --prune
```

**View the Status of Your Migrations**:
```bash
php artisan migrate:status
```

**Run Migrations Without Actually Running Them (Pretend Mode)**:
```bash
php artisan migrate --pretend
```

**Run Migrations in Isolation**:
```bash
php artisan migrate --isolated
```

**Run Migrations Without a Prompt (Force)**:
```bash
php artisan migrate --force
```

**Rollback the Latest Migration Operation**:
```bash
php artisan migrate:rollback
```

**Rollback the Last Five Migrations**:
```bash
php artisan migrate:rollback --step=5
```

**Rollback Migrations by a Specific Batch (e.g., batch 3)**:
```bash
php artisan migrate:rollback --batch=3
```

**Rollback Migrations Without Actually Running Them (Pretend Mode)**:
```bash
php artisan migrate:rollback --pretend
```

**Rollback All Migrations**:
```bash
php artisan migrate:reset
```

**Rollback All Migrations and Then Execute the Migrate Command**:
```bash
php artisan migrate:refresh
```

**Rollback All Migrations and Execute the Migrate Command with Seeding**:
```bash
php artisan migrate:refresh --seed
```

**Rollback All Migrations and Execute the Migrate Command with a Step Option**:
```bash
php artisan migrate:refresh --step=5
```

**Drop All Tables and Re-run All Migrations**:
```bash
php artisan migrate:fresh
```

**Drop All Tables and Re-run All Migrations with Seeding**:
```bash
php artisan migrate:fresh --seed
```

### Seeder
**Create a New Seeder**:
```bash
php artisan make:seeder UserSeeder
```

**Seed the Database**:
```bash
php artisan db:seed
```

**Seed a Specific Seeder Class (e.g., UserSeeder)**:
```bash
php artisan db:seed --class=UserSeeder
```

**Drop All Tables and Re-run All Migrations and Seeds**:
```bash
php artisan migrate:fresh --seed
```

**Drop All Tables and Re-run All Migrations and Specific Seeder (e.g., UsersTableSeeder)**:
```bash
php artisan migrate:fresh --seed --seeder=UsersTableSeeder
```

**Seed the Database Without a Prompt**:
```bash
php artisan db:seed --force
```

### Redis
**Install the Predis Composer Package**:
```bash
composer require predis/predis
```

**View a List of All Available Artisan Redis Commands**:
```bash
php artisan redis:command
```

**Scan for Redis Commands**:
```bash
php artisan redis:command --scan
```

### Eloquent ORM
**Create a New Model**:
```bash
php artisan make:model Flight
```

**Create a New Model and Its Migration**:
```bash
php artisan make:model Flight --migration
```

**View a List of All Available Artisan Model Commands**:
```bash
php artisan model:show Flight
```

### Generate a model and a FlightFactory class...
**Create a New Model and Its Factory**:

```bash
php artisan make:model Flight --factory
```

**Create a New Model and Its Factory (Using Short Option)**:

```bash
php artisan make:model Flight -f
```

### Generate a model and a FlightSeeder class...
**Create a New Model and Its Seeder**:

```bash
php artisan make:model Flight --seed
```

**Create a New Model and Its Seeder (Using Short Option)**:

```bash
php artisan make:model Flight -s
```

### Generate a model and a FlightController class...
**Create a New Model and Its Controller**:

```bash
php artisan make:model Flight --controller
```

**Create a New Model and Its Controller (Using Short Option)**:

```bash
php artisan make:model Flight -c
```

### Generate a model, FlightController resource class, and form request classes...
**Create a New Model, Its Controller, Resource, and Requests**:

```bash
php artisan make:model Flight --controller --resource --requests
```

**Create a New Model, Its Controller, Resource, and Requests (Using Short Option)**:

```bash
php artisan make:model Flight -crR
```

### Generate a model and a FlightPolicy class...
**Create a New Model and Its Policy**:

```bash
php artisan make:model Flight --policy
```

**Create a New Model and Its Policy (Using Short Option)**:

```bash
php artisan make:model Flight -p
```

### Generate a model and a migration, factory, seeder, and controller...
**Create a New Model and Its Migration, Factory, Seeder, and Controller**:

```bash
php artisan make:model Flight -mfsc
```

This command combines multiple options to create the model with the following associated components:

- Migration (`-m`)
- Factory (`-f`)
- Seeder (`-s`)
- Controller (`-c`)


### Shortcut to generate a model, migration, factory, seeder, policy, controller, and form requests...
**Create a New Model and Its Migration, Factory, Seeder, Policy, Controller, and Form Requests**:

```bash
php artisan make:model Flight --all
```

### Generate a pivot model...
**Create a New Pivot Model**:

```bash
php artisan make:model Member --pivot
```

**Create a New Pivot Model (Using Short Option)**:

```bash
php artisan make:model Member -p
```

---

**Prune Models Without Corresponding Database Tables**:

```bash
php artisan model:prune --pretend
```

### Scopes
**Create a New Scope**:

```bash
php artisan make:scope AncientScope
```

**Create a New Scope for a Specific Model**:

```bash
php artisan make:scope AncientScope --model=Flight
```

### Observers
**Create a New Observer**:

```bash
php artisan make:observer UserObserver --model=User
```

### Casts
**Create a New Cast**:

```bash
php artisan make:cast Json
```

**Create a New Inbound Cast** (Applied when setting a value on the model):

```bash
php artisan make:cast Hash --inbound
```

### Resources
**Create a New Resource**:

```bash
php artisan make:resource UserResource
```

**Create a New Resource Collection** (Using the `--collection` option):

```bash
php artisan make:resource User --collection
```

**Create a New Resource Collection**:

```bash
php artisan make:resource UserCollection
```

### Factories
**Create a New Factory**:

```bash
php artisan make:factory FlightFactory
```

### Testing
**Create a New Test**:
```bash
php artisan make:test UserTest
```

**Create a New Unit Test**:
```bash
php artisan make:test UserTest --unit
```

**Create a New Pest Test**:
```bash
php artisan make:test UserTest --pest
```

**Create a New Unit Test with Pest**:
```bash
php artisan make:test UserTest --unit --pest
```

**Run Tests**:
```bash
php artisan test
```

**Run a Specific Test Suite and Stop on Failure**:
```bash
php artisan test --testsuite=Feature --stop-on-failure
```

**Generate a Code Coverage Report**:
```bash
php artisan test --coverage
```

**Generate a Code Coverage Report with Minimum Coverage**:
```bash
php artisan test --coverage --min=80.3
```

**Generate a Performance Profile**:
```bash
php artisan test --profile
```

### NPM
**Install All of the Project's Dependencies**:
```bash
npm install
```

**Compile Your Assets for Development**:
```bash
npm run dev
```

**Compile Your Assets for Production**:
```bash
npm run build
```
