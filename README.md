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

- **2020 was the peak year:** sales rose **163%** to $10.2M (+$6.3M), with AOV up 31% and order count up 101%, driven by the pandemic shift to online shopping.
- **2021 was mixed:** order count grew 6%, but AOV fell 15% ($300 → $255). This led to a **10% drop in sales**. More customers bought, but they spent less per order.
- **2022 was the worst year:** sales fell **46%**, AOV fell 10%, and order count fell 40%.
- **Net 4-year change:** sales and order count are both up ~28% from 2019 to 2022, but most of the 2020 gains were lost.
- **Best single month:** December 2020 at **$1.25M**.
- **2022 got worse as the year went on:** sales were down year over year in every month, and from August onward the declines reached 48–73%.

<p align="center">
  <img width="54%" alt="Historical Monthly Rev" src="https://github.com/user-attachments/assets/87fad8c3-32e6-431d-81f4-02a0c8edcda2" />
  <img width="44%" alt="Growth rates heatmap" src="https://github.com/user-attachments/assets/8cf6c928-fb5f-4366-9816-bd62e91de9e3" />
</p>




### Seasonality Trends:

- **February** drops sharply from January every year (-31% to -33%), except in 2020 (+4%).
- **October** is consistently the weakest month (-18% to -26% MoM). October 2022 was an outlier at **-55%**, which suggests something beyond normal seasonality.
- **November–December** show a holiday surge every year, including 2022.


## <p align="center"> Product Performance

- **Three products drive 85% of all-time revenue ($28.1M):**
  - 27in 4K gaming monitor: **35%** ($9.85M)
  - Apple AirPods headphones: **28%** ($7.74M)
  - MacBook Air laptop: **22%** ($6.30M)
- **Revenue share is stable:** this top-3 share held steady from 2019 to 2022.

<p align="center">
  <img width="70%" alt="ChatGPT Image Sep 27, 2026, 04_46_44 PM" src="https://github.com/user-attachments/assets/0fdd8b91-fda1-4fed-ae27-0db8e3354dc9" />
</p>

- **2020 growth was broad-based:** MacBook +384%, ThinkPad +222%, iPhone +170%, monitor +114%, AirPods +99%.
- **Every product declined in 2022:** drops ranged from -31% (webcam) to -91% (Bose). The downturn was not tied to any single product; demand fell proportionally after COVID.
- **Samsung Webcam** was the only product to grow in 2021 (**+134%**), while overall sales fell 10%. However, it makes up only 1% of all-time sales.
- **Apple iPhone** posted the strongest holiday-season growth (**82%**), but it accounts for only ~1% of revenue ($213K all-time).
- **Bose SoundSport headphones** are the weakest product: **<1% of revenue** ($3.3K all-time) and a **91% decline** in 2022.
## <p align="center"> Loyalty Program

- **All-time sales:** non-loyalty customers still lead, at **$17.1M (61%)** vs. **$11.0M** for loyalty members.
- **Loyalty members overtook non-loyalty in 2021:** loyalty sales were **$4.9M vs. $4.3M**, and loyalty orders were **19,552 vs. 16,306**. Loyalty members stayed ahead in 2022.
- **Loyalty share of sales grew from 11% (2019) to 55% (2022).**
- **Non-loyalty sales were a 2020 spike:** they peaked at $7.2M, then fell to $2.2M by 2022. This points to one-time pandemic buyers, and their exit is a major reason for the downturn.
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty % Sales" src="https://github.com/user-attachments/assets/589eb5f9-df9d-4dd5-9864-d8ff1d443456" />

</p>

- **Loyalty AOV is steady and rising:** $207 → $228 → $249 → $245 (2019–2022).
- **Non-loyalty AOV is volatile:** $233 → **$345** → $261 → $214. The monthly peak was ~$384 in late 2020.
- **2022:** loyalty AOV passed non-loyalty AOV ($245 vs. $214). During the downturn, non-loyalty AOV dropped sharply while loyalty AOV barely moved.
- **Faster first purchase:** loyalty members buy **1.6 months** after account creation, vs. **2.3 months** for non-loyalty (~30% faster).
<p align="center">
<img width="70%" alt="Loyalty Non-Loyalty aov" src="https://github.com/user-attachments/assets/58d10bd7-fc3d-4dfa-a39c-695e79f57cf7" />

</p>

## <p align="center"> Regional Comparisons
- **North America dominates:** it generated **$14.6M** of $28.1M, more than EMEA, APAC, and LATAM combined.
- **EMEA** is second at **$8.2M**. **APAC** ($3.7M) and **LATAM** ($1.7M) are minor markets.
- **Regional mix is mostly flat year to year.** NA's share rose to **~55%** of 2022 sales (from ~49% in 2021), tying results even more closely to one region.
- **2020:** every region grew 151–213%.
- **2022:** every region declined. APAC fell -52%, EMEA -51%, and LATAM -56%, while NA held up best at **-39%**.
<p align="center">
  <img width="90%" alt="Yearly Sales By Region" src="https://github.com/user-attachments/assets/8f36da9a-728f-404e-946d-fdb0713b9b04" />

</p>
- **2022 AOV by region:** APAC **$249**, NA **$237**, EMEA **$225**, LATAM **$168** (NA is 41% above LATAM).
- **LATAM's AOV fell the most:** $295 → $215 → **$168** (2020–2022), a **43% drop**. That is roughly double the 21–22% declines in the other regions.
- **Why:** LATAM's 2022 mix leaned toward cheaper accessories:
  - Charging cable packs: 3.2% of sales (vs. 1.3–1.6% elsewhere)
  - Webcams: 3.9% of sales (vs. 1.5–2.7% elsewhere)

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
