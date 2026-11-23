---
name: "College Scorecard: Is College Worth It?"
tools: [Python, HTML, vega-lite,Altair]
image: assets/pngs/caps.jpeg
description: "Data Visualization Project that explores the college scorecard data, trying to help students understand if college is worth it for them!"
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Tuition, Paychecks, and Student Loans: Is a Four Year Degree worth it

by Colton Murphy, Group 32


Picking a College is one of the biggest money investments people make, and the price tags are all over the place. Some cost under $15,000 a year once you add up tuition, housing, books and everything else. On the other hand some cost clost to $100,000. So its fair to ask if the investment is worth it? I dug into data from the U.S. Department of Education's College Scorecard, whicch tracks cost and student outcomes for nearly every college in the country, to find out. I focuesd on 1,682 schools that mainly give out bachelors degrees and that report both their cost and how much their students go on to earn.

## The Big Picture: does a degree really pay off at all?

![alt text](<../assets/pngs/Earngs Chart by Education Level.png>)

Source: U.S Bureau of Labor Statistics Earnings and unemployment rates by education attainment, 2025[Chart]. Retrieved November 23, 2026 from 'https://www.bls.gov/emp/graphics/unemployment-rates-and-earnings.htm'

Before comparing colleges to each other it helps to know whether a bachelors degree is worth it in general. This chart from the U.S. Bureau of Labor Stastics says yes on average. In 2025, a typical full time worker earned $1,578 a week compared to $966 for someone with a high school diploma. Thats about 60% more or roughly $37,024 per year which is a massive gap. Degree holders were also less likely to be out of work with a 2.8% unemployment compared to 4.3% for high school graduates. So a degree pays off on average. The real question is how much you should pay for one.

## Explore it Yourself: Cost vs Earnings

<vegachart schema-url="{{ site.baseurl }}/assets/json/Earn_OT_Dash.json" style="width: 100%"></vegachart>

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/Earn_OT_Dash.json" style="width: 100%"></vegachart>
```
This chart compares the cost of attendance vs the median earnings of a student 10 years after starting college. Each dot is a different collge. Dots farther right cost more per year, and dots higher up are colleges is the median earnings that student a student makes 10 years after starting. The colors show what kind of school it is, blue for public, orange for private nonprofit and green for private for profit. 

How to use it: Hover over any dot to see the schools name, location, cost, earings, graduation rate and typical student loan debt. Click and drag a box over a group of dots and the bottom chart updates to show how earnings grow for the schools you picked 6,8,and 10 years after starting college. You can double click to clear your box. You can also use the pick a state dropdown to highlight one states shools like (IL for Illinois). The bottom chart then only shows that state.

What I see is that theres a lot of spread at every price. More expensive schools do tend to have higher earnings, especially the very expensive ones in the top right. But plent of $20,000 per year public schools match or beat private schools that cost two to three times as much. 

## Same Earnings, Half the Price
<vegachart schema-url="{{ site.baseurl }}/assets/json/type_chart.json" style="width: 100%"></vegachart>

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/type_chart.json" style="width: 100%"></vegachart>
```
This chart brings the scatter plot down to one comparison. For each type of school, the gray bar is the typical(median) yearly cost and the blue bar is the typical earnings 10 years later. Public schools cost about 25,600 a year and private nonprofits cost about 52,200, roughly twice as much, but their former students end up earing almost the exact same, around 59,000. For profit schools land in the middle on price but are at the bottom on earnings. 

## The cost after graduation: student loans
<vegachart schema-url="{{ site.baseurl }}/assets/json/debt_dash.json" style="width: 100%"></vegachart>

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/debt_dash.json" style="width: 100%"></vegachart
```

The price of college doesnt end at graduation. Most students borrow, and the loan payments follow them for years. The top chart shows each schools typical(median) student laon debt at graduation against its typical earnings 10 years after starting. Drag a box over any group of dots, and the bottom chart shows what chare of a typical monthly paycheck goes to the monthly loan payment(Debt numbers are missing for 67 schools, so they dont appear here.)

Two things standout. First borrowing more doest mean earning more. The dots dont tred upward from left to right, so schools where students take on bigger loans dont sem to produce higher earners. Second , for profit students get hit twice. Their typical debt is the highest and they also earn the least. Across all schools a typical for profit grduates loan payment takes about 9% of their montly paycheck, about double what public school graduates pay and well above the 5.3% that private non profits pay.

## What This Means
The takeaway is that a higher price tag doesnt guarantee a bigger paycheck, and bigger loans dont either. For a lot of students, a public school can deliver the same typical earnings for about half the cost, with smaller loan payments taking less of each after graduation paychek. That said, earning numbers only include students who got federal financial aid, like pell grands or federal loans. They also include students who started at a school but didnt finish which may pull down earnings. So, use this as a starting point when comparing school outcomes not the final word.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

<div class="left">
{% include elements/button.html link="https://github.com/coltonmurph/coltonmurph.github.io/blob/main/data/Most-Recent-Cohorts-Institution.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/coltonmurph/coltonmurph.github.io/blob/main/python_notebooks/Scorecard.ipynb" text="The Analysis" %}
</div>

