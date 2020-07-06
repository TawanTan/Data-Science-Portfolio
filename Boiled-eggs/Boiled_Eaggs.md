# Funny Boiled Eggs 

&emsp;This project was a part of the Design of Engineer Experiment course while I was studying at university. To study and understandingthe experiment with 2<sup>k</sup> factorial designs.  
&emsp;In my province Buddha Sothorn buddha statue is very famous. People believe that they must worship him with many many boiled eggs like thousand. So we need many eggs with inside are cooked and all solid. But we still want to save the production cost as much as possible. Therefore, we designed this experiment by using The 2<sup>k</sup> factorial design to find the factors and treatment for boiling the eggs with inside are cooked and all solid.  
![Sothron](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/SothornEggs.jpeg)

## Experiment design

### Factors
- Temperature
- Time
- Water level
### Response
- Level of boiled eggs By following the levels as shown below
![EggsLeavels](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/EggsLevels.jpg)

### Treatment combination
Boils eggs by following contrast coefficients 2<sup>3</sup> table below  

|Run	|	A	|	B	|	C   |
|:-----:|:-----:|:-----:|:-----:|
|  1	|	-	|	+	|	-   |
|  2  	|	+  	|	+  	|	-   |
|  3  	|	-  	|	-  	|	-   |
|  4  	|	+  	|	-  	|	-   |
|  5  	|	-  	|	+  	|	+   |
|  6	| 	+  	|	+  	|	+   |
|  7  	|	-	|	-  	|	+   |
|  8  	|	+	|  	-  	|	+   |  

- Note  
    - A is the temperature with high (+) and low (-) levels of 80 degrees Celsius and 95 degrees Celsius  
    - B is the time with high level (+) and low (-) of 9 minutes and 12 minutes
    - C is the water level with high (+) and low (-) of 0.4 liters and 0.8 liters

## Data analysis

### 2<sup>k</sup> factorial 

|Run	|	 Temperatur	|	Time	|	Water level   |  Response|
|:-----:|:-----:|:-----:|:-----:|:-----:|
|  1	|	80	|	9	|	0.4   |   3   |
|  2  	|	95  |	9  	|	0.4   |   6   |
|  3  	|	80  |	12  |	0.4   |   4   |
|  4  	|	95  |	12 	|	0.4   |   7   |
|  5  	|	80 	|	9 	|	0.8   |   4   |
|  6	| 	95  |	9  	|	0.8   |   6   |
|  7  	|	80	|	12  |	0.8   |   5   |
|  8  	|	95	|  	12 	|	0.8   |   8   |
 
 ![cubeplot](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/2kCube.png)
 
 - If the analysis results from the 2<sup>k</sup> factorial method shows two or more factors, use the experimental point(treatment) increase in 2<sup>k</sup> factorial.
 - If there is only 1, use the One-Way ANOVA design.

![EffectGraph](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/EffectGraph.png "title-1") ![EffectChart](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/EffectChart.png "title-1")

&emsp; The normal plot of the estimator of all influences and Pareto Chart shows that ```A (temperature)``` has a significant impact on the ripeness level of boiled eggs.

|Source of variation|Sum of squares|Degree of freedom|Mean squares|F-value|P-value|
|:------------------|:------------:|:---------------:|:----------:|:-----:|:-----:|
|Main Effects       |     15.1250  |        1        |   15.1250  | 19.11 | 0.005 |
|Temp               |     15.1250  |        1        |   15.1250  | 19.11 | 0.005 |
|Residual Error     |     4.7500   |        6        |   0.7917   |
|Pure Error         |     4.7500   |        6        |   0.7917   |
|Total              |     19.8750  |        7        |

&emsp; Factor A has a significant effect on the level ripeness of boiled eggs (P-value <0.05), which confirms the analysis results obtained from The normal plot of the estimator of all influences. Therefore use The ```One-Way ANOVA``` design.

#### Model Adequacy Checking

![NormPlot](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/Normal_plot.png "title-1") ![TimeSeq](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/TimeSeq.png "title-2") ![V](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/ConVariance.png "title-3")

&emsp; Shows that the data obtained from the results are suitable to the statistical model of the 2<sup>3</sup> factorial

---

### One-Way ANOVA
&emsp; The only significant factor effecting the boiled eggs is temperature. Therefore, additional experiments were carried by designing a single factor experiment.

|temperature|1    |  2  |   3   |  mean |
|:---------:|:---:|:---:|:-----:|:-----:|
|92         |  8  |  7  |	 8  |	7.67|
|89         |  7  |  6  |	 7  |	6.67|
|86	        |  6  |  6  |	 7  |	6.33|
|83	        |  5  |  5  |	 6  |	5.33|
*Three replicate

#### Hypothesis testing
&emsp;&emsp;&emsp;&emsp;H0 : μ1 = μ2 = μ3  
&emsp;&emsp;&emsp;&emsp;H1 : μi ≠ μj,for at least one pair (i,j)  
&emsp;&emsp;&emsp;&emsp;By μ1, μ2, μ3 are mean ripeness level of boiled eggs at 92, 89, 86, 83  

#### Model Adequacy Checking

![NormPlot2](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/Normal_plot2.png "title-1") ![TimeSeq2](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/TimeSeq2.png "title-2") ![V2](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/ConVariance2.png "title-3")

- From the first one you can see that the graph has a tende in linear, showing that the data obtained from the experiment has normal distribution.  
- From the second one, you can see that there are no pattern signs indicating the abnormalities of data.  
- From the third one, you can see that there are no pattern in megaphone indicating the abnormalities.

|Source of variation|Sum of squares|Degree of freedom|Mean squares|F-value|P-value|
|:------------------|:------------:|:---------------:|:----------:|:-----:|:-----:|
|Temperature        |     8.500    |        4        |   2.125    | 5.95  | 0.021 |
|Error              |     2.500    |        7        |    0.357   |
|Total              |     11.000   |        11       |

&emsp;&emsp;```F-value = 5.95 > f 0.05,4,7 = 4.12```  
&emsp;&emsp;```Reject H0``` and conclude that temperature affects the ripeness of the eggs  
- Note  
The conclusion can only shows that different temperatures affect the ripeness of the eggs on average significantly. But can't tell how the different temperatures affect the ripeness of the eggs

---

### Multiple Comparisons

#### The least significant difference method (LSD) or Fisher
Grouping Information Using Fisher Method  
 
|temp|  N  |  Mean  |Grouping|
|:--:|:---:|:------:|:------:|
|92  |  3  |7.6667  |A       |
|89  |  3  |6.6667  |A B     |
|86  |  3  |6.3333  |  B C   |
|83  |  3  |5.3333  |    C   |

The LSD method shows that There weren't  significant differences in temperature between 89 ° c and 86 ° c.
 
#### The Tukey's test
Grouping Information Using Tukey Method

|temp|  N  |  Mean  |Grouping|
|:--:|:---:|:------:|:------:|
|92  |  3  |7.6667  |A       |
|89  |  3  |6.6667  |A B     |
|86  |  3  |6.3333  |A B     |
|83  |  3  |5.3333  |  B     |

The Tukey's test shows that There weren't  significant differences in temperature between 89 ° c and 86 ° c.

## Conclusion
&emsp;There is only one factor, that is the temperature that has a significant effect. Therefore temperature is used as a single factor experiment by determine the time of boiling for 12 minutes and the water level of 0.8 liters because it is the level of the factor that causes the most cooked eggs. The results from a single factor experiment found that at 92 ° C the average ripeness level of boiled eggs was as close as 95 ° C. Therefore, the temperature was chosen to be 92 ° C because of the economic factors and eggs still having the highest level of ripeness



