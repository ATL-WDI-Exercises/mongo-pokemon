# Mongo Pokemon Lab

Time for some Pokemon query fun in the MongoDB console...

* First, grab the `seed.json` file from your repo.
* Next, import it into MongoDB using the `mongoimport` feature. Make sure you're in the directory that includes the file before running this command in the terminal:

`mongoimport -d pokemon -c pokemons --jsonArray < seed.json`


<br>

## Helpful Mongo Commands

| Command                       | Description                                |
|:----------------------------- |:------------------------------------------ |
| `brew services`               | Start or Stop MongoDBserver                |
| `mongo`                       | Start a MongoDB Shell (client)             |
| `show dbs`                    | Show a list of Databases                   |
| `use <database_name>`         | Set your current database                  |
| `db`                          | Verify your current database               |
| `show collections`            | Show the collections in the current DB     |
| `db.<collection_name>.find()` | Query a particular collection              |
| `.pretty()`                   | Make a JSON Object 'pretty'                |

Also, be sure to check the [MongoDB docs](https://www.mongodb.org).

<br>

## Pokemon Queries

__STEP 1__ - Print all the Pokemon names to the MongoDB console like so `name: <name_of_pokemon>`.
<br>

__STEP 2__ - Find the Pokemon with the name "Mew".
<br>

__STEP 3__ - How many Pokemons are 87.5 male?
<br>

__STEP 4__ - How many Pokemons have `ice : "2"`?
<br>

__STEP 5__ - How many Pokemons have `ice : "2"` AND `female : "12.5"`?
<br>

__STEP 6__ - How many Pokemons have `"speed": "60"` OR `"type" : "Grass"`?
<br>

__STEP 7__ - How many have BOTH `"speed": "60"` AND `"type" : "Grass"`?
<br>

__STEP 8__ - Create a new collection named `Schmittymons` and add a new `Schmittymon` with the folowing traits:

* **name**: Schmitty
* **img**: http://40.media.tumblr.com/tumblr_m78kl3JexC1rag2cto1_500.jpg
* **tutor**:
	* **name**: grass pledge
	* **gen**: V
* **happiness**: 99
