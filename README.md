<img width="1000" height="400" alt="ChatGPT Image Sep 23, 2026, 02_12_59 PM" src="https://github.com/user-attachments/assets/0e6e9fab-9507-41cd-90c3-d8710ee875b8" />

# LumaTech - E-commerce Analysis
LumaTech is a global e-commerce company that has sold more than 28M dollars of popular electronics since its inception in 2019. With vast amounts of previously underutilized data on sales, product offerings, the loyalty program, and refunds, I am partnering with the head of the Operations team to thoroughly analyze this information and uncover critical insights. This analysis and recommendations will be used to enhance LumaTech's commercial performance across the sales, marketing, and product teams.

An interactive PowerBI dashboard can be found (here).

The SQL queries performed to uncover these insights can be found (here)

## ERD Diagram
LumaTech's database structure as seen below consists of four tables: orders, customers, geo_lookup, and order_status, with a total row count of 108,127 records.
<img width="1875" height="1114" alt="image" src="https://github.com/user-attachments/assets/d6d58ba1-5461-4303-9673-3a877abdeb58" />
Prior to beginning the analysis, a variety of checks were conducted for quality control and familiarization with the datasets. 

# Deep Dive Insights
## Sales Trends
### Overview:

From 2019-2022, over **108K orders generated $28M in sales, with both metrics showing a 28% growth increase** over this four-year period. Particularly noteworthy, **sales surged dramatically by over 6M in 2020** during the onset of the pandemic, as consumer purchasing patterns pivoted sharply toward online ordering. However, this momentum did not sustain through 2021 and 2022, as **trends in sales (-46%), average order value (AOV) (-10%), and order count (-40%) showed substantial declines.** Finding ways to maintain the value captured during 2020 and 2021 is key to continue towards sustained long term growth.

(sales,aov,order count chart)

### Seasonality Trends:

Typically, February and October underperform compared to the preceding months, while December and January boast high average sales due to the holiday season. Notably, in 2020, March sales surged 50% over February, an anomaly not reflecting the usual trend from 2019-2022, where March generally sees a modest increase over February.

## Product Performance

Gaming monitors and laptops are the basis of CoreTech's revenue stream. While these categories historically accounted for a maximum of 75% of total sales, 2021 stands out with an unprecedented concentration, reaching nearly 95% of all transactions. Interestingly, headphone sales, which previously represented 26% of revenue, were almost completely absent in 2021, potentially indicating either a data recording oversight or supply chain disruptions affecting product availability.

## Loyalty Program

In an aggregate of the past four years, the non-loyalty program generally outperformed the loyalty program, generating almost double (17M). However, a closer look at the trends reveals that the loyalty program surpassed the non-loyalty program in total sales in 2021 and in Average Order Value (AOV) in 2022. Loyalty customers also take almost 30% less time to make a purchase, with 1.6 months after account creation vs. 2.3 months for non-loyalty. Evidence suggests that the loyalty program's AOV has been steadily growing, as opposed to the volatile non-loyalty program.

## Regional Comparisons

North America grew in importance in 2022, increasing revenue share to 55% and order share to 53% among known region sales.

Sales and average order value (AOV) fell across all regions in 2022. North America remains the largest AOV with $242, 39% above Latin America, the lowest performer.

Europe, the Middle East, and Africa saw a significant increase in order volume share in 4Q22, climbing from 26% to 33% quarter-over-quarter among known region sales.

## Refund Rates

Headphones, making up an average of 45% of all product sales, demonstrate one of the lowest average return frequencies among all products (2%). In contrast, laptops (6%) and gaming monitors (22%), which sell in much smaller quantities, experience the highest rate of returns with a maximum of 18%. This pattern aligns with typical consumer behavior, as customers often purchase several headphone sets during the operational lifetime of a single laptop.

The sudden decline in returns observed in 2021 could be attributed to incomplete refund data, suggesting either data tracking complications or the implementation of new return restrictions. If such a no-refund policy was introduced in 2021, it would not only explain the absence of return data in 2022 but also likely have substantial effects on both buying patterns and overall customer contentment.

## Recommendations

Based on the uncovered insights, the following recommendations have been provided:

With 85% of orders and 70% of revenue coming from just three products, diversifying the product portfolio is crucial. Expanding the accessory category with new product lines, particularly Apple charging cables, would provide upsell opportunities.

Despite the general sales success of Apple products, iPhone sales have been disappointingly low (1% of revenue in 2022). Enhancing marketing efforts to previous Apple product buyers could boost sales.

Look to capitalize on the growing share of Samsung accessories (32% of order count in 2022) by introducing higher-cost Samsung products in already carried product categories such as laptops and cellphones.

Re-evaluate Bose SoundSport Headphones. As the product has never made up more than 1% of annual revenue, attempt to sell through the product by implementing bundle offers and flash sales to non-Apple ecosystem loyalty members before discontinuing.

Continue and push forward the loyalty program. In order to convert non-members, consider offering a one-time sign-up discount paired with increased general marketing of membership benefits and savings. Focus targeted and personalized ads to previous customers, and utilize past order data to increase marketing efforts when previously purchased products may need replacing.
