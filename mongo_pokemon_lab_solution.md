##Mongo Pokemon Lab

Time for some Pokemon query fun in the MongoDB console... 

* First, grab the `seed.json` file from your repo.
* Next, import it into MongoDB using the `mongoimport` feature. Make sure you're in the directory that includes the file before running this command in the terminal:

`mongoimport -d test -c pokemons --jsonArray < seed.json`


<br>

##Helpful Mongo Commands
#####To start mongod
`brew services`
#####To start the MongoDB Shell
 `mongo`
 
#####To list your databases

`show dbs`

#####To choose a database

`use <database_name>`

#####To verify your current database

`db`

#####To show the collections in that database
`show collections`

#####To query the particular collection in that database

`db.<collection_name>.find()`

#####To make a JSON Object 'pretty'

`.pretty()`

Also, be sure to check the [MongoDB docs](https://www.mongodb.org).


<br>

##Pokemon Queries

__STEP 1__ - Print all the Pokemon names to the MongoDB console like so `name: <name_of_pokemon>`.


SOLUTION: `db.pokemons.find().forEach( function(pokemon) {print ("name: " + pokemon.name); } );` 

__STEP 2__ - Find the Pokemon with the name "Mew".

SOLUTION: `db.pokemons.find({name: "Mew"});`

__STEP 3__ - How many Pokemons are 87.5 male?

SOLUTION: `db.pokemons.find({"misc.sex.male":87.5}).count()`

__STEP 4__ How many Pokemons have `ice : "2"`?

SOLUTION: `db.pokemons.find({"damages.ice": "2"}).count()`

__STEP 5__ How many Pokemons have `ice : "2"` AND `female : "12.5"`?

SOLUTION: `db.pokemons.find({$and: [{"damages.ice": "2"}, {"misc.sex.female":"12.5"}]}).count()`

__STEP 6__ How many Pokemons have `"speed": "60"` OR `"type" : "Grass"`?

SOLUTION: `db.pokemons.find({$or: [{"stats.speed": "60"}, {"type":"Grass"}]}).count()`

__STEP 7__ How many have BOTH `"speed": "60"` AND `"type" : "Grass"`?

SOLUTION: `db.pokemons.find({$and: [{"stats.speed": "60"}, {"type":"Grass"}]}).count()`

__STEP 8__ Create a new collection named `Schmittymons` and add a new `Schmittymon` with the folowing traits:

* **name**: Schmitty
* **img**: http://40.media.tumblr.com/tumblr_m78kl3JexC1rag2cto1_500.jpg
* **tutor**: 
	* **name**: grass pledge
	* **gen**: V
* **happiness**: 99







 