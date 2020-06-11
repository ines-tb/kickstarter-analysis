# An Analysis of Kickstarter Campaigns.
Performing Analysis on Kickstarter data to uncover trends.

### Analysis goal
The goal of this study is to analyze the viability of **crowdfunding a theater** project, particularly a **play**, in the United States with an estimated budget of over **\$10,000**.

##### Data Source
The dataset used contains over 4000 projects from 2009 to 2017, from which 3038 were original from the U.S. This makes our data trustworthy for the purpose of our analysis.

---
### Findings
First thing we need to find out is how popular the category of our interest is among the funded projects, given that a larger sample will provide more robust results.

* In the below chart (_picture 1_) we can check that **theater is the most demanded category**, a fact also holds in the U.S.
  ![ParentCategoryOutcomes](./media/1.ParentCategoryOutcomes.png?raw=true)

  _Picture 1_

  ![ParentCategoryOutcomesUS](./media/2.ParentCategoryOutcomesUS.png?raw=true)

  _Picture 2_

  
Another definitive point to be considered is the outcome of the financings depending on the period they were launched.   
* It can easily be checked (_picture 3_) that, independently of the category, the months of **May and June** are significantly more successful, being December the worst time to start any plan. In the case of theater (_picture 4_), this behavior is even more drastic and the spike in May more pronounced, gradually reducing until the end of the year.
  ![OutcomesBasedOnLaunchDate](./media/3.OutcomesBasedOnLaunchDate.png?raw=true)

  _Picture 3_

  ![OutcomesBasedOnLaunchDateTheater](./media/4.OutcomesBasedOnLaunchDateTheater.png?raw=true)

  _Picture 4_

Statistically, we have also extracted some particularly useful information (_picture 5_) to help us group the U.S. theatrical shows in order to limit the risk and take decisions with solid foundations.
* The measures of Central Tendency have provided some decisive insights. The average goal of a successful project is **\$5,000** and the median goal **\$3,000**, figures remarkably close to the corresponding average and median pledge. On the other hand, in the case of failed plays, the situation is utterly different, given that not only the average and median goal are around double, **\$10,000** and **\$5,000** respectively, but also the pledge amounts descend significantly in comparison to little over \$500 for average pledge and \$100 for the median.
* In the case of Spread Measures, although half of the failed shows had a goal between \$2,000 and \$10,000, the extremely high standard deviation for them of $21,968 indicates that there exist some outlier point(s) in the sample.  
Also, the fact that **75% of the successful plays** got a pledge below **\$5,700** implies that high budget projects are unlikely to meet their goals. However, that is not the only reason for breakdown. As the maximum amount collected by 75% of failed plays was \$501, there were other reasons, cost unrelated, for them to founder.
![DescriptiveAnalysisPlaysUS](./media/5.DescriptiveAnalysisPlaysUS.png?raw=true)
  
  _Picture 5_
---
### Recommendations

Given the information in the previous section, although a 60% of the theater proposals were successfully financed, there are several key points that could determine the outcome of the campaign.
* The first thing is the time of the year. We have seen how important is the moment where the collection is started, so it should be planned to be started in **May or June**, preferably the former, as it is the month when the graph hits its maximum among the theater collective. 
* Secondly, it would be highly recommended to **reconsider the requested amount**. The estimated budget is twice the average pledged amount for plays in U.S. Having in mind that three quarters of the successfully funded have a pledge below \$5700, the amount \$10,000 should be decreased to have better chances of dodging failure.
* Moreover, due to fact that the majority of failed projects had very low pledges, it follows that there must be other reasons apart from the costly projects that prevents them from success. A further non-numerical analysis is recommended to help finding subtle similitudes among them that could have led to failure and avoid them in current plan.

---
### Challenge
After the previously studied project came close to its goal in a short period of time, an extra analysis is required to determine whether the length of a campaign may contribute to its ultimate success or failure.

The same dataset will be used to extract this new information. Live projects will be ignored in this analysis.

##### Conclusions
* In the first chart (_"Outcomes Based on Goals"_) it is seen that the goal is a conclusive element, the higher the goal, the lower the chances to reach it except for amounts from **\$35,000 to \$45,000** that are comparable in success to the plays with a budget lower than $5,000. Apart from the mentioned interval, \$20,000 is the point from which the percentage of failure starts to be higher than success.
In our case, with a \$10,000 goal, the data states that around **54% of the plays with similar finance needs succeed** in the past. 
  ![Outcomes Based on Goals](./media/Ch1.OutcomesBasedOnGoals.png?raw=true)

* The below picture (_Outcomes Based On Launch Date_) exposes undoubtedly the effect of the release date in the result. Particularly in theater, May is without a doubt the best month to start a fundraising, as the year progresses the likelihood of success highly decreases.
  ![Outcomes Based On Launch Date](./media/Ch1.OutcomesBasedOnLaunchDate.png?raw=true)

* In the same graph, since both cancelations and failed series are both fairly constant, they have not huge impact in the total amount of projects. Then, the percentage is mainly affected by the remaining element, in this case successful projects. I.e. a higher number of projects could lead to a higher success as the total sum follows a similar trend as the success. However, from the data and charts presented it cannot be inferred unless further research due to a lack of other dimensions in the data that can affect the investments, as seasonal, behavioral, or general country wealthiness.   


##### Data Limitations
The data does not provide information about the moment when the backers contributed to the projects. This missing information could be crucial to determine the optimal campaign duration, as it could happen that certain fundraisings reached their goals in their last days and reducing the time would make them fail. Other scenario could be that extending the duration of an already successful project may be an unnecessary waste of time.

##### Additional analysis
* The first remaining thing to do is to calculate the duration of the campaigns, adding a new column the dataset with the days passed since the start of the funding until the end. If this data was displayed in a pivot table that charts the outcome of each Kickstarter project based on the duration and filtered by Category, it could be uncovered which campaign duration are the most successful.
* Additionally, to complete the previous table we would combine both campaign duration and goal amount. For that purpose, another column for 'Goal Group' will be added to set which of the 12 groups used in the _Outcomes Based on Goals_ section, each project belongs to.
Then with a pivot table that charts the outcome of each Kickstarter project based on the duration filtered by Category and Goal Group will give us more information about which duration will suits better for our estimated budget in order to succeed.
