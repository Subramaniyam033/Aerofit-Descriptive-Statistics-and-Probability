### Problem Statement:
Leveraging the customer data collected by Aerofit consisting of the Gender, Age, Income, Weekly Usage, Fitness, Marital Status and Miles run on treadmill to 
identify characteristics which make the customer buy a particular treadmill out of KP281, KP481 and KP781 in the increasing order of expenditures. 
Further providing recommendations of treadmill for future orders/customers based on their profile.

### EDA Insights: 
* The dataset had 180 rows
* There is no Null values or duplicates in the dataset.
* Age and income / Miles and Income are positively correlated
* Miles, Income, Usage and Fitness are highly correlated
* Gender is also correlated with Usage, fitness,Income and Miles.
* The more advanced the product is, the more its usage and hence more the miles run which in turns improves the fitness.
* Outliers were found in Income, Miles and Age but the dataset has only 180 rows hence we didnt remove the outliers.
* Maritial status has No effect
* Around 55% of women prefer KP281 and only 10% prefer KP781. While around 35% of men prefer KP781.
* 95% of customers having fitness level of 5 use KP781 and none of those having fitness level below 3 use KP781.

**Customer Profiles for KP781**
* Only people having incomes greater than 70k have run over 220 miles and all of then use KP781.
* Recommend KP781 if one or more conditions are satisfied along with a necessary condition of Income > 70000:-
    a) Education Level >= 18
    b) Usage days > = 5
    c) Fitness Levels = 5
    d) The person runs more than 150 miles(80% of them use KP781)

* Never Recommend KP781 if one or more of these conditions are satisfied:-
    a) Education Levels < 14
    b) Fitness < 3
    c) Age < 20
    d)Income < 45000
    e) Miles run < 50

**Why very few women have bought the luxurious KP781 treadmill?**
Only 2 women have incomes over 70k which is certainly the reason for a large proportion of them not buying KP781(affordability).

**Note for below mentioned points**
KP281 and KP481 don't have much differences in their costs and the characteristics of customers who use them . Still a few of them have been identified but they need to be validated with an incremental data.

**Customer Profiles for KP281:**
* Women having incomes below 70k and age > 40
* Customers having income in range 60k-70k and usage days=3
* Customers having income in range 45k-50k and usage days=2
* Customers having income in range 35k-45k and usage days=4
* Customers having income in range 50k-60k and usage days=4
* Customers with Fitness=4, age closer to 40 and income 50k-60k
* Customers with Education Level=16, Age>32 and income 45k-50k
* Customers with Education Level=16, Age>45 and income 60k-70k
* Customers with Age in 25-30 and 35-40 having incomes in range 35k-45k
* Customers with 40+ Age and 60k-70k income
* Women with incomes < 35k and whose miles run < 105
* Customers with usages=5, incomes in range 35k-45k and who run more than 140 miles
* Customers with Fitness=5, incomes < 70k and Incomes in 45k-50k
* Customers with Education level=15 having incomes less than 35k
* Customers with Usages=3, miles run < 70 and Age>40
* Customers with Usages=2 and Age between 25-30

**Customer Profiles for KP481:**

* Women having incomes below 70k and age between 32-37
* Customers with age < 25, incomes in range 50-60k and the miles run is in the range 100-150
* Customers with Fitness=4, age in range 25-32 and income 50k-60k
* Customers with Education Level=16, Age< 22 and income 45k-50k
* Customers with Education Level=16, Age< 35 and income 60k-70k
* Customers with 35-40 Age and 60k-70k income
* Women with incomes < 35k and whose miles run >105
* Men with incomes 60k-70k and who tread in range 100-150 miles
* Customers with Fitness=4, incomes < 45k-50k and who run more than 100 miles
* Customers with Education level=13 having incomes in ranges 45-60k
* Customers with Usages=2 and Age>40
