### Decomposition

1. Go through the mockups and describe[1] every piece of functionality in terms of user stories[2]
  * What do the buttons and other controls do?
  * What segues are there and where do they do?
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
| - | -- |--- | -- | -- | -- |
| 1 |  4 |  4 |  2 |  1 |  0 |
| 2 |  6 |  3 |  4 |  0 |  0 |
| 3 |  3 |  2 |  4 |  0 |  0 |
| 4 |  0 |  0 |  0 |  0 |  0 |
| 5 |  0 |  0 |  0 |  0 |  0 |

| P | .2 | .5 | 1. | 3. | D5 |
| - | -- |--- | -- | -- | -- |
| 1 | .8 |  2 |  2 |  3 |  0 | 6.8 Days * 0.75 = 5.1 
| 2 | 1.2 |  1.5 |  4 |  0 |  0 | 6.7 Days * 0.5 = 3.4
| 3 | .6 |  1 |  4 |  0 |  0 | 5.6 Days * 0.25 = 1.4
| 4 |  0 |  0 |  0 |  0 |  0 |
| 5 |  0 |  0 |  0 |  0 |  0 |

10 days * 2 = 20 days = 1 month

Another way would be to sum P1 and P2 and ignore P3 and below. That yields 28 days, which would probably be called a month, but should more accurately be called a month and a half, since there are only 20 work days in a month.

It's probably not true that all the P2s will be cleared, though, or they wouldn't be in another priority category. It would be more accurate to say that the estimate is 14-28 days, depending on how the P2s shake out. That works out to about 20 days, which is about a month.


### Team Dynamics

Multiple people can distribute work, but not evenly. It would be a similar drop off to the probability of priority levels being implemented.

20 Days (1 Month) for a team of:

#  Effectiveness - Divisor - Time

1. 100% - 1.00 - 20 Days (1 Month)
2. 75% - 1.75 - 12 Days
3. 50% - 2.25 - 9 Days (2 Weeks)
4. 25% - 2.50 - 8 Days
5. 10% - 2.60 - 8 Days



### Notes

1. __Issue Trackers__ are numerous. Pick a good one. I recommend GitHub.
2. __User Stories__ are brief descriptions of an interaction one can have with the product.
  * I need to log in.
  * I want to set my profile picture.
  * I want to read my messages.
  * I want to write a message.
  * I want to edit my message.
  * I want to save my changes.
3. Start with 2 or 3 and adjust as you measure your ability to make accurate estimates.
