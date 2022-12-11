https://open.substack.com/pub/abinoda/p/developer-productivity-at-google?r=6a0vo&utm_campaign=post&utm_medium=email

Prior studies have looked at developer productivity, however many of these studies have either looked at controlled environments or used field studies, making it difficult for organizations to confidently apply the results. This study builds on existing literature by looking at an ecologically valid context and drawing strong causal conclusions about what affects developer productivity. 

For this study, the researchers used a panel data analysis technique, which has the advantage of enabling stronger causal inference. Panel data uses data collected at multiple points in time from the same individuals, examining how measurements change over time. 

Their analysis suggested that 16 out of the 39 metrics studied have a statistically significant causal relationship with perceived overall productivity, which we can see in Table 3. A few examples from the table: 

-   Perceived productivity is causally related to satisfaction with **code quality**. Perceived productivity is also causally related to satisfaction with technical debt. 
    
-   Engineers who reported **their tools and infrastructure were not innovative** were more likely to report lower productivity. 
    
-   Engineers hindered by **shifting project priorities** were likely to report lower productivity.
    

[![](https://substackcdn.com/image/fetch/w_469,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fd96ef294-ffd5-4fee-bdeb-a0d50788ee0d_767x1600.png)](https://substack.com/redirect/27911acc-36f5-496b-acc8-b3d5c6f16464?j=eyJ1IjoiNmEwdm8ifQ.ZCbAnUp8LcsNA3npSrsIAwicnQYnCxwwtyVeBqeKEaU)

Researchers note that the Effect Size column in the table “should be read as a percent change in the dependent variable is associated with that percent change in the independent variable. For instance, for code quality, a 100% change in project code quality (from “Very dissatisfied“ to “Very satisfied” to quality) is associated with a 10.5% increase in self-reported productivity.”

The data suggests that satisfaction with code quality within projects is the strongest productivity factor among the 39 factors studied. 

The researchers also looked to understand the direction of the causality with this factor: whether code quality causes productivity, vice versa, or both. To test these hypotheses, researchers looked to see whether changes in perceived code quality correlated with changes in logs-based productivity metrics. Their results showed that changes in code quality were correlated with changes in productivity, however there was no evidence showing that changes in productivity correlated with changes in code quality. 

## **Final thoughts**

Engineers and DevEx teams might inherently understand that factors like code quality affect productivity, but don’t have the data to support that notion. This paper provides that evidence. It may be useful for communicating a hypothesis for making an investment in an area like code quality, tools and infrastructure, or the team’s approach to planning.