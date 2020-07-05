# Funny Boiled Eggs 
---
This project was a part of the Design of Engineer Experiment course while I was studying at university. To study the experiment with 2<sup>k</sup> factorial designs.  

---
## The idea is...
Boiled eggs are easy to make. But not easy to make delicious We therefore designed this experiment by using The 2<sup>k</sup> Factorial Design.  

### Factors
- Temperature
- Time
- Water level
### Response
- Levels of boiled eggs By following the levels as shown below
![EggsLeavels](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/EggsLevels.jpg)

### Experiment design
- Boils eggs by following contrast coefficients 2<sup>3</sup> table below  
<center>

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

</center>

- Note  
    - A is the temperature with high (+) and low (-) levels of 80 degrees Celsius and 95 degrees Celsius  
    - B is the time with high level (+) and low (-) of 9 minutes and 12 minutes
    - C is the water level with high (+) and low (-) of 0.4 liters and 0.8 liters

### Data analysis
 
Result table
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
 
 
 
 
 Analyze result by using Minitab program 
 - If the analysis results from the 2<sup>k</sup> factorial method shows two or more factors, use the experimental point(treatment) increase in 2<sup>k</sup> factorial.
 - If there is only 1, use the One-Way ANOVA design.




















Model Adequacy Checking

![NormPlot](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/Normal_plot.png "title-1") ![](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/TimeSeq.png "title-2") ![](https://raw.githubusercontent.com/TawanTan/Data-Science-Portfolio/master/Boiled-eggs/ConVariance.png "title-3")





