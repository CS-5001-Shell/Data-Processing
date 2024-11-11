# Practice with JSON and Data Processing

## Getting Started
For this assignment, you will write a program that will load data from a JSON file and perform some processing on the data.

You will work with the [IMDB](https://www.imdb.com/) movies dataset available
from [Kaggle](https://www.kaggle.com/). To prepare for this assignment you will
need to download the JSON version of the dataset available here:
[https://www.kaggle.com/datasets/gorochu/complete-imdb-movies-dataset](https://www.kaggle.com/datasets/gorochu/complete-imdb-movies-dataset).
(requires Kaggle login)

To prepare for the assignment, familiarize yourself with the dataset. You will work with the file in movie.json/movie.json. 

You will need to extract the title, rating, year, users_rating, and runtime for each movie.

You will need to import the json module to load the JSON data into a dictionary. Refer to the following documentation: [https://docs.python.org/3/library/json.html](https://docs.python.org/3/library/json.html)

## Requirements
Write a program that will load the data into a list of `Movie` objects. For full
credit, you must implement the following:

- a `Movie` class that includes, at minimum, the following properties: title,
  rating, year, users_rating, and runtime 
- a `MovieList` class that includes the following methods:

  - `get_years`: returns a list of unique years, sorted by year. There are several years that appear multiple times in the dataset but should appear only once in your output.
  * `get_long_movies`: returns a list of all titles of movies that have a runtime
    greater than 200 minutes, sorted by title.
  * `get_common_rating`: returns the most common rating -- that is the rating (e.g., PG-13, R) that appears most often.
  * `get_low_rated_count`: returns the count of user_ratings that are lower than 4.
  * `get_mid_rated_count`: returns the count of user_ratings that are between 4
    and 7, inclusive of both 4 and 7.
  * `get_top_rated_count`: returns the count of user_ratings that are greater than 7 . 

Below is an example of what your output will look like. 

```python
Unique Years

------------

 [1903, 1908, 1909, 1910, 1911, 1912, 1913, 1914, 1915, 1916, 1917, 1918, 1919, 1920, 1921, 1922, 1923, 1924, 1925, 1926, 1927, 1928, 1929, 1930, 1931, 1932, 1933, 1934, 1935, 1936, 1937, 1938, 1939, 1940, 1941, 1942, 1943, 1944, 1945, 1946, 1947, 1948, 1949, 1950, 1951, 1952, 1953, 1954, 1955, 1956, 1957, 1958, 1959, 1960, 1961, 1962, 1963, 1964, 1965, 1966, 1967, 1968, 1969, 1970, 1971, 1972, 1973, 1974, 1975, 1976, 1977, 1978, 1979, 1980, 1981, 1982, 1983, 1984, 1985, 1986, 1987, 1988, 1989, 1990, 1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998, 1999, 2000, 2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020]


Long Movies

-----------

 [****, A Woman in Grey, Abraham & Sarah, the Film Musical, Ace Drummond, Adventures of Captain Marvel, Adventures of Red Ryder, Adventures of the Flying Cadets, Atom Man vs. Superman, Batman, Batman and Robin, Battling with Buffalo Bill, Beatrice Fairfax, Ben-Hur, Blackhawk: Fearless Champion of Freedom, Blake of Scotland Yard, Blood and Honor, Brenda Starr, Reporter, Buck Rogers, Burn 'Em Up Barnes, Captain America, Captain Midnight, Captain Video, Master of the Stratosphere, Chelsea Girls, Chick Carter, Detective, Clancy of the Mounted, Custer's Last Stand, Danger Island, Dante's Inferno, Daredevils of the Red Circle, Darkest Africa, Deadwood Dick, Detective Lloyd, Dick Tracy, Dick Tracy Returns, Dick Tracy vs. Crime, Inc., Dick Tracy's G-Men, Don Winslow of the Coast Guard, Don Winslow of the Navy, Drums of Fu Manchu, Early Women Filmmakers, Exodus, Fighting with Kit Carson, Finger Prints, Flaming Frontiers, Flash Gordon, Flash Gordon's Trip to Mars, G-Men vs. The Black Dragon, Gang Busters, Gettysburg, Giant, Gods and Generals, Gone with the Wind, Gordon of Ghost City, Gunfighters of the Northwest, Hamlet, Hands Up, Haunted Harbor, Hawk of the Wilderness, Heaven's Gate, Her Dangerous Path, Heroes of the West, Holt of the Secret Service, It's a Mad Mad Mad Mad World, Jack Armstrong, Jungle Jim, Jungle Menace, Jungle Mystery, Jungle Queen, Jungle Raiders, Junior G-Men, Junior G-Men of the Air, KSI vs. Logan Paul II, King Lear, King of the Congo, King of the Royal Mounted, King of the Texas Rangers, King of the Wild, Law of the Wild, Lightning Hutch, Lipstick and Bullets, Lost City of the Jungle, Lucille Love: The Girl of Mystery, Malcolm X, Mandrake, the Magician, Manhunt of Mystery Island, Marshal Law: Reconciliation, Mutantz, Nazis and Zombies, Mysterious Doctor Satan, Mystery Mountain, Mystery of the River Boat, Nan of the North, Once Upon a Time in America, Overland Mail, Patria, Perils of Nyoka, Perils of Pauline, Perils of the Royal Mounted, Perils of the Wild, Pirate Treasure, Pirates of the High Seas, Psychotic State, Radio Patrol, Raiders of Ghost City, Red Barry, Renaldo and Clara, Riders of Death Valley, Rightways Down, River of Fundament, Roar of the Iron Horse - Rail-Blazer of the Apache Trail, Robinson Crusoe of Clipper Island, Rooster Teeth: Best of RT Shorts and Animated Adventures, Rory Gallagher: Live at Montreux, Rustlers of Red Dog, SOS Coast Guard, Scouts to the Rescue, Sea Raiders, Secret Agent X-9, Secret Agent X-9, Secret Service in Darkest Africa, Shadow of Chinatown, Son of Geronimo: Apache Avenger, Spy Smasher, Star Trek III: Redemption, Superman, Tailspin Tommy, Tailspin Tommy in The Great Air Mystery, Tarzan the Tiger, Terror Trail, Tex Granger: Midnight Rider of the Plains, The Ace of Scotland Yard, The Adventures of Frank Merriwell, The Adventures of Rex and Rinty, The Adventures of Robinson Crusoe, The Adventures of Sir Galahad, The Adventures of Smilin' Jack, The Airmail Mystery, The Amazing Exploits of the Clutching Hand, The Avenging Arrow, The Beloved Adventurer, The Black Coin, The Call of the Savage, The Carter Case, The Cremaster Cycle, The Desert Hawk, The Devil Horse, The Fighting Devil Dogs, The Fighting Marines, The Galloping Ghost, The Godfather: Part II, The Gospel of Luke, The Great Adventures of Captain Kidd, The Great Alaskan Mystery, The Great Gamble, The Greatest Adventure: The Book of Dragons, The Greatest Story Ever Told, The Green Archer, The Green Hornet, The Green Hornet Strikes Again!, The Hazards of Helen, The Hope Diamond Mystery, The House Without a Key, The Hurricane Express, The Iceman Cometh, The Irishman, The Jade Box, The King of the Kongo, The Last Frontier, The Last of the Mohicans, The Lightning Raider, The Lightning Warrior, The Lone Defender, The Lone Ranger, The Lone Ranger Rides Again, The Lost City, The Lost Jungle, The Lost Special, The Lurking Peril, The Marvel Experience, The Masked Rider, The Master Key, The Master Key, The Miracle Rider, The Monster and the Ape, The Mysterious Mr. M, The Mysterious Pilot, The Mystery Squadron, The Mystery of the Double Cross, The New Adventures of J. Rufus Wallingford, The New Adventures of Tarzan, The Oregon Trail, The Painted Stallion, The Phantom, The Phantom Creeps, The Phantom Empire, The Phantom Rider, The Phantom of the Air, The Purple Monster Strikes, The Red Rider, The Republic, The Return of Chandu, The Roaring West, The Royal Mounted Rides Again, The Scarlet Horseman, The Shadow, The Shadow of the Eagle, The Ten Commandments, The Three Musketeers, The Tiger's Trail, The Timber Queen, The Trail of the Octopus, The Trey o' Hearts, The Valley of Vanishing Men, The Vanishing Legion, The Vanishing Shadow, The Vigilante: Fighting Hero of the West, The Vigilantes Are Coming, The Whispering Shadow, The Wolf Dog, The Works and Days (of Tayoko Shiojiri in the Shiotani Basin), Tim Tyler's Luck, Undersea Kingdom, War and Peace, West Side Avenue, White Eagle, Who Pays?, Wild West Days, Winners of the West, Young Eagles, Zombie Horror Fright Fest!, Zorro Rides Again, Zorro's Black Whip, Zorro's Fighting Legion]


Most Common Rating

------------------

 R


Number of Movies with Rating Lower than 4

-----------------------------------------

 6213



Number of Movies with Rating 4 - 7

----------------------------------

 45415



Number of Movies with Rating Higher than 7

------------------------------------------

 10428
 
```


In addition to the functionality above, your grade will depend upon the design of your `Movie` class and the overall design of your solution. You are welcome to use additional classes and/or methods. 

### Hints
1. Some of the entries may have a value of None for the rating, year,
   users_rating, and/or runtime. You will need to handle these appropriately.
   These entries should still be included in your dataset; however, an entry
   that does not include, for example, a year, could still appear as a long
   movie but would not affect the `get_years` functionality.
2. If the runtime is in excess of 999 min it may have a ',' (e.g., 1,487 min).
   You will need to handle these by removing the ',' and treating the remaining
   digits as an `int`.
3. To sort your output, you may find it useful to implement methods `__lt__`, `__gt__`, etc in your Movie class. See: [https://www.programiz.com/python-programming/operator-overloading](https://www.programiz.com/python-programming/operator-overloading)

**Submission:** The main functionality of your program must be submitted in a file
called *movie_stats.py* in your Lab 10 repository. Your `MovieList` class must be in file called *movie_list.py*. It is acceptable to include
other files if you choose to implement your classes in separate files.

## Assignment Submission

To earn credit for this assignment you must commit all of your changes to your GitHub repository prior to the deadline. It is strongly recommended that you commit your changes regularly. Do not wait until you complete all parts of the assignment to upload your (partial) solution.

Step 1 - *Stage Changes*: Select the Source Control icon in the VSCode left menu. In the Changes section, click the + to *Stage All Changes*.

Step 2 - Commit Message: In the text box that says Message enter a meaningful message that describes the change you just completed.

Step 3 - *Commit & Push*: Select the down arrow in the blue box that says Commit. Choose *Commit & Push*.

Step 4 - Verify: Visit the repository on GitHub to confirm that your changes were uploaded successfully