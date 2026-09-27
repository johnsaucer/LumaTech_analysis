<p align="center">
  <img width="400" alt="Logo" src="https://github.com/user-attachments/assets/32808252-9cab-47b0-83bb-01be2b9c686b" />
</p>

# <p align="center"> E-commerce Analysis
**LumaTech** is a global e-commerce company that has sold more than **28M** dollars of popular electronics since its inception in 2019. With vast amounts of previously underutilized data on sales, product offerings, the loyalty program, and refunds, I am partnering with the head of the Operations team to thoroughly analyze this information and uncover critical insights. This analysis and recommendations will be used to enhance **LumaTech's** commercial performance across the sales, marketing, and product teams.

The Entity Relationship Diagram can be found [here](./path/to/file.md)

The SQL queries performed to uncover these insights can be found [here](https://github.com/johnsaucer/LumaTech_analysis/blob/main/Queries.sql)

# <p align="center"> Deep Dive Insights
## <p align="center"> Sales Trends
### Overview:

From 2019-2022, over **108K orders generated $28M in sales, with both metrics showing a 28% growth increase** over this four-year period. Particularly noteworthy, **sales surged dramatically by over 6M in 2020** during the onset of the pandemic, as consumer purchasing patterns pivoted sharply toward online ordering. However, this momentum did not sustain through 2021 and 2022, as **trends in sales (-46%), average order value (AOV) (-10%), and order count (-40%) showed substantial declines.** Finding ways to maintain the value captured during 2020 and 2021 is key to continue towards sustained long term growth.

<p align="center">
  <img width="54%" alt="Historical Monthly Rev" src="https://github.com/user-attachments/assets/87fad8c3-32e6-431d-81f4-02a0c8edcda2" />
  <img width="44%" alt="Growth rates heatmap" src="https://github.com/user-attachments/assets/8cf6c928-fb5f-4366-9816-bd62e91de9e3" />
</p>




### Seasonality Trends:

Sales typically dip in February and October relative to the months before them, while December and January run high on holiday demand. March 2020 stands out as an exception: sales climbed 50% over February, well beyond the modest March gains seen across 2019-2022. This spike coincided with the onset of the COVID-19 pandemic, which likely drove the unusual surge rather than any normal seasonal pattern.


## <p align="center"> Product Performance

Three products drive CoreTech's revenue: the 27in 4K gaming monitor, Apple AirPods headphones, and the MacBook Air laptop. Together they account for 85% of all-time revenue ($28.1M), with the monitor alone contributing 35%, AirPods 28%, and the MacBook 22%.

<p align="center">
  <img width="70%" alt="ChatGPT Image Sep 27, 2026, 04_46_44 PM" src="https://github.com/user-attachments/assets/0fdd8b91-fda1-4fed-ae27-0db8e3354dc9" />
</p>

The Apple iPhone posted the highest sales growth during the holiday season at 82%. At the other end, Bose Soundsport headphones significantly underperformed, generating less than 1% of total sales and falling 91% in 2022, the steepest decline of any product.

The 2020-2022 pattern was not product-specific. Every product declined in 2022, which suggests the business was reacting proportionally to post-COVID demand rather than losing ground in any one category.
## <p align="center"> Loyalty Program

Across the four years, non-loyalty customers generated more revenue than loyalty members, $17.1M versus $11.0M, or about 61% of the $28.1M total. The yearly trend tells a different story. Non-loyalty sales peaked at $7.2M in 2020 and fell to $2.2M by 2022, likely because that surge was driven by one-time buyers. Loyalty sales held up far better and passed non-loyalty in 2021 ($4.9M vs. $4.3M). By 2022, loyalty members made up about 55% of sales, up from 11% in 2019. They also placed more orders than non-loyalty customers from 2021 onward (19,552 vs. 16,306 in 2021). 
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty % Sales" src="https://github.com/user-attachments/assets/589eb5f9-df9d-4dd5-9864-d8ff1d443456" />

</p>

Average order value (AOV) shows the same divergence. Loyalty AOV climbed from $207 in 2019 to $249 in 2021 and held at $245 in 2022, while non-loyalty AOV was volatile, spiking to $345 in 2020 before dropping to $214 in 2022. That put loyalty ahead on AOV in 2022. Loyalty customers also make their first purchase sooner: 1.6 months after account creation vs. 2.3 months for non-loyalty, roughly 30% faster. Evidence suggests that the loyalty program's AOV has been steadily growing, as opposed to the volatile non-loyalty program
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty aov" src="https://github.com/user-attachments/assets/58d10bd7-fc3d-4dfa-a39c-695e79f57cf7" />

</p>

## <p align="center"> Regional Comparisons
North America is LumaTech's dominant market, generating $14.5M of the $28M in total sales, more than EMEA, APAC, and LATAM combined. EMEA is a distant second at $8.22M, while APAC and LATAM are minor markets. In 2022, North America's share of revenue rose to 55% and its share of orders to 53% among known region sales, tying the company's results even more closely to one region's behavior.
<p align="center">
  <img width="90%" alt="Yearly Sales By Region" src="https://github.com/user-attachments/assets/8f36da9a-728f-404e-946d-fdb0713b9b04" />

</p>
Sales and average order value (AOV) fell in every region in 2022. North America's AOV was $237, second only to APAC's $249 and 41% above LATAM, the lowest at $168. LATAM's AOV decline is the sharpest: after peaking at $295 in 2020, it fell to $215 in 2021 and $168 in 2022, a 43% drop. That is roughly double the 21-22% declines APAC, EMEA, and North America saw over the same period. The 2022 product mix helps explain it. LATAM leaned more into lower-priced accessories, with charging cable packs at 3.2% of its sales (vs. 1.3-1.6% elsewhere) and webcams at 3.9% (vs. 1.5-2.7%).


<p align="center">
<img width="90%" alt="AOV By Region" src="https://github.com/user-attachments/assets/265f8894-675c-4e14-b26c-40fdcb6d9a5f" />

</p>

## <p align="center"> Refund Rates

The stakeholder wants to focus on Apple products, so the Return Rate - Apple Products chart is the starting point. MacBook Air laptops have the highest refund rate of the three, at 18% in 2019 and 17% in 2020, before falling to 6% in 2021. iPhones followed a similar path (11%, 11%, 5%), and AirPods headphones were the lowest (6%, 10%, 4%). Averaged over 2019-2021, that works out to 13% for MacBooks, 9% for iPhones, and 7% for AirPods. Refund rates rise with price: AirPods sell for about $160, iPhones for about $710-$750, and MacBooks for about $1,500-$1,650. AirPods still generate the most Apple refunds by count (473 in 2019, 1,529 in 2020, 634 in 2021) because they sell in far greater volume. Apple refunds more than tripled from 545 in 2019 to 1,853 in 2020, alongside the pandemic sales surge. iPhone refund counts are tiny (4 to 13 per year), so those rates are volatile.

<p align="center">
<img width="700" height="400" alt="Return Rate - Apple Products" src="https://github.com/user-attachments/assets/9f3b95ab-da21-4ce4-8006-0ab0c30897fb" />
</p>

Across all products, the same pattern holds. ThinkPad laptops (14%) and MacBooks (13%) have the highest average refund rates, followed by iPhones (9%), gaming monitors (8%), AirPods (7%), webcams (4%), and charging cable packs (2%), with Bose soundsport headphones at 0%. The overall average is 6%. By share of total refunds, AirPods account for 49.0% and gaming monitors 26.9%, largely because of sales volume, while MacBooks make up 8.4% and ThinkPads 6.4%. This fits typical consumer behavior: low-priced accessories are returned least, and customers often buy several sets of headphones over the life of a single laptop.

The sharp decline in 2021 deserves scrutiny. The overall refund rate fell from 9% in 2020 to 4% in 2021, and every product declined, with the ThinkPad falling from 17% to 9% and the gaming monitor from 11% to 5%. Apple products show zero refunds in 2022. A drop this uniform is more likely a data issue than a change in customer behavior, pointing to either incomplete refund tracking or a new return restriction. If a no-refund policy was introduced in 2021, it would explain the missing 2022 data and would likely have affected both buying patterns and customer satisfaction.
## <p align="center"> Recommendations

Based on the uncovered insights, the following recommendations have been provided:

With 85% of orders and 70% of revenue coming from just three products, diversifying the product portfolio is crucial. Expanding the accessory category with new product lines, particularly Apple charging cables, would provide upsell opportunities.

Despite the general sales success of Apple products, iPhone sales have been disappointingly low (1% of revenue in 2022). Enhancing marketing efforts to previous Apple product buyers could boost sales.

Look to capitalize on the growing share of Samsung accessories (32% of order count in 2022) by introducing higher-cost Samsung products in already carried product categories such as laptops and cellphones.

Re-evaluate Bose SoundSport Headphones. As the product has never made up more than 1% of annual revenue, attempt to sell through the product by implementing bundle offers and flash sales to non-Apple ecosystem loyalty members before discontinuing.

Continue and push forward the loyalty program. In order to convert non-members, consider offering a one-time sign-up discount paired with increased general marketing of membership benefits and savings. Focus targeted and personalized ads to previous customers, and utilize past order data to increase marketing efforts when previously purchased products may need replacing.
