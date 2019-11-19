---------------------------------------------------------------------
************************ Liri Bot App *******************************
---------------------------------------------------------------------

To see a short video demonstating this app please follow this link: https://youtu.be/kjfuRGyqvuw

This is a simple app which allows the user to query three possible APIs:

*OMDB (A free API ala IMDB)
*Bandsintown.com (A website which allows the user to find nearby concerts)
*Spotify (A famous music streaming site)

This app allows the user to request info from these sites and the prsents 
them in a simple to read format. It is a quick and easy CLI app, and might 
work well for someone who is often doing work on the command line and enjoys
movies and music. 

The app is organized as follows: There is a main javascript file conatining
the brunt of code being used in this app. Within that file there are four main 
functions being implemented, which the user can select from on the command line. 
Each of these corresponds to the API the user wishes to query. The commands are 
as follows: 

"node liri.js concert-this '<artist/band name here>'"
    Using the "bandsintown.com" API this command will allow the user to input an artist 
    or band into the command line and liri app will return an up to date schedule of t
    his artist's upcoming concerts. 

"node liri.js spotify-this-song '<song name here>'"
    Using the spotify API this command will request relevant data to a chosen song
    and return the following info: 
       * Artist(s)
       * The song's name
       * A preview link of the song from Spotify
       * The album that the song is from

"node liri.js movie-this '<movie name here>'"
    Using the OMDB API this command will request relevant data to a chosed movie 
    and return the following info: 
        * Title of the movie.
        * Year the movie came out.
        * IMDB Rating of the movie.
        * Rotten Tomatoes Rating of the movie.
        * Country where the movie was produced.
        * Language of the movie.
        * Plot of the movie.
        * Actors in the movie.


'node liri.js do-what-it-says'
    This command will run the "spotify-this" command and check the random.txt file 
    for a song to reuqest data for. A future release of this app might truly randomise
    this and search spotify completely randoly. 

Each of these functions is then used in a switch statement which checks the two arguments
the user inputs to determine which function to run and what to search for when running. 

Finally, in order for a user to run this app, they will need to install the create a dotenv
file with their own spotify keys. If the user ever decides to push this app anywhere which 
it can be publically viewed, it would be advisable to not include the dotenv file. In addition 
to this, the user will also need to to run an npm install within this file, the following dependencies
will be installed: 
    
    "axios": "^0.19.0",
    "dotenv": "^8.2.0",
    "moment": "^2.24.0",
    "node-spotify-api": "^1.1.1"

Again to see a short video demonstating this app please follow this link: https://youtu.be/kjfuRGyqvuw

