# Location Resolver Challenge

## Overview

At Latana we conduct surveys all over the world. One way we find participants is through mobile advertising
using [RTB](https://en.wikipedia.org/wiki/Real-time_bidding). This can involve processing a large amount of traffic
(thousands of requests per second), and one of the challenges we face is to ensure we can do this efficiently.

For instance, we may need to decide whether to show a survey to a user. One approach we can use is to filter requests
using location information. For each request, we resolve the location (a
[latitude / longitude](https://en.wikipedia.org/wiki/Geographic_coordinate_system#Latitude_and_longitude) coordinate)
to a country or specific region (e.g. a US county). We can then filter requests according to whether we have surveys in
particular countries or regions.

We would like you to implement a way of resolving locations (coordinates) to US counties. To assist you, we have
prepared an outline project and a [shapefile](https://en.wikipedia.org/wiki/Shapefile) containing some reference data.
Your solution can trade-off between speed (time taken to resolve the location) and accuracy, however when a location
is resolved, it should be correct.

## Instructions

1. Create a copy of the `location-resolver-challenge` public repository. *Please do not fork the source repo directly as
   you cannot restrict access to a forked public repository*.
    - [Create a new private repository](https://help.github.com/en/articles/creating-a-new-repository)
      called `location-resolver-challenge`
    - [Duplicate the source repository](https://help.github.com/en/articles/duplicating-a-repository) (remember to
      replace your `{exampleuser}` in the command below)
    ```
    $ git clone --bare git@github.com:DaliaResearch/location-resolver-challenge.git
    $ cd location-resolver-challenge.git
    $ git push --mirror git@github.com:{exampleuser}/location-resolver-challenge.git
    $ cd .. 
    $ rm -rf location-resolver-challenge.git
    ```
    - Clone the duplicated repo
    ```
    $ git clone git@github.com:{exampleuser}/location-resolver-challenge.git
    ```

1. Implement your solution ...
    - Your solution should implement the `CountyResolver` interface.
    - We have included a `BasicCountyResolver` as an example.
    - Include your new tests within the `ResolverTest` class to demonstrate the performance of your solution.
    - The project should compile using maven (i.e. `mvn clean install`).

1. Include any instructions (or other useful comments) in a clearly marked text file.

1. Commit your changes locally then push to the remote repository.

1. Add the user **pc256**
   as [collaborator to the repository](https://help.github.com/en/articles/inviting-collaborators-to-a-personal-repository)
   .

1. Drop us an email letting us know you've finished.

## Other Useful Information

- The `ResolverTest` runs using a small locations file (`locations-small.csv`). If you get things running really
  quickly, try the full `locations.csv` file!
- Feel free to use external libraries so long as your solution cleanly runs using maven.
- Document your progress, successes and failures using the git commits.
- Use Java 11 and structure your code in a clear manner.
- If you would like to view the shapefile you can do so using [QGIS](https://www.qgis.org/en/site/) 
  (_though this is not required for the challenge_)
- You can find documentation for the geotools libraries at https://docs.geotools.org/

### Happy Coding!
