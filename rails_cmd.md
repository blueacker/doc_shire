rails about                            # List versions of all Rails frameworks and the environment
rails stats                              # Report code statistics (KLOCs, etc) from the application or engine
rails test                                # Runs all tests in test folder except system ones
rails routes                           # Print out all defined routes in match order, with names
rails secret                            # Generate a cryptographically secure secret key (for cookie sessions)
rails test:db                          # Run tests quickly, but also reset db
rails test:system                  # Run system tests only
rails notes                             # Enumerate all annotations (use notes:optimize, :fixme, :todo for focus)
rails notes:todo                   # 查看特定类型的注解，如TODO. 注意，注解的名称是小写形式
rails notes:custom ANNOTATION=BUG  # 查看自定义的note
rails runner "Model.long_running_method"                          # 不进入rails console就执行对应的命令
rails runner -e production "Model.long_running_method"  # 在指定环境运行命令
rails runner lib/code_to_be_run.rb                                           # 运行文件代码

>  默认情况下，`rails notes` 在 `app`、`config`、`db`、`lib` 和 `test` 目录中搜索。如果想搜索其他目录，可以通过 `config.annotations.register_directories` 选项配置。
>  config.annotations.register_directories("spec", "vendor")
>
>  还可以通过 `SOURCE_ANNOTATION_DIRECTORIES` 环境变量指定，目录之间使用逗号分开:
>  export SOURCE_ANNOTATION_DIRECTORIES='spec,vendor'


rails restart                           # Restart app by touching tmp/restart.txt
rails middleware                  # Prints out your Rack middleware stack



- [ ] rails active_storage:install          # Copy over the migration needed to the application
- [ ] rails app:template                       # Applies the template supplied by LOCATION=(/path/to/template) or URL
- [ ] rails app:update                          # Update configs and some other initially generated files (or use just update:configs or update:bin)
- [x] rails assets:clean[keep]              # Remove old compiled assets
- [x] rails assets:clobber                     # Remove compiled assets
- [ ] rails assets:environment           # Load asset compile environment
- [x] rails assets:precompile              # Compile all the assets named in config.assets.precompile
- [ ] rails cache_digests:dependencies                # Lookup first-level dependencies for TEMPLATE (like messages/show or comments/_comment.html)
- [ ] rails cache_digests:nested_dependencies  # Lookup nested dependencies for TEMPLATE (like messages/show or comments/_comment.html)



### rails:db

- [x] rails db:create                                # Creates the database from DATABASE_URL or config/database.yml for the current RAILS_ENV (use db:create:all to create all databases in the config). Without RAILS_ENV or when RAILS_ENV is development, it defaults to creating the development and test databases
- [ ] rails db:data:dump                        # Dump contents of database to db/data.extension (defaults to yaml)
- [ ] rails db:data:dump_dir                 # Dump contents of database to curr_dir_name/tablename.extension (defaults to yaml)
- [ ] rails db:data:load                          # Load contents of db/data.extension (defaults to yaml) into database
- [ ] rails db:data:load_dir                    # Load contents of db/data_dir into database
- [x] rails db:drop[:all]                           # Drops the database from DATABASE_URL or config/database.yml for the current RAILS_ENV (use ` db:drop:all` to drop all databases in the config). Without RAILS_ENV or when RAILS_ENV is development, it defaults to dropping the development and test databases
- [ ] rails db:dump                                # Dump schema and data to db/schema.rb and db/data.yml
- [ ] rails db:environment:set             # Set the environment value for the database
- [ ] rails db:fixtures:load                    # Loads fixtures into the current environment's database
- [ ] rails db:load                                   # Load schema and data from db/schema.rb and db/data.yml
- [x] rails db:migrate                             # Migrate the database (options: VERSION=x, VERBOSE=false, SCOPE=blog)
- [x] rails db:migrate:status                 # Display status of migrations

- [x] rails db:rollback                             # Rolls the schema back to the previous version (specify steps w/ STEP=n)

- [x] rails db:schema:cache:clear        # Clears a db/schema_cache.yml file

- [x] rails db:schema:cache:dump      # Creates a db/schema_cache.yml file

- [x] rails db:schema:dump                 # Creates a db/schema.rb file that is portable against any DB 

  supported by Active Record

- [x] rails db:schema:load                     # Loads a schema.rb file into the database

- [x] rails db:seed                                   # Loads the seed data from db/seeds.rb

- [x] rails db:setup                                  # Creates the database, loads the schema, and initializes with the seed 

  data (use db:reset to also drop the database first)

- [x] rails db:structure:dump                # Dumps the database structure to db/structure.sql

- [x] rails db:structure:load                   # Recreates the databases from the structure.sql file

- [x] rails db:version                               # Retrieves the current schema version number

---


rails initializers                        # Print out all defined initializers in the order they are invoked by Rails
rails log:clear                           # Truncates all/specified *.log files in log/ to zero bytes (specify which logs with LOGS=test,development)

rails time:zones[country_or_offset]      # List all time zones, list by two-letter country code (`rails time:zones[US]`), or list by UTC offset (`rails time:zones[-8]`)
rails tmp:clear                          # tmp:cache:clear, tmp:sockets:clear, tmp:screenshots:clear
rails tmp:create                       # Creates tmp directories for `cache`, `sockets`, and `pids`

rails yarn:install                       # Install all JavaScript dependencies as specified via Yarn
rails dev:cache                         # Toggle development mode caching on/off



---

rails generate task                  # Generate self defined task as above

