# Cheap GPS

![alt text](https://imgs.xkcd.com/comics/cheap_gps.png)

Inspired by [XKCD #407](https://xkcd.com/407/). This project is not associated with XKCD in any way.

This project is a progessive webapplication. It is a non-traditional navigation application that instead of giving directions turn by turn or even using compas barings it simply uses a scale of:

"freezing" ← "cold" → "warm" → "hot!" → "on fire!"

And when moving:

"colder" ←→ "warmer" → "hotter!"

Thus it is slightly more useful than in the comic in that you get more immediate feedback when changing direction. The suffixed adjectives can appear regardless of how warm you are. For instance, if you are "hot!" but turn around and start going the wrong way, it will display "colder" even though in absolute terms you are still warm.

## Algorithms

The application uses absolute distance from the destination to deturmine warm or cold. You are considered moving if you're GPS location is significant different than the last sample. 

The application does not consider the direction of roads. For example, a road might be pointing right at your destination but end before reaching it. Going down that road would still be "warmer" (until you have to turn around and head back). Another example would be when traveling on a road the will eventually get you to your destination but will temporarily take you further away. For a short period of time you will be getting "colder" even though in a traditional navigation app you would be getting closer to your destination.

Thus in some cases to get to your destination you may need to get cold before you get warm.
