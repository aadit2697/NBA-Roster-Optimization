# Rubric for Project Proposal

Your project proposal will follow the format of a standard research proposal, and will be written in markdown format.  It will be saved in the same directory as this rubric, and simply named "proposal.md."  It should not be longer than 2-3 pages max, and may be shorter.  It will have the following sections.

### Title

  NBA Team Rooster Optimization

### Team

Point of Contact: aadit2697
Member1: aadit2697 
Member2: revanthshahukaru
Member3: mnmcfadd
Member4: VrushaliLad799
Member5: Kapil1917T

### Introduction

Our NBA project revolves around using historical game data to develop two predictive models with practical applications for teams and players -
Model 1 aims to predict whether a team will win or lose a game based on various player-level features, including player performance statistics and game outcomes.
Model 2 aims to predict whether a player will be benched or play in a game, leveraging the predictions from Model 1 along with other relevant player features.
 
Basis our research, we have identified an approach wherein we combine player-level statistics, team-level statistics, gameovergame data, leaguedashboard data to provide valuable insights into player usage and team success. By incorporating predicted game outcomes from the first model into the second model, we hope to capture how player performance impacts team decisions in real-time.
 
The significance of our work lies in its potential to assist coaches, team managers, and analysts in making informed decisions. By accurately forecasting game results and player benching, our models can guide lineup choices, player rotations, and in-game strategies. Ultimately, our project aims to empower NBA teams with actionable insights that enhance performance and decision-making.

Limitation to our current process is encountering cases when there are new players into question.

### Literature Review

In today's NBA landscape, understanding player performance and game outcomes is crucial for teams, coaches, and analysts seeking a competitive edge1. Traditionally, basketball analytics has relied on basic statistics like points scored, rebounds, and shooting percentages to evaluate player contributions and team effectiveness2. While these methods offer valuable insights, they often fall short in capturing the complexities of the game.
 
While existing research has explored various facets of NBA analytics, such as player efficiency metrics and lineup optimization4, there exists a notable gap in integrating predictive models to forecast both game outcomes and player usage decisions simultaneously. Our proposed approach aims to bridge this gap by providing a comprehensive framework for decision support in NBA teams.
 
Stakeholder Needs:
 
**NBA Coaches**: Coaches require actionable insights into game outcomes and player availability to make informed decisions regarding lineup selections and in-game strategies.
 
**Team Managers**: Effective roster management and resource allocation are essential for team managers as they rely on detailed analyses of player performance and usage patterns to optimize team compositions and maximize success.
 
**Player Agents**: Player agents play a crucial role in representing athletes' interests as they seek comprehensive insights into factors influencing player playing time and performance to negotiate favorable contracts and endorsements.
 
**Sports Analysts**: Analysts aim to provide engaging and informative coverage of NBA games for broadcasters, media outlets, and fans alike as they rely on advanced analytics and predictive modeling to deliver accurate and insightful commentary on player and team performance.
 
By addressing the specific needs of these stakeholders through advanced analytics and predictive modeling, our approach aims to enhance decision-making processes and drive success in the NBA arena.
 
Citations referred -
1. Hollinger, J. (2004). Pro Basketball Forecast. Potomac Books, Inc. ↩
 
2. Oliver, D. (2004). Basketball on Paper: Rules and Tools for Performance Analysis. Potomac Books, Inc. ↩
 
3. Lewis, M. (2004). Moneyball: The Art of Winning an Unfair Game. W. W. Norton & Company. ↩
 
4. Engelmann, J. B., & Wolpert, D. M. (2014). "Resource Allocation as an Optimal Decision Problem." Frontiers in Human Neuroscience, 8, 792

### Data and Methods

Our study focuses on analyzing NBA game data to uncover insights that could aid teams in making better decisions on player usage and predicting game outcomes accurately.

#### Data

https://github.com/swar/nba_api/tree/master/src/nba_api/stats/endpoints 

Before proceeding with modeling, we ensured our data was clean and consistent. This involvs addressing errors, handling missing values, and organizing categorical data appropriately. We also standardized numerical values to maintain consistency.

Feature Engineering:
To enhance our models, we engineered some new features based on basketball knowledge and prior research. These features include player name, ID, team name, team ID, and player bench status. We also incorporated key performance indicators such as three-pointers made and points scored if not benched.

Our modeling strategy is divided into two parts:
 
Game Outcome Prediction (Model 1):
 
Target Variable: Win or loss
Features: Player and team stats, game context (which includes features like Player name, id, team_name, team_id, benched/not,three_pointers, points_scored_if_not_benched)
Model: Using machine learning algorithms like logistic regression or decision trees, we predict game outcomes based on historical data. This model aids in forecasting whether a team will win or lose.
Player Usage Prediction (Model 2):
 
Target Variable: Player bench status
Features: Player and team stats, game outcomes (predicted by Model 1) and other relevant features which were utiilized while building the first model
Model: Utilizing the game outcomes predicted by Model 1, we train another model to predict whether a player will be benched or participate in the game. This helps teams make informed decisions regarding player selection.

Limitations and Considerations:
While we're optimistic about our models' potential, following might be their limitations. Biases in the data and the inherent uncertainty of sports can impact their accuracy. Nevertheless, by continuously refining our approach and remaining receptive to feedback, we aim to provide valuable insights to NBA teams, enabling them to make better-informed decisions on and off the court.

#### Methods

In our methods section, we'll outline our approach to building and evaluating our models. We'll start by explaining the transformations and preprocessing steps we'll apply to our data to get it ready for modeling. This might include things like cleaning up missing values, encoding categorical variables, and scaling numerical features.
For our modeling techniques, we'll use a combination of algorithms such as decision trees, logistic regression, and random forests.
To evaluate our models, we'll use metrics like accuracy, precision, recall, and F1-score. These metrics will help us assess how well our models are performing and whether they're meeting the needs of our stakeholders. We'll also consider factors like interpretability and computational efficiency when evaluating our models.
Overall, our goal is to develop models that are accurate, reliable, and useful for predicting game outcomes and player performance in the NBA.

### Project Plan

| Period       | Activity                                                     | Milestone                                                                                       |
|--------------|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| 3/1 - 3/7    | Collect and clean NBA game data                              | Gather NBA game data and perform basic cleaning tasks.                                           |
| 3/8 - 3/14   | Explore NBA game data                                        | Dive into the data to find interesting insights and potential features for our models.           |
| 3/15 - 3/21  | Create useful features for models                            | Develop features that will help our models make accurate predictions.                            |
| 3/22 - 3/28  | Build Model 1                                                | Train and test the first model using the prepared data.                                          |
| 3/29 - 4/4   | Develop Model 2 based on Model 1 outputs                     | Use the results from Model 1 to build and evaluate the second model.                              |
| 4/5 - 4/11   | Evaluate and improve model performance                       | Check how well our models are doing and make adjustments if needed.                               |
| 4/12 - 4/18  | Share progress with stakeholders                             | Show our findings to stakeholders and gather their feedback.                                       |
| 4/19 - 4/25  | Write up project details and finalize report                 | Put together all our work into a detailed report.                                                 |
| 4/26 - 4/30  | Review and revise as necessary                               | Go over everything one last time and make any final tweaks.                                        |
| 4/30 - 4/30    | Submit final report and deliverables                         | Send in our report and other materials.                        |

### Risks

Data Quality and Availability:
Risk: The NBA game data we rely on may have quality issues or be incomplete.
Mitigation: We'll carefully check our data sources and fix any errors or missing information. If needed, we'll look for other data sources to fill in any gaps.

Model Performance:
Risk: Our predictive models might not perform as well as we hope, making our predictions unreliable.
Mitigation: We'll keep an eye on how well our models are doing and tweak them based on what we learn. We'll also try different modeling approaches and add more features if necessary.

Stakeholder Adoption:
Risk: NBA teams and other decision-makers may not be interested in using our insights and suggestions.
Mitigation: We'll talk to stakeholders early on to hear their thoughts and address any worries they have. Showing them real-life examples of how our models can help might convince them to give it a try.

Regulatory and Ethical Considerations:
Risk: We might run into problems with rules and ethics around using data, like privacy concerns or making sure our models are fair.
Mitigation: We'll make sure we follow all the rules and guidelines about using data. We'll also be open about how our models work and be ready to explain our decisions.

New Player:
Risk: If we have no past data for new players.
Mitigation: Skip predictions for such players who are rookies.

Contingency Plan:
What if things don't go as planned? If our models keep failing or nobody wants to use them, we'll rethink our approach.
Mitigation: We'll take a good look at what we've done and figure out what needs fixing. We'll keep testing and trying new ideas until we find something that works better. And we'll keep talking to people to understand what they need and want.



# Grading

- Does your proposal include all of the above mentioned sections? [10 points]
- Have you clearly identifed your stakeholders and their needs [10 points]
- Have you answered the 5 Heilmeier questions mentioned effectively [20 points]
- Is you proposal plan feasible, and do you have sufficient detail to give me confidence that you will succeed? [10 points] 

[^1]: Like this
