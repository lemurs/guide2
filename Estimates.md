### Decomposition

1. Go through the mockups and describe[1] every piece of functionality in terms of user stories[2]
  * What do the buttons and other controls do?
  * What segues are there and where do they go?
  * What has a color, font, or other customization?
  * Where do the images or text come from?
2. Assign each user story a [difficulty](./Difficulty.md) estimate.
  * Split or combine into individual issues as you go.
3. Assign each issue a [priority](./Priority.md) level.
4. Calculate time estimates by adding difficulties and multiplying the sum by the accuracy coefficient[3]
  * p x Pp x d x Td * cA (priority x probability x difficulty x time x accuracy)
5. Adjust priorities accordingly.


### Calculations

What does it look like if we weigh the priority levels by probability?

Random sample set:

| P | D1 | D2 | D3 | D4 | D5 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | 4 | 4 | 2 | 1 | 0 |
| 2 | 6 | 3 | 4 | 0 | 0 |
| 3 | 3 | 2 | 4 | 0 | 0 |
| 4 | 0 | 0 | 0 | 0 | 0 |
| 5 | 0 | 0 | 0 | 0 | 0 |

| P | .2 | .5 | 1. | 3. | D5 | Sums
| :-: | :-: | :-: | :-: | :-: | :-: | ---
| 1 | .8 |  2 |  2 |  3 |  0 | 6.8 Days * 1.00 = 6.1 Days
| 2 | 1.2 |  1.5 |  4 |  0 |  0 | 6.7 Days * 0.75 = 5.0 Days
| 3 | .6 |  1 |  4 |  0 |  0 | 5.6 Days * 0.50 = 2.8 Days
| 4 |  0 |  0 |  0 |  0 |  0 | 0 * 0.25 = 0
| 5 |  0 |  0 |  0 |  0 |  0 | 

That's a total of 13.9 rounded up to 14 days * the accuracy coefficient of 2 to give 28 days, which is about a month and a half.

Another way would be to sum P1 and P2 and ignore P3 and below. That, coincident to this example, also yields 28 days.

It's probably not true that all the P2s and P3s will be cleared, though, or they wouldn't be in another priority category. It would be more accurate to say that the estimate is between 4-6 weeks, depending on how the P2s and P3s shake out.

### Team Dynamics

Multiple people can distribute work, but not evenly. It would be a similar drop off to the probability of priority levels being implemented.

20 Days (1 Month) for a team of:

Effectiveness - Divisor - Time

1. 100% - 1.00 - 20 Days (1 Month)
2. 75% - 1.75 - 12 Days
3. 50% - 2.25 - 9 Days (2 Weeks)
4. 25% - 2.50 - 8 Days
5. 10% - 2.60 - 8 Days


### Using Metrics

Estimates need no longer be static goals that are either hit or missed, but living metrics that give continuous insight into the ongoing status of a project and performance of its team, not just in hitting estimates, but in making estimates in the first place.

For example, it's one thing to divide the total amount of work by the number of people (times some efficiency coefficient) but once issues are actually assigned, you can instead treat work queues like parallel processes, calculating per worker estimates. Three one-day tasks divided by 3 people will take longer than 1 day if all the tasks are in the same person's queue. 

Feeding data such as how many issues of a given difficulty are actually closed in a given day, and how long it actually took to close them lets you not only see how closely performance matches estimates, but how many issues were reclassfied at a higher difficulty, and how long into working on the problem did it become apparent to revise the estimate.

What's important are not the minutes it takes to flip the switch on an implementation, but the time it takes upon dedicating oneself to solving that problem to closing its issue. If a five minute implementation took 3 days of walking around in frustrated circles to achieve, it's a 3 day problem.


### Notes

1. __Issue Trackers__ are numerous. Pick a good one. I recommend GitHub.
2. __User Stories__ are brief descriptions of an interaction one can have with the product.
  * I need to log in.
  * I want to set my profile picture.
  * I want to read my messages.
  * I want to write a message.
  * I want to edit my message.
  * I want to save my changes.
3. __Accuracy Coefficients__ start with 2 or 3 and adjust as you measure your ability to make accurate estimates.
