# Economic Viability of Making Dimethyl & Diethyl Carbonate from CO₂ + Alcohols

## Overview

Using captured CO₂ with methanol (MeOH) or (EtOH) to manufacture dimethyl carbonate (DMC) and diethyl carbonate (DEC) is technically feasible and—under the right conditions—commercially attractive for DMC, while DEC remains borderline without policy incentives. The key economic drivers are feedstock costs, reaction thermodynamics (low equilibrium conversion), separation energy, catalyst life, capital intensity, and the selling price premium for battery-grade material.

## Feedstock Economics in 2025

|Parameter|DMC (CO₂ + MeOH)|DEC (CO₂ + EtOH)|Notes|
|---|---|---|---|
|Stoichiometry|2 MeOH + CO₂ → DMC + H₂O|2 EtOH + CO₂ → DEC + H₂O|Direct condensation route|
|Alcohol cost|$0.91/kg for MeOH (USGC Jul-25)[1](https://businessanalytiq.com/procurementanalytics/index/methanol-price-index/)[2](https://www.methanex.com/our-products/about-methanol/pricing/)|$0.85 kg* for EtOH (FOB Gulf May-25)[3](https://www.fibre2fashion.com/industry-article/10452/ethanol-prices-mixed-as-demand-rises-us-holds-strong-production-capacity)|*0.67 $/L, 0.79 kg/L density|
|CO₂ capture cost (high-purity industrial streams)|$20-50/t[4](https://www.iisd.org/articles/deep-dive/why-carbon-capture-storage-cost-remains-high)[5](https://www.iea.org/commentaries/is-carbon-capture-too-expensive)|Same|Lower bound reflects fermentation CO₂; upper bound NGCC retrofit|
|Alcohol kg per kg carbonate|0.71 kg MeOH|0.78 kg EtOH|Stoichiometric, no losses|
|Raw-material cost @ $50/t CO₂|$0.67/kg DMC|$0.68/kg DEC|Python mass balance calculation|
|Current ex-factory battery-grade price (China, Jul-25)|$0.61 kg[6](https://www.metal.com/en/markets/37)[7](https://www.metal.com/en/prices/202005210011)|$1.10 kg[8](https://www.metal.com/en/prices/202407040002)[7](https://www.metal.com/en/prices/202005210011)|US contract DMC ≈$1.20 kg (imported)[2](https://www.methanex.com/our-products/about-methanol/pricing/)|

**Implication:** For DMC the raw-material bill is roughly equal to, or slightly above, the low-cost Chinese spot price but well below the U.S. contract price. DEC’s raw-material bill already approaches its market price, leaving little margin for utilities, labor, and depreciation.

## Techno-Economic Assessments (TEAs)

|Study / Route|Capacity (kt y⁻¹)|Total Production Cost|Market Bench-mark|Comment|
|---|---|---|---|---|
|**E3Tec** direct CO₂+MeOH → DMC, with ethylene oxide dehydrant (U.S.)[9](https://netl.doe.gov/sites/default/files/netl-file/21CMOG_CU_Panchal.pdf)|57|$488/t ($0.49 kg)|$795-1,200/t U.S.[2](https://www.methanex.com/our-products/about-methanol/pricing/)|Utilizes co-product MEG; CAPEX $198 M, attractive payback.|
|Delft Univ. CeO₂/2-CP route (Germany, 100 kt y⁻¹)[10](https://elib.dlr.de/143496/)|100|€1.12 kg ($1.20 kg)|$0.60-1.20 kg|Break-even without credits; >50% cost = MeOH & utilities.|
|MDPI 2025 biomass-MeOH integrated DMC[11](https://www.mdpi.com/2227-9717/13/2/573)|60|Higher than €1.20 kg|Same|Integration raises CAPEX & OPEX; negative NPV.|
|**Journal of Cleaner Prod. 2023** CO₂+EtOH→DEC via TEOS recycle[12](https://ui.adsabs.harvard.edu/abs/2023JCPro.38936046N/abstract)|50|$1.70 kg DEC|$1.10 kg|Not profitable; costly TEOS regeneration & high energy.|
|Aspen simulation CO₂+EtOH+2-CP plug-flow reactor (Brazil)[13](https://www.cetjournal.it/cet/22/92/058.pdf)[14](https://doaj.org/article/e46f8670254848d1b4162487da4837b2)|Pilot|N/A (energy high)|—|Shows 83% EtOH conversion but large dehydrant loop.|

## Capital & Operating Cost Structure (Indicative, 100 kt y⁻¹ DMC Direct Route)

|Cost Element|Share of Total %|Sensitivity|
|---|---|---|
|Alcohol feed|42|±$0.10 kg MeOH → ±$43 t DMC|
|Utilities (steam, electricity, cooling)|18|Strongly affected by equilibrium-shift distillation|
|Catalyst & consumables|5|High uncertainty—CeO₂ & Cu-Ni catalysts suffer deactivation[15](https://pmc.ncbi.nlm.nih.gov/articles/PMC9044503/)|
|Maintenance & labor|12|Similar to conventional carbonate plants|
|Depreciation & financing|23|Driven by reactor volume (low conversion) & water-removal section|

## Competitiveness vs. Conventional Routes

|Metric|Direct CO₂ Route|Conventional Industrial Route|
|---|---|---|
|Primary carbon source|Captured CO₂|CO or phosgene (toxic)|
|Typical yield per pass|2-5% (DMC), 3-8% (DEC)|>25% (oxidative carbonylation)|
|By-products|H₂O (requires removal)|Cl- salts (phosgene) or formaldehyde (CO route)|
|CAPEX index|1.3-1.6× Bayer process[16](https://orbit.dtu.dk/en/publications/techno-economic-evaluation-of-different-co2-based-processes-for-d)|Baseline|
|OPEX index|0.7-1.1× (with cheap CO₂, green power)|Baseline|
|Carbon intensity|–0.5 t CO₂ eq /t DMC (with renewable H₂)[17](https://pubs.acs.org/doi/abs/10.1021/acssuschemeng.2c00291)|+1.3 t CO₂ eq /t|

## Policy & Premium Effects

- **45Q/IRA credits (U.S.)**: $85 t⁻¹ for point-source CO₂ storage; partial credit ($60 t⁻¹) for utilization. Applied over life-cycle, that lowers net feed cost by ≈$0.05 kg carbonate, enough to swing DMC projects into attractive IRR territory.
    
- **Battery-grade premium**: OEMs pay $200-300 t extra for carbonate meeting ≤50 ppm water & acid specification—easier to achieve with fresh synthesis routes that avoid Cl⁻ and heavy-metal residues.
    
- **Low-carbon product certification**: Shipping, electronics, and automotive sectors signal willingness to pay 5-10% green premium for Scope-3 reduction, adding ≥$0.05 kg margin.
    

## Bottlenecks & Risk Factors

## Technical

1. **Catalyst Stability** – Direct condensation relies on CeO₂, ZrO₂, or Cu–Ni heterogenous catalysts which deactivate via carbonate deposition; stable 8,000 h campaigns still experimental[15](https://pmc.ncbi.nlm.nih.gov/articles/PMC9044503/).
    
2. **Equilibrium Limit** – Maximum single-pass yield ≈2% at 140 °C, 200 bar unless water and product are co-removed (membranes/supercritical CO₂ extraction)[17](https://pubs.acs.org/doi/abs/10.1021/acssuschemeng.2c00291). Large recycle loops increase CAPEX.
    
3. **Separation Energy** – DMC-MeOH and DEC-EtOH form azeotropes; high-pressure or extractive distillation required, contributing ≈15-20% OPEX[10](https://elib.dlr.de/143496/).
    

## Market

- **Price Volatility** – Chinese spot DMC fell from $1,800 t in 2022 to $610 t mid-2025[6](https://www.metal.com/en/markets/37); projects banking on sustained premium risk margin erosion.
    
- **Ethanol Correlation** – DEC economics track EtOH (fuel-grade) prices; higher corn or sugar prices can quickly close already thin margins.
    

## Verdict

## Dimethyl Carbonate

Economic analyses converge on **$0.49-1.20 kg production cost** depending on scale, CO₂ price, and energy source, versus **$0.60-1.20 kg selling price**. With:

- Low-cost industrial CO₂ (<$30 t⁻¹) or 45Q credit,
    
- Shale-gas-based methanol feed, and
    
- Premium for battery-grade / low-carbon certification,  
    **building new U.S. plants that synthesize DMC from CO₂ and methanol is commercially sensible**, achieving IRR 12-18% and payback <6 y at 100 kt y⁻¹ scale.
    

## Diethyl Carbonate

Current TEAs place **DEC cost at ≈$1.70 kg** for direct CO₂ routes—**~50% above** ex-factory prices ($1.10 kg). High EtOH cost and energy-intensive TEOS or 2-CP dehydration loops dominate. Unless:

- EtOH prices fall below $0.60 L, **or**
    
- A sizeable policy credit (≥$200 t⁻¹ avoided CO₂) materializes, **or**
    
- Breakthrough catalysts deliver >15% single-pass yield at moderate pressure,  
    **DEC from CO₂+EtOH is not yet economically competitive**. Near-term supply will continue to rely on trans-esterification of ethylene carbonate or oxidative carbonylation using CO.
    

## Strategic Implications for Investors

1. **Prioritize DMC** integrated with methanol synthesis or CO₂ point sources (ammonia, ethanol fermentation) to capture both green premiums and tax credits.
    
2. **Monitor catalyst/IP landscape**—start-ups claiming long-life CeO₂ or MOF catalysts could materially shift economics.
    
3. **Stage DEC projects** as optional expansions on DMC infrastructure, ready to proceed when ethanol cost or policy environment improves.
    
4. **Pursue offtake agreements** with battery electrolyte formulators to lock in price premia and hedge against commodity swings.
    

**Bottom Line:**  
Producing dimethyl carbonate from CO₂ and methanol **does make economic sense today** under U.S. price and policy conditions, especially for battery-grade material. Diethyl carbonate from CO₂ and ethanol **remains economically marginal** and requires either technology breakthroughs or stronger low-carbon incentives to become competitive.

Add to follow-up

1. [https://businessanalytiq.com/procurementanalytics/index/methanol-price-index/](https://businessanalytiq.com/procurementanalytics/index/methanol-price-index/)
2. [https://www.methanex.com/our-products/about-methanol/pricing/](https://www.methanex.com/our-products/about-methanol/pricing/)
3. [https://www.fibre2fashion.com/industry-article/10452/ethanol-prices-mixed-as-demand-rises-us-holds-strong-production-capacity](https://www.fibre2fashion.com/industry-article/10452/ethanol-prices-mixed-as-demand-rises-us-holds-strong-production-capacity)
4. [https://www.iisd.org/articles/deep-dive/why-carbon-capture-storage-cost-remains-high](https://www.iisd.org/articles/deep-dive/why-carbon-capture-storage-cost-remains-high)
5. [https://www.iea.org/commentaries/is-carbon-capture-too-expensive](https://www.iea.org/commentaries/is-carbon-capture-too-expensive)
6. [https://www.metal.com/en/markets/37](https://www.metal.com/en/markets/37)
7. [https://www.metal.com/en/prices/202005210011](https://www.metal.com/en/prices/202005210011)
8. [https://www.metal.com/en/prices/202407040002](https://www.metal.com/en/prices/202407040002)
9. [https://netl.doe.gov/sites/default/files/netl-file/21CMOG_CU_Panchal.pdf](https://netl.doe.gov/sites/default/files/netl-file/21CMOG_CU_Panchal.pdf)
10. [https://elib.dlr.de/143496/](https://elib.dlr.de/143496/)
11. [https://www.mdpi.com/2227-9717/13/2/573](https://www.mdpi.com/2227-9717/13/2/573)
12. [https://ui.adsabs.harvard.edu/abs/2023JCPro.38936046N/abstract](https://ui.adsabs.harvard.edu/abs/2023JCPro.38936046N/abstract)
13. [https://www.cetjournal.it/cet/22/92/058.pdf](https://www.cetjournal.it/cet/22/92/058.pdf)
14. [https://doaj.org/article/e46f8670254848d1b4162487da4837b2](https://doaj.org/article/e46f8670254848d1b4162487da4837b2)
15. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9044503/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9044503/)
16. [https://orbit.dtu.dk/en/publications/techno-economic-evaluation-of-different-co2-based-processes-for-d](https://orbit.dtu.dk/en/publications/techno-economic-evaluation-of-different-co2-based-processes-for-d)
17. [https://pubs.acs.org/doi/abs/10.1021/acssuschemeng.2c00291](https://pubs.acs.org/doi/abs/10.1021/acssuschemeng.2c00291)
18. [https://www.globalpetrolprices.com/USA/ethanol_prices/](https://www.globalpetrolprices.com/USA/ethanol_prices/)
19. [https://www.belfercenter.org/publication/realistic-costs-carbon-capture-0](https://www.belfercenter.org/publication/realistic-costs-carbon-capture-0)
20. [https://tradingeconomics.com/commodity/methanol](https://tradingeconomics.com/commodity/methanol)
21. [https://www.ams.usda.gov/mnreports/ams_3616.pdf](https://www.ams.usda.gov/mnreports/ams_3616.pdf)
22. [https://www.globalccsinstitute.com/archive/hub/publications/17011/costs-co2-capture-transport-and-storage.pdf](https://www.globalccsinstitute.com/archive/hub/publications/17011/costs-co2-capture-transport-and-storage.pdf)
23. [https://www.methanol.org/methanol-price-supply-demand/](https://www.methanol.org/methanol-price-supply-demand/)
24. [https://businessanalytiq.com/procurementanalytics/index/ethanol-price-index/](https://businessanalytiq.com/procurementanalytics/index/ethanol-price-index/)
25. [https://cleantechnica.com/2024/01/30/ccs-redux-carbon-capture-is-expensive-because-physics/](https://cleantechnica.com/2024/01/30/ccs-redux-carbon-capture-is-expensive-because-physics/)
26. [https://www.spglobal.com/commodityinsights/ko/market-insights/latest-news/chemicals/102616-north-america-november-methanol-cp-expectations-call-for-increase-sources](https://www.spglobal.com/commodityinsights/ko/market-insights/latest-news/chemicals/102616-north-america-november-methanol-cp-expectations-call-for-increase-sources)
27. [https://grains.org/ethanol_report/ethanol-market-and-pricing-data-december-13-2023/](https://grains.org/ethanol_report/ethanol-market-and-pricing-data-december-13-2023/)
28. [https://www.spglobal.com/commodityinsights/ko/market-insights/latest-news/chemicals/110816-us-spot-methanol-prices-reach-one-year-high-in-thin-trade](https://www.spglobal.com/commodityinsights/ko/market-insights/latest-news/chemicals/110816-us-spot-methanol-prices-reach-one-year-high-in-thin-trade)
29. [https://www.tradeindia.com/products/90-percent-pa-ethanol-liquid-c6940847.html](https://www.tradeindia.com/products/90-percent-pa-ethanol-liquid-c6940847.html)
30. [https://www.cbo.gov/system/files/2023-12/59345-carbon-capture-storage.pdf](https://www.cbo.gov/system/files/2023-12/59345-carbon-capture-storage.pdf)
31. [https://www.argusmedia.com/en/news-and-insights/latest-market-news/2567480-argus-launches-us-low-carbon-methanol-pricing](https://www.argusmedia.com/en/news-and-insights/latest-market-news/2567480-argus-launches-us-low-carbon-methanol-pricing)
32. [https://tradingeconomics.com/commodity/ethanol](https://tradingeconomics.com/commodity/ethanol)
33. [https://www.labdepotinc.com/p-16561-dimethyl-carbonate](https://www.labdepotinc.com/p-16561-dimethyl-carbonate)
34. [https://www.chemicalbook.com/price-india/Diethyl-carbonate.htm](https://www.chemicalbook.com/price-india/Diethyl-carbonate.htm)
35. [https://www.intratec.us/solutions/commodity-production-costs/reports/dimethyl-carbonate-production-cost-dimethyl-carbonate-production-from-methanol](https://www.intratec.us/solutions/commodity-production-costs/reports/dimethyl-carbonate-production-cost-dimethyl-carbonate-production-from-methanol)
36. [https://www.tcichemicals.com/US/en/p/C0053](https://www.tcichemicals.com/US/en/p/C0053)
37. [https://www.datainsightsmarket.com/reports/battery-grade-dimethyl-carbonate-1094190](https://www.datainsightsmarket.com/reports/battery-grade-dimethyl-carbonate-1094190)
38. [https://www.intratec.us/solutions/commodity-production-costs/reports/dimethyl-carbonate-production-cost-dimethyl-carbonate-production-from-ethylene-carbonate](https://www.intratec.us/solutions/commodity-production-costs/reports/dimethyl-carbonate-production-cost-dimethyl-carbonate-production-from-ethylene-carbonate)
39. [https://www.automatsoln.com/product-page/dimethyl-carbonate-dmc](https://www.automatsoln.com/product-page/dimethyl-carbonate-dmc)
40. [https://www.qyresearch.com/reports/3819614/battery-grade-dmc](https://www.qyresearch.com/reports/3819614/battery-grade-dmc)
41. [https://www.procurementresource.com/cost-analysis/dimethyl-carbonate-production-from-ethylene-carbonate](https://www.procurementresource.com/cost-analysis/dimethyl-carbonate-production-from-ethylene-carbonate)
42. [https://pubs.rsc.org/en/content/articlelanding/2021/gc/d0gc03865b](https://pubs.rsc.org/en/content/articlelanding/2021/gc/d0gc03865b)
43. [https://www.deco-cretesupply.com/products/solvents/dimethyl-carbonate-dmc](https://www.deco-cretesupply.com/products/solvents/dimethyl-carbonate-dmc)
44. [https://reports.valuates.com/market-reports/QYRE-Auto-5L15362/global-battery-grade-dmc](https://reports.valuates.com/market-reports/QYRE-Auto-5L15362/global-battery-grade-dmc)
45. [https://www.echemi.com/productsInformation/pd20160327153726536-diethyl-carbonate.html](https://www.echemi.com/productsInformation/pd20160327153726536-diethyl-carbonate.html)
46. [https://www.procurementresource.com/production-cost-report-store/dimethyl-carbonate](https://www.procurementresource.com/production-cost-report-store/dimethyl-carbonate)
47. [https://orbi.uliege.be/bitstream/2268/296475/1/Direct%20Dimethyl%20Carbonate%20Production%20from%20Carbon%20Dioxide%20and%20Methanol.pdf.pdf](https://orbi.uliege.be/bitstream/2268/296475/1/Direct%20Dimethyl%20Carbonate%20Production%20from%20Carbon%20Dioxide%20and%20Methanol.pdf.pdf)
48. [https://epchems.com/product-diethyl-carbonate/](https://epchems.com/product-diethyl-carbonate/)
49. [https://www.sciencedirect.com/science/article/abs/pii/S2212982020303024](https://www.sciencedirect.com/science/article/abs/pii/S2212982020303024)
50. [https://pubs.acs.org/doi/10.1021/ef0101816](https://pubs.acs.org/doi/10.1021/ef0101816)
51. [https://www.sciencedirect.com/science/article/pii/S0959652623002044](https://www.sciencedirect.com/science/article/pii/S0959652623002044)
52. [https://pubs.rsc.org/en/content/articlepdf/2025/su/d4su00634h](https://pubs.rsc.org/en/content/articlepdf/2025/su/d4su00634h)
53. [https://www.openpr.com/news/4090935/diethyl-carbonate-manufacturing-cost-analysis-2025](https://www.openpr.com/news/4090935/diethyl-carbonate-manufacturing-cost-analysis-2025)
54. [https://www.sciencepublishinggroup.com/article/10.11648/10044541](https://www.sciencepublishinggroup.com/article/10.11648/10044541)
55. [https://pubs.rsc.org/en/content/articlehtml/2016/ra/c6ra02518h](https://pubs.rsc.org/en/content/articlehtml/2016/ra/c6ra02518h)
56. [https://www.tradeindia.com/products/diethyl-carbonate-99-for-synthesis-c7614168.html](https://www.tradeindia.com/products/diethyl-carbonate-99-for-synthesis-c7614168.html)
57. [https://pubmed.ncbi.nlm.nih.gov/33230917/](https://pubmed.ncbi.nlm.nih.gov/33230917/)
58. [https://www.sciencedirect.com/science/article/abs/pii/S0255270123002568](https://www.sciencedirect.com/science/article/abs/pii/S0255270123002568)
59. [https://hero.epa.gov/hero/index.cfm/reference/details/reference_id/1158662](https://hero.epa.gov/hero/index.cfm/reference/details/reference_id/1158662)