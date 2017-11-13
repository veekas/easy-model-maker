# Easy Model Maker

This repo is just an abstraction of the [sequelize-auto](https://github.com/sequelize/sequelize-auto) library. Currently sequelize-auto breaks with with the latest version of pg, so I made this as a stopgap measure while they update the package. Easy Model Maker is a separate repo so you don't have to clutter up actual projects with out-of-date packages.

You can read more about sequelize-auto and how to customize it beyond what I've laid out [here](https://github.com/sequelize/sequelize-auto).

## Directions

1. create your database. example:

```s
createdb database_name
```

2. add tables and columns to your database in [Postico](https://eggerapps.at/postico/) or similar tool
3. enter the following in the command line (replacing 'database_name' with your db name)

```s
sequelize-auto -o ./models -h localhost -d database_name -e postgres
```

4. you should now have your auto-generated models saved in the ./models folder. Copy them to your project directory. That's it!
