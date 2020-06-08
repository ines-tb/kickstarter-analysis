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
![picture 1](../media/1.ParentCategoryOutcomes.png?raw=true)
![picture 2](../media/2.ParentCategoryOutcomesUS.png?raw=true)

Another definitive point to be considered is the outcome of the financings depending on the period they were launched.   
* It can easily be checked (_picture 3_) that, independently of the category, the months of **May and June** are significantly more successful, being December the worst time to start any plan. In the case of theater (_picture 4_), this behavior is even more drastic and the spike in May more pronounced, gradually reducing until the end of the year.
![picture 3](../media/3.OutcomesBasedOnLaunchDate.png?raw=true)
![picture 4](../media/4.OutcomesBasedOnLaunchDateTheater.png?raw=true)

Statistically, we have also extracted some particularly useful information (_picture 5_) to help us group the U.S. theatrical shows in order to limit the risk and take decisions with solid foundations.
* The measures of Central Tendency have provided some decisive insights. The average goal of a successful campaign is **\$5,000** and the median goal **\$3,000**, figures remarkably close to the corresponding average and median pledge. On the other hand, in the case of failed plays, the situation is utterly different, given that not only the average and median goal are around double, **\$10,000** and **\$5,000** respectively, but also the pledge amounts descend significantly in comparison to little over \$500 for average pledge and \$100 for the median.
* In the case of Spread Measures, although half of the failed shows had a goal between \$2,000 and \$10,000, the extremely high standard deviation for them of $21,968 indicates that there exist some outlier point(s) in the sample.  
Also, the fact that **75% of the successful plays** got a pledge below **\$5,700** implies that high budget projects are unlikely to meet their goals. However, that is not the only reason for breakdown. As the maximum amount collected by 75% of failed plays was \$501, there were other reasons, cost unrelated, for them to founder.
![picture 5](../media/5.DescriptiveAnalysisPlaysUS.png?raw=true)

---
### Recommendations

Given the information in the previous section, although a 60% of the theater proposals were successfully financed, there are several key points that could determine the outcome of the campaign.
* The first thing is the time of the year. We have seen how important is the moment where the collection is started, so it should be planned to be started in **May or June**, preferably the former, as it is the month when the graph hits its maximum among the theater collective. 
* Secondly, it would be highly recommended to **reconsider the requested amount**. The estimated budget is twice the average pledged amount for plays in U.S. Having in mind that three quarters of the successfully funded have a pledge below \$5700, the amount \$10,000 should be decreased to have better chances of dodging failure.
* Moreover, due to fact that the majority of failed campaigns had very low pledges, it follows that there must be other reasons apart from the costly projects that prevents them from success. A further non-numerical analysis is recommended to help finding subtle similitudes among them that could have led to failure and avoid them in current plan.
