<p align="center">
  <img width="400" alt="Logo" src="https://github.com/user-attachments/assets/32808252-9cab-47b0-83bb-01be2b9c686b" />
</p>

# <p align="center"> E-commerce Analysis
**LumaTech** is a global e-commerce company that has sold more than **28M** dollars of popular electronics since its inception in 2019. With vast amounts of previously underutilized data on sales, product offerings, the loyalty program, and refunds, I am partnering with the head of the Operations team to thoroughly analyze this information and uncover critical insights. This analysis and recommendations will be used to enhance **LumaTech's** commercial performance across the sales, marketing, and product teams.

The Entity Relationship Diagram can be found [here](https://github.com/johnsaucer/LumaTech_analysis/blob/main/ERD.png)

The SQL queries performed to uncover these insights can be found [here](https://github.com/johnsaucer/LumaTech_analysis/blob/main/Queries.sql)

# <p align="center"> Deep Dive Insights
## <p align="center"> Sales Trends
### Overview:

- **2020 was a one-time spike.** Sales rose 163% to $10.2M. That single year made up 36% of all four years' revenue. Both demand and spend per order rose: order count doubled and AOV rose 31%.
- **2021 hid a problem.** Orders grew 6%, but sales fell 10%. The cause was the product mix. Laptop sales (MacBook + ThinkPad) dropped $1.3M, which covers the entire decline, while lower-priced monitors grew. Customers kept buying, but they bought cheaper items.
- **2022 undid the pandemic gains.** Sales fell 46% and orders fell 40%. AOV returned to $230, exactly the 2019 level. The 28% net growth from 2019 to 2022 came entirely from more orders; spend per order did not grow at all.
- **The business ended 2022 below where it started.** Q4 2022 sales ($649K) were 45% below Q4 2019. October 2022 ($178K) was the lowest month in the dataset. Momentum going into 2023 is negative.

<p align="center">
  <img width="54%" alt="Historical Monthly Rev" src="https://github.com/user-attachments/assets/87fad8c3-32e6-431d-81f4-02a0c8edcda2" />
  <img width="44%" alt="Growth rates heatmap" src="https://github.com/user-attachments/assets/8cf6c928-fb5f-4366-9816-bd62e91de9e3" />
</p>




### Seasonality Trends:

**Holiday demand is the most reliable pattern in the data.** November and December grew month over month every year, even in 2022 (+17%, +26%). This is the best window for promotions.
- **February and October are consistent soft spots.** February typically drops about 32% from January, and October about 18–26% from September. Both are candidates for off-peak promotions.
- **October 2022 (-55% MoM) broke the pattern.** A drop that far outside the normal range suggests an event beyond seasonality and should be investigated.
- **March 2020 (+50%)** marks the start of the COVID surge, compared with the usual 6–11% March lift.


## <p align="center"> Product Performance

- **Revenue is highly concentrated.** The gaming monitor (35%), AirPods (28%), and MacBook Air (22%) generate 85% of revenue, so these three products largely determine company performance.

<p align="center">
  <img width="70%" alt="ChatGPT Image Sep 27, 2026, 04_46_44 PM" src="https://github.com/user-attachments/assets/0fdd8b91-fda1-4fed-ae27-0db8e3354dc9" />
</p>

- **Laptops rose the most in 2020 and fell the most afterward.** MacBook (+384%) and ThinkPad (+222%) led the 2020 growth, likely because of work-from-home demand. MacBook then fell 35% in 2021 and 55% in 2022.
- **The gaming monitor is the most resilient core product.** It was the only top product to grow in 2021 (+8%). Its 2022 sales still finished 35% above 2019.
- **The 2022 decline was across the board.** Every product fell, and the four largest each lost $0.5–1.4M. This points to a drop in overall demand rather than a problem with any single product.
- **iPhone is underused.** It accounts for about 1% of revenue, yet it shows the strongest holiday growth (82%). Demand exists but is not being captured the rest of the year.
- **Bose SoundSport is dead weight.** It produced $3.3K in total revenue over four years, 0.01% of sales.
## <p align="center"> Loyalty Program

- **All net growth came from loyalty members.** From 2019 to 2022, loyalty sales rose from $0.4M to $2.7M (+$2.3M). Non-loyalty sales fell from $3.5M to $2.2M, ending below their 2019 level.
- **Non-loyalty demand was mostly temporary.** Non-loyalty sales peaked at $7.2M in 2020 and then fell 69% by 2022, the pattern of one-time pandemic buyers. Losing these buyers is the main cause of the downturn.
- **Loyalty members became the core customer base.** They passed non-loyalty sales in 2021 and made up 55% of sales and 52% of orders in 2022, up from 11% of sales in 2019.
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty % Sales" src="https://github.com/user-attachments/assets/589eb5f9-df9d-4dd5-9864-d8ff1d443456" />

</p>

- **Loyalty spending per order is steadier.** Loyalty AOV stayed within $207–249 across all four years. Non-loyalty AOV swung from $214 to $345. In 2022, loyalty AOV held at $245 while non-loyalty AOV fell to $214.
- **Loyalty members still declined in 2022, but through fewer orders, not smaller orders.** Loyalty orders fell 43% while their AOV held steady. The problem to solve is purchase frequency, not spend per order.
- **Loyalty members buy sooner.** Their first purchase comes 1.6 months after sign-up, versus 2.3 months for non-loyalty customers (about 30% faster).
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty aov" src="https://github.com/user-attachments/assets/58d10bd7-fc3d-4dfa-a39c-695e79f57cf7" />

</p>

## <p align="center"> Regional Comparisons
- **North America is the main market.** It produced $14.6M (52% of sales), more than EMEA ($8.2M), APAC ($3.7M), and LATAM ($1.7M) combined.
- **All regions rose and fell together.** Every region grew 151–213% in 2020 and declined in 2022. Because the swings were shared, the downturn was global rather than regional.
- **North America's 2022 share gain reflects the other regions falling faster.** North America declined 39%, while the other regions fell 51–56%. This pushed its share to about 55%. Relying on North America is safer in the short term but increases concentration risk.

<p align="center">
  <img width="90%" alt="Yearly Sales By Region" src="https://github.com/user-attachments/assets/8f36da9a-728f-404e-946d-fdb0713b9b04" />
</p>

- **LATAM has a spend-per-order problem.** Its AOV fell 43% from 2020 to 2022 ($295 → $168), about twice the 21–22% drop elsewhere. The cause is product mix. In 2022, cable packs (3.2%) and webcams (3.9%) made up roughly double their share of sales in other regions. LATAM customers are still buying, but mostly low-priced accessories.

<p align="center">
<img width="90%" alt="AOV By Region" src="https://github.com/user-attachments/assets/265f8894-675c-4e14-b26c-40fdcb6d9a5f" />
</p>

## <p align="center"> Refund Rates

### Apple Products (stakeholder focus)
- **MacBook Air has the highest refund rate:** 18% → 17% → 6% (2019–2021), for a **13% average**.
- **iPhone:** 11% → 11% → 5% (**9% average**). Only 4–13 refunds per year, so this rate is volatile.
- **AirPods:** 6% → 10% → 4% (**7% average**).
- **Refund rate rises with price:** AirPods sell for ~$160, iPhones for ~$710–750, and MacBooks for ~$1,500–1,650.
- **AirPods lead Apple in refund *count*** (473 → 1,529 → 634) because of their sales volume.
- **Apple refunds more than tripled in 2020** (545 → 1,853), alongside the sales surge.

<p align="center">
<img width="80%" alt="ChatGPT Image Sep 27, 2026, 05_42_28 PM" src="https://github.com/user-attachments/assets/ca35fc9c-39ed-409a-aa67-09335e232cf3" />

</p>

### All Products
- **Average refund rate (2019–2021):** ThinkPad **14%**, MacBook **13%**, iPhone 9%, monitor 8%, AirPods 7%, webcam 4%, cable pack 2%, Bose 0%. The overall average is **6%**.
- **Share of total refunds:** AirPods **49.0%**, monitor **26.9%**, MacBook 8.4%, ThinkPad 6.4%. These shares are driven mainly by volume.
- **Pattern:** low-priced accessories are returned least; high-priced laptops are returned most.

### Data Quality Flag
- **2021 refunds fell sharply for every product** (overall 9% → 4%; ThinkPad 17% → 9%; monitor 11% → 5%).
- **2022 shows zero refunds** across all products.
- **Likely cause:** a drop this uniform points to **incomplete refund tracking or a new return restriction**, not a change in customer behavior.
- **What to check:** if a no-refund policy began in 2021, it may also have affected purchasing and customer satisfaction. This should be confirmed with the Operations team.

## <p align="center"> Recommendations
- **Diversify beyond the top 3 products.** 85% of revenue comes from three products. Expand accessories (e.g., Apple charging cables) to create upsell opportunities.
- **Push iPhone marketing to existing Apple buyers.** iPhones are ~1% of revenue but show the strongest holiday growth. Concentrate campaigns in Nov–Dec.
- **Grow the Samsung line.** Samsung accessories are a growing share of orders. Consider adding higher-priced Samsung products in categories LumaTech already carries (laptops, phones).
- **Sell through, then discontinue, Bose SoundSport.** It has never exceeded 1% of revenue. Use bundles and flash sales first.
- **Invest in the loyalty program.** Members are more stable, have higher AOV, and buy sooner.
  - Offer a one-time sign-up discount to convert non-members.
  - Use past order data for targeted replacement and upgrade campaigns.
- **Protect LATAM AOV.** Bundle low-priced accessories with core products to lift order value.
- **Investigate the refund data gap** before drawing conclusions from 2021–2022 refund trends.
