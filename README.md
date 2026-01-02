The code utilizes manually inputted data on the location of soccer penalties taken to calculate the probability of scoring in a certain area with logistic regression. It includes graphs, with or without heatmaps, to better understand the distribution of goals, saves, and misses. A total of 100 shots, 50 for each trial, were utilized.

The following information is a more in-depth explanation of the code:

The data is manually inputted with four portions: shot number, outcome, strength, and x-y coordinates.

The shot number only takes into account which penalty is being taken to track the data for the legend.

The outcome consists of either a goal, miss, or save. The goal only counts if the ball crossed the whole line. A miss counts if it does not cross the line without goalkeeper interference. A save counts if any goalkeeper interference/contact was made.

The strength is dependent on the penalty-taker's interpretation of the shot. It is divided into three: low strength, medium (mid) strength, and high strength. Height has no impact on the strength, however, the results may display correlation.

The x-y coordinates are manually inputted and may be done with video footages for better inputs. Any data on or beyond -4 or +4 on the x-axis must be counted as a miss or save. Any data on or beyond +2.67 on the y-axis must be counted as a miss or save. Any data below 0 yards on the y-axis are not valid data points.

All inputs must align with each result for the code to run smoothly. Any mis-inputs or errors may lead to syntax errors or wrong results.

The graphs were created utilizing seaborn to train the model and provide the user with visuals that could be used for a better analysis of results.

The black outline represents a soccer goal, measuring 8 yards across and 2.67 tall. The center of the x-axis is 0 yards spanning from -4 to +4. The y-axis begins at 0 yards and reaches 2.67 yards.

The logistic regression model comes with an interactive portion to calculate the probability of scoring in any location utilizing x-y coordinates. Any data on or beyond -4 or +4 on the x-axis will output 0 probability as it is beyond the goal limits. Any data on or beyond +2.67 on the y-axis will output 0 probability as it is beyond the goal limits. Any data below 0 yards on the y-axis are not valid data points.

The current probabilty displayed at the end of the code is the probability of scoring at (0,0).

Credits: Emmanuel-Angelo Ojadi and Eduardo Medina Tapia

Template: Jupyterlab Notebooks by Github
