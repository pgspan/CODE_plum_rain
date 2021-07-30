# CODE_plum_rain

This code package is used to assess the impact of plum rain on the carbon emissions of the power system.

Before we begin, we need to install the Matlab software on a server and install the [Yalmip](https://yalmip.github.io/) optimization solution tool and the [Gurobi](https://www.gurobi.com/) or [Cplex](https://www.ibm.com/analytics/cplex-optimizer) solver. After configuring the above software, the specific solution process is as follows:

Based on the file named "Carbon_CapacityES_Cost_calculation.m", the carbon emissions and corresponding optimization results of the provincial power system, whether considering plum rain’s impact or not, are calculated. In this process, we can in sequence choose a year, a change trend fluctuation, a province, and finally, an option whether considering plum rain’s impact or not. The optimized results include the cost objective, carbon emissions, electric storage capacity, coal power output, gas power output, and hourly power balances during the plum rain period.

On this basis, four pathways to offset the plum rain’s incremental carbon emissions under the base case are given. Here we choose the year 2040, the change trend fluctuation of 0, and regardless of the impact of the plum rain. 

In the first pathway, based on the file of "C2N.m", the coal power is converted to natural gas power (C2N) to offset the plum rain’s incremental carbon emissions. Enter a province number when performing "C2N.m" to obtain the levelized cost of CO2 mitigation (LCCM) and hourly power balance from 2 July to 8 July.

In the C2N+DR pathway, based on the program "C2N_DR.m", C2N+DR is used to offset the plum rain’s incremental carbon emissions. Enter a province number when performing " C2N_DR.m " to obtain the levelized cost of CO2 mitigation (LCCM) and hourly power balances under different DR compensation costs and DR powers.

In the C2N+CCUS pathway, based on the program "C2N_CCUS.m", C2N+CCUS is used to offset the plum rain’s incremental carbon emissions. Enter a province number when performing " C2N_CCUS.m " to obtain the levelized cost of CO2 mitigation (LCCM), compensating energy and hourly power balances under different CCUS costs and CCUS efficiencies.

In the C2N+LD pathway, based on the program "C2N_LD.m", C2N+LD is used to offset the plum rain’s incremental carbon emissions. Enter a province number when performing "C2N_LD.m " to obtain the levelized cost of CO2 mitigation (LCCM), net released energy and hourly power balances under different LD power and energy capacity costs.

It should be noted that the default solution gap of Gorubi and Cplex is 1e-4. Therefore, the optimization results with different gaps will be slightly different, but it will not affect the substantive results of this article.

Note:
Set of years: 2020, 2030, 2040, 2050
Set of change trend fluctuations: 0, 0.25, -0.25
Set of provinces: 1-Jiangsu, 2-Anhui, 3-Zhejiang, 4-Jiangxi, 5-Hubei, 6-shanghai, 7-Hunan
In addition, 1 denotes considering plum rain impact, and 0 denotes not considering plum rain impact.
