# PokemonGoMaps
Heat maps of the locations of different types of Pokemon in Paris, from the PokemonGo game.

Code in R.


1. GridPatternSearch

First, a grid pattern search was done using pokvision.exe (today out). The search was only done around Paris. A grid pattern of 13 by 13 is done, and Pokemons around each center of these squares are searched.
The first program generates a .sh file, 'allCommandLines.sh'.


2. allCommandLines.sh

The .sh will launch every 15 minutes with Windows crontab.


3. GetTablePokemonLocations

Data generated by allCommandLines.sh need to be cleaned in preparation for the maps and study.
The table tablePokemonLocations includes the following columns:
  - namePokemon: name of the pokemon
  - latitude
  - longitude
  - date
  - hour
  - squareLong: the longitude-square into which the location belongs
  - squareLat: the latitude-square into which the location belongs
At the end of the program, the table is saved.


4. HeatMapPokemon

With the use of tablePokemonLocations, a heat map for each Pokemon can be made.