# Laravel-CLI-Command-List
## Laravel Project CMD Tool
1. Create a new project
   -- composer create-project laravel/laravel example-app

2. Run the project
    -- php artisan serve

3. Copy the .env.example to .env
    -- cp .env.example .env
    -- copy .env.example .env

4. Generate the key
    -- php artisan key:generate

5. About Application
    -- php artisan about (You can get a quick overview of your application's configuration, drivers, and environment via the about Artisan command)
    -- php artisan about --only=environment (If you're only interested in a particular section of the application overview output, you may filter for that section using the --only)
    -- php artisan config:show database (To explore a specific configuration file's values in detail, you may use the config:show Artisan command)

6. Encryption
    -- php artisan env:encrypt (To encrypt an environment file, you may use the env:encrypt command)
    -- php artisan env:encrypt --env=staging (You may encrypt a specific environment file using the --env flag)

7. Decryption
    -- php artisan env:decrypt (To decrypt an environment file, you may use the env:decrypt command)
    -- php artisan env:decrypt --env=staging (You may decrypt a specific environment file using the --env flag)
    -- php artisan env:decrypt --force (In order to overwrite an existing environment file, you may provide the --force option to the env:decrypt command)

8. Caching
    -- php artisan config:clear (This command may be used to purge the cached configuration)
    -- php artisan config:cache (To cache your current configuration, you may use the config:cache Artisan command, The command should not be run during local development as configuration options will frequently need to be changed during the course of your application's development)
    
    -- php artisan event:cache (To cache your events and listeners, you may use the event:cache command)

    -- php artisan route:cache (To cache your application's routes, you may use the route:cache Artisan command)
    -- php artisan route:clear (To clear your route cache, you may use the route:clear command)

    -- php artisan view:cache (To cache your Blade views, you may use the view:cache Artisan command)
    -- php artisan view:clear (To clear the view cache, you may use the view:clear command)


9. Debug Mode
    -- php artisan down (To enable maintenance mode, execute the down Artisan command)
    -- php artisan down --refresh=15 (If you would like the Refresh HTTP header to be sent with all maintenance mode responses, you may provide the refresh option when invoking the down command. The Refresh header will instruct the browser to automatically refresh the page after the specified number of seconds)
    -- php artisan down --retry=60 (You may also provide a retry option to the down command, which will be set as the Retry-After HTTP header's value, although browsers generally ignore this header)
    -- php artisan down --secret="1630542a-246b-4b66-afa1-dd72a4c43515" (To allow maintenance mode to be bypassed using a secret token, you may use the secret option to specify a maintenance mode bypass token)
    -- php artisan down --render="errors::503" (If you would like to display a custom view when your application is in maintenance mode, you may use the render option to specify the view that should be displayed)
    -- php artisan down --redirect=/ (If you would like to redirect the user to a different URL when your application is in maintenance mode, you may use the redirect option to specify the URL to which the user should be redirected)
    -- php artisan up (To bring the application out of maintenance mode, use the up command)

10. App Directory
    -- php artisan list make (To view a list of all available commands, you may use the list command)
    -- php artisan list make --format=json (You may also use the --format option to specify the output format for the command list)

11. Autoloader Optimization
    -- composer install --optimize-autoloader --no-dev (To optimize Composer's autoloader, you may use the optimize-autoloader command)

12. Service Providers
    -- php artisan make:provider RiakServiceProvider (To create a service provider, use the make:provider command)

13. Route List
    -- php artisan route:list (To view a list of all registered routes for the application, you may use the route:list command)
    -- php artisan route:list -v (To view more details about each route such as the route middleware, you may use the -v option)
    -- php artisan route:list -vv (To view even more details about each route such as the route middleware, you may use the -vv option)
    -- php artisan route:list --except-vendor (To view a list of all registered routes for the application except vendor routes, you may use the --except-vendor option)
    -- php artisan route:list --only-vendor (To view a list of all registered routes for the application except vendor routes, you may use the --only-vendor option)

14. Middleware
    -- php artisan make:middleware EnsureTokenIsValid (To create a new middleware, use the make:middleware command)

15. Controller
    -- php artisan make:controller PhotoController (To create a new controller, use the make:controller command)
    -- php artisan make:controller ProvisionServer --invokable (To create a single action controller, use the --invokable flag)
    -- php artisan make:controller PhotoController --resource (To create a resource controller, use the --resource flag)
    -- php artisan make:controller PhotoController --model=Photo --resource (To create a resource controller with its own model, use the --model flag)
    -- php artisan make:controller PhotoController --model=Photo --resource --requests (To create a resource controller with its own model and custom requests, use the --model and --requests flags)
    -- php artisan make:controller PhotoController --api (To create an API controller, use the --api flag)

16. View 
    -- php artisan make:view greeting (To create a new view, use the make:view command)

17. Component
    -- php artisan make:component Alert (To create a new component, use the make:component command)
    -- php artisan make:component Forms/Input (To create a new component within a subdirectory, use the make:component command)
    -- php artisan make:component forms.input --view (To create a new component with a custom view, use the --view flag)
    -- php artisan make:component Alert --inline (To create a new component with an inline view, use the --inline flag)

18. NPM
    -- npm install (To install all of the project's dependencies, you may use the install command)
    -- npm run dev (To compile your assets, use the dev command)
    -- npm run build (To compile your assets for production, use the build command)

18. Session 
    -- php artisan session:table (To generate a migration that creates the sessions table, use the session:table command)

19. Form Request Validation
    -- php artisan make:request StorePostRequest (To create a new form request class, use the make:request command)
    -- php artisan make:rule Uppercase (To create a new validation rule, use the make:rule command)
    -- php artisan make:rule Uppercase --implicit (To create a new implicit validation rule, use the --implicit flag)

20. Error Handling
    -- php artisan vendor:publish --tag=laravel-errors (To publish the error views used by the default exception handler, use the vendor:publish Artisan command)

21. Logging
    Laravel Pail is a package that allows you to easily dive into your Laravel application's log files directly from the command line. Unlike the standard tail command, Pail is designed to work with any log driver, including Sentry or Flare. In addition, Pail provides a set of useful filters to help you quickly find what you're looking for.
    -- composer require laravel/pail (To get started, install the laravel/pail Composer package)
    -- php artisan pail (To start tailing logs, run the pail command)
    -- php artisan pail -v (To increase the verbosity of the output and avoid truncation (…), use the -v option)
    -- php artisan pail -vv (For maximum verbosity and to display exception stack traces, use the -vv option)
    -- php artisan pail --filter="production" (To filter the logs by a given string, use the --filter option)
    -- php artisan pail --message="User created" (To filter the logs by a given string, use the --message option)
    -- php artisan pail --level=error (To filter the logs by a given level, use the --level option)
    -- php artisan pail --user=1 (To filter the logs by a given user ID, use the --user option)

22. Artisan Console
    -- php artisan list (To view a list of all available Artisan commands, you may use the list command)
    -- php artisan help migrate (To view more information about a given command, such as its description, arguments, options, and aliases, use the help command)

    ## Tinker (REPL)
    Laravel Tinker is a powerful REPL for the Laravel framework, powered by the PsySH package
    -- composer require laravel/tinker (To get started, install the laravel/tinker Composer package)
    -- php artisan tinker (To enter the Tinker REPL, run the tinker Artisan command)
    -- php artisan vendor:publish --provider="Laravel\Tinker\TinkerServiceProvider" (To publish Tinker's configuration file, use the vendor:publish Artisan command)

    ## Writing Commands
    In addition to the commands provided with Artisan, you may build your own custom commands.
    -- php artisan make:command SendEmails (To create a new command, use the make:command Artisan command)
    -- php artisan mail:send 1 --isolated (To run a command in isolation, use the --isolated flag)
    -- php artisan mail:send 1 --isolated=12 (To run a command in isolation for a given number of seconds, use the --isolated flag with a value in seconds)
    -- php artisan mail:send 1 --queue (To queue a command, use the --queue flag)
    -- php artisan mail:send 1 --queue=default (To queue a command on a specific queue, use the --queue flag with a value)
    -- php artisan mail:send 1 -Qdefault (To queue a command on a specific queue, use the -Q flag with a value)
    -- php artisan mail:send 1 2 (To run a command on multiple connections or queues, use multiple arguments)
    -- php artisan mail:send --id=1 --id=2 (To run a command on multiple connections or queues, use multiple arguments)

    ## Stub Customization
    -- php artisan stub:publish (To publish all of the package's stubs, use the stub:publish command)

23. Broadcasting
    -- composer require pusher/pusher-php-server (To get started, install the pusher/pusher-php-server Composer package)
    -- composer require ably/ably-php  (To get started, install the ably/ably-php Composer package)
    -- npm install --save-dev laravel-echo pusher-js (To get started, install the laravel-echo and pusher-js packages)

24. Channels
    -- php artisan channel:list (To view a list of all of the registered channels, you may use the channel:list command)
    -- php artisan make:channel OrderChannel (To create a new channel, use the make:channel command)

25. Events & Listeners
    -- php artisan event:generate (To generate all of the events and listeners for your application, you may use the event:generate command)
    -- php artisan make:event PodcastProcessed (To create a new event class, use the make:event command)
    -- php artisan make:listener SendPodcastNotification --event=PodcastProcessed (To create a new event listener, use the make:listener command)

26. Storage
    -- php artisan storage:link (To create the symbolic link, you may use the storage:link Artisan command)
    -- composer require league/flysystem-aws-s3-v3 "^3.0" --with-all-dependencies (To get started, install the league/flysystem-aws-s3-v3 Composer package)
    -- composer require league/flysystem-ftp "^3.0" (To get started, install the league/flysystem-ftp Composer package)
    -- composer require league/flysystem-sftp-v3 "^3.0" (To get started, install the league/flysystem-sftp-v3 Composer package)
    -- composer require league/flysystem-path-prefixing "^3.0" (To get started, install the league/flysystem-path-prefixing Composer package)
    -- composer require league/flysystem-read-only "^3.0" (To get started, install the league/flysystem-read-only Composer package)
    -- composer require spatie/flysystem-dropbox (To get started, install the spatie/flysystem-dropbox Composer package)

27. HTTP Client
    -- composer require guzzlehttp/guzzle (To get started, install the guzzlehttp/guzzle Composer package)

28. Localization
    -- php artisan lang:publish (To publish all of the package's language files, use the lang:publish command)

29. Mail
    -- composer require symfony/mailgun-mailer symfony/http-client (To get started, install the symfony/mailgun-mailer and symfony/http-client Composer packages)
    -- composer require symfony/postmark-mailer symfony/http-client (To get started, install the symfony/postmark-mailer and symfony/http-client Composer packages)
    -- composer require aws/aws-sdk-php (To get started, install the aws/aws-sdk-php Composer package)
    -- composer require mailersend/laravel-driver (To get started, install the mailersend/laravel-driver Composer package)
    -- php artisan make:mail OrderShipped (To create a new mailable class, use the make:mail Artisan command)
    -- php artisan make:mail OrderShipped --markdown=emails.orders.shipped (To create a new mailable class with a Markdown template, use the --markdown option)
    -- php artisan vendor:publish --tag=laravel-mail (To publish the mail configuration file, use the vendor:publish Artisan command)
    -- composer require symfony/brevo-mailer symfony/http-client (To get started, install the symfony/brevo-mailer and symfony/http-client Composer packages)

30. Notifications
    -- php artisan make:notification InvoicePaid (To create a new notification class, use the make:notification Artisan command)
    -- php artisan vendor:publish --tag=laravel-notifications (To publish the notification configuration file, use the vendor:publish Artisan command)
    -- php artisan make:notification InvoicePaid --markdown=mail.invoice.paid (To create a new notification class with a Markdown template, use the --markdown option)
    -- php artisan vendor:publish --tag=laravel-mail (To publish the mail configuration file, use the vendor:publish Artisan command)
    -- php artisan notifications:table (To generate a migration that creates the notifications table, use the notifications:table command)
    -- composer require laravel/slack-notification-channel (To get started, install the laravel/slack-notification-channel Composer package)

31. Queues
    -- php artisan queue:work --queue=high,default (To start the worker, you may use the queue:work command)
    -- php artisan queue:table (To generate a migration that creates the jobs table, use the queue:table command)
    -- php artisan make:job ProcessPodcast (To create a new job class, use the make:job Artisan command)
    -- php artisan queue:work --tries=3 (To specify the maximum number of times a job should be attempted, you may use the --tries switch on the queue:work command)
    -- php artisan queue:work --timeout=30 (To specify the maximum number of seconds a child process can run, you may use the --timeout switch on the queue:work command)
    -- php artisan queue:batches-table (To generate a migration that creates the batches table, use the queue:batches-table command)
    -- php artisan queue:work (To start the worker, you may use the queue:work command)
    -- php artisan queue:work -v (To increase the verbosity of the worker's output, you may use the -v option)
    -- php artisan queue:listen (To start the worker in "listen" mode, you may use the queue:listen command)
    -- php artisan queue:work redis (To start the worker for a specific connection, you may use the queue:work command with the connection name as the first argument)
    -- php artisan queue:work redis --queue=emails (To start the worker for a specific queue, you may use the queue:work command with the queue name as the first argument)
    -- php artisan queue:work --once (To process only the next job on the queue, you may use the --once switch on the queue:work command)
    -- php artisan queue:work --max-jobs=1000 (To process only the next job on the queue, you may use the --once switch on the queue:work command)
    -- php artisan queue:work --stop-when-empty (To stop the worker when the queue is empty, you may use the --stop-when-empty switch on the queue:work command)
    -- php artisan queue:work --max-time=3600 (To stop the worker after a specified amount of time, you may use the --max-time switch on the queue:work command)
    -- php artisan queue:work --sleep=3 (To specify the number of seconds to wait before polling for new jobs, you may use the --sleep switch on the queue:work command)
    -- php artisan queue:work --queue=high,low (To specify the queues the worker should listen on, you may use the --queue switch on the queue:work command)
    -- php artisan queue:restart (To restart all of the queue workers, you may use the queue:restart command)
    -- php artisan queue:work --timeout=60 (To specify the maximum number of seconds a child process can run, you may use the --timeout switch on the queue:work command)
    -- php artisan queue:failed-table (To generate a migration that creates the failed_jobs table, use the queue:failed-table command)
    -- php artisan queue:work redis --tries=3 (To specify the maximum number of times a job should be attempted, you may use the --tries switch on the queue:work command)
    -- php artisan queue:work redis --tries=3 --backoff=3 (To specify the number of seconds to wait before retrying a job, you may use the --backoff switch on the queue:work command)
    -- php artisan queue:failed (To view all of your failed jobs, you may use the queue:failed command)
    -- php artisan queue:retry --queue=name (To retry all of the failed jobs for a given queue, you may use the queue:retry command)
    -- php artisan queue:retry all (To retry all of the failed jobs, you may use the queue:retry command)
    -- php artisan queue:retry 5 (To retry a specific failed job, you may use the queue:retry command)
    -- php artisan queue:forget 5 (To delete a specific failed job, you may use the queue:forget command)
    -- php artisan queue:flush (To delete all of the failed jobs, you may use the queue:flush command)
    -- php artisan queue:prune-failed (To delete all of the failed jobs that are older than a given number of days, you may use the queue:prune-failed command)
    -- php artisan queue:prune-failed --hours=48 (To delete all of the failed jobs that are older than a given number of hours, you may use the queue:prune-failed command)
    -- php artisan queue:work --daemon (To run the worker in daemon mode, you may use the --daemon switch on the queue:work command)

    ## Storing Failed Jobs In DynamoDB
    -- composer require aws/aws-sdk-php (To get started, install the aws/aws-sdk-php Composer package)

    ## Clearing Jobs From Queues
    -- php artisan queue:clear (To delete all of the jobs from a given queue, you may use the queue:clear command)
    -- php artisan queue:clear --queue=emails (To delete all of the jobs from a given queue, you may use the queue:clear command)
    -- php artisan queue:clear redis --queue=emails (To delete all of the jobs from a given queue, you may use the queue:clear command)

    ## Monitoring Your Queues 
    -- php artisan queue:monitor redis:default,redis:deployments --max=100

32. Task Scheduling
    -- php artisan schedule:list (To view all of your scheduled tasks, you may use the schedule:list command)
    -- php artisan schedule:interrupt (To interrupt a scheduled task, you may use the schedule:interrupt command)
    -- php artisan schedule:run (To run your scheduled tasks, you may use the schedule:run command)
    -- php artisan schedule:work (To run the scheduler in the background, you may use the schedule:work command)

33. Policies
    -- php artisan make:policy PostPolicy (To create a new policy, use the make:policy Artisan command)
    -- php artisan make:policy PostPolicy --model=Post (To create a new policy for a model, use the --model option)

34. Database
    -- php artisan migrate (To run all of your outstanding migrations, execute the migrate Artisan command)
    -- php artisan db (To view a list of all available Artisan commands, you may use the list command)
    -- php artisan db mysql (To view a list of all available Artisan commands, you may use the list command)
    -- php artisan db:show (To view a list of all of the database connections configured for your application, you may use the db:show command)
    -- php artisan db:show --database=pgsql (You may specify which database connection should be inspected by providing the database connection name to the command via the --database option)
    -- php artisan db:show --counts --views (If you would like to include table row counts and database view details within the output of the command, you may provide the --counts and --views options, respectively)
    -- php artisan db:table users (To view the table definition for a given table, you may use the db:table command) 
    -- php artisan db:monitor --databases=mysql,pgsql --max=100 (To monitor your database connections, you may use the db:monitor command)
    -- php artisan migrate:install (To create the migration repository, you may use the migrate:install Artisan command)
    -- php artisan make:migration create_flights_table (To create a new migration, use the make:migration Artisan command)
    -- php artisan make:migration add_votes_to_users_table --table=users (To create a migration that modifies an existing table, use the --table option)
    -- php artisan schema:dump (To dump your database schema, you may use the schema:dump Artisan command)
    -- php artisan schema:dump --prune (To dump your database schema without comments, you may use the --prune option)
    -- php artisan schema:dump --database=testing --prune (To dump your database schema without comments, you may use the --prune option)
    -- php artisan migrate (To run all of your outstanding migrations, execute the migrate Artisan command)
    -- php artisan migrate:status (To view the status of your migrations, you may use the migrate:status Artisan command)
    -- php artisan migrate --pretend (To run the migrations without actually running them, you may use the --pretend option)
    -- php artisan migrate --isolated (To run the migrations in isolation, you may use the --isolated option)
    -- php artisan migrate --force (To run the migrations without a prompt, you may use the --force option)
    -- php artisan migrate:rollback (To roll back the latest migration operation, you may use the migrate:rollback command)
    -- php artisan migrate:rollback --step=5 (To roll back the last five migrations, you may use the --step option)
    -- php artisan migrate:rollback --batch=3 (To roll back all of the migrations that were run within a given batch, you may use the --batch option)
    -- php artisan migrate:rollback --pretend (To roll back the migrations without actually running them, you may use the --pretend option)
    -- php artisan migrate:reset (To roll back all of your application's migrations, you may use the migrate:reset command)
    -- php artisan migrate:refresh (To roll back all of your migrations and then execute the migrate command, you may use the migrate:refresh command)
    -- php artisan migrate:refresh --seed (To roll back all of your migrations and then execute the migrate:refresh command, you may use the --seed option)
    -- php artisan migrate:refresh --step=5 (To roll back all of your migrations and then execute the migrate command, you may use the migrate:refresh command)
    -- php artisan migrate:fresh (To drop all tables and re-run all migrations, you may use the migrate:fresh command)
    -- php artisan migrate:fresh --seed (To drop all tables and re-run all migrations, you may use the migrate:fresh command)

35. Seeder
    -- php artisan make:seeder UserSeeder (To create a new seeder, use the make:seeder Artisan command)
    -- php artisan db:seed (To seed your database, you may use the db:seed Artisan command)
    -- php artisan db:seed --class=UserSeeder (To seed a specific seeder class, you may use the --class option)
    -- php artisan migrate:fresh --seed (To drop all tables and re-run all of your migrations and seeds, you may use the migrate:fresh command)
    -- php artisan migrate:fresh --seed --seeder=UsersTableSeeder (To drop all tables and re-run all of your migrations and seeds, you may use the migrate:fresh command)
    -- php artisan db:seed --force (To seed your database without a prompt, you may use the --force option)

36. Redis
    -- composer require predis/predis (To get started, install the predis/predis Composer package)
    -- php artisan redis:command (To view a list of all available Artisan commands, you may use the list command)
    -- php artisan redis:command --scan (To view a list of all available Artisan commands, you may use the list command)

37. Eloquent ORM
    -- php artisan make:model Flight (To create a new model, use the make:model Artisan command)
    -- php artisan make:model Flight --migration (To create a new model and its migration, use the --migration or -m option)
    -- php artisan model:show Flight (To view a list of all available Artisan commands, you may use the list command)

    ## Generate a model and a FlightFactory class...
    -- php artisan make:model Flight --factory (To create a new model and its factory, use the --factory)
    -- php artisan make:model Flight -f (To create a new model and its factory, use the -f option)
 
    ## Generate a model and a FlightSeeder class...
    -- php artisan make:model Flight --seed (To create a new model and its seeder, use the --seed option)
    -- php artisan make:model Flight -s (To create a new model and its seeder, use the -s option)
    
    ## Generate a model and a FlightController class...
    -- php artisan make:model Flight --controller (To create a new model and its controller, use the --controller option)
    -- php artisan make:model Flight -c (To create a new model and its controller, use the -c option)
    
    ## Generate a model, FlightController resource class, and form request classes...
    -- php artisan make:model Flight --controller --resource --requests (To create a new model and its controller, resource, requests use the --controller --resource --requests option)
    -- php artisan make:model Flight -crR (To create a new model and its controller, resource, requests use the -c option)
    
    ## Generate a model and a FlightPolicy class...
    -- php artisan make:model Flight --policy (To create a new model and its policy, use the --policy or -p option)
    
    ## Generate a model and a migration, factory, seeder, and controller...
    -- php artisan make:model Flight -mfsc (To create a new model and its migration, factory, seeder, and controller, use the --migration, --factory, --seeder, and --controller options)
    
    ## Shortcut to generate a model, migration, factory, seeder, policy, controller, and form requests...
    -- php artisan make:model Flight --all (To create a new model and its migration, factory, seeder, policy, controller, and form requests, use the --all option)
    
    ## Generate a pivot model...
    -- php artisan make:model Member --pivot (To create a new pivot model, use the --pivot option)
    -- php artisan make:model Member -p (To create a new pivot model, use the -p option)

    -- php artisan model:prune --pretend (To delete all of the models that don't have a corresponding database table, you may use the model:prune command)

38. Scopes
    -- php artisan make:scope AncientScope (To create a new scope, use the make:scope Artisan command)
    -- php artisan make:scope AncientScope --model=Flight (To create a new scope for a model, use the --model option)

39. Observers
    -- php artisan make:observer UserObserver --model=User

40. Casts
    -- php artisan make:cast Json (To create a new cast, use the make:cast Artisan command)
    -- php artisan make:cast Hash --inbound (To create a new cast that is only applied when setting a value on the model, use the --inbound option)

41. Resources
    -- php artisan make:resource UserResource (To create a new resource, use the make:resource Artisan command)
    -- php artisan make:resource User --collection (To create a new resource collection, use the --collection option)
    -- php artisan make:resource UserCollection (To create a new resource collection, use the make:resource Artisan command)

42. Factories
    -- php artisan make:factory FlightFactory (To create a new factory, use the make:factory Artisan command)

43. Testing
    -- php artisan make:test UserTest (To create a new test, use the make:test Artisan command)
    -- php artisan make:test UserTest --unit (To create a new unit test, use the --unit option)
    -- php artisan make:test UserTest --pest (To create a new Pest test, use the --pest option)
    -- php artisan make:test UserTest --unit --pest (To create a new unit test, use the --unit option)
    -- php artisan test (To run your application's tests, you may use the test Artisan command)
    -- php artisan test --testsuite=Feature --stop-on-failure (To run a specific test suite, you may use the --testsuite option  and --stop-on-failure)
    -- php artisan test --coverage (To generate a code coverage report, you may use the --coverage option)
    -- php artisan test --coverage --min=80.3 (To generate a code coverage report, you may use the --coverage option)
    -- php artisan test --profile (To generate a performance profile, you may use the --profile option)
