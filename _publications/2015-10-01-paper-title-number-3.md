---
title: "Multi-Time Scale Market Participation Strategy of Wind-Energy Storage Combined System Considering Uncertainty"
collection: publications
permalink: /publication/2015-10-01-paper-title-number-3
excerpt: 'This is an EI-indexed Chinese journal where I am both the student-first and corresponding author (in projects funded by the China State Grid Corporation, the first author of the paper is usually an employee of the company). I have translated the core content of the paper into English, and you can view it by clicking the link above.'
date: 2023-05-28
venue: 'Electric Power Automation Equipment'
#slidesurl: 'http://academicpages.github.io/files/slides3.pdf'
paperurl: 'http://WenrongWei2000.github.io/files/Multi-time.pdf'
citation: 'Xin Sun, Wenrong Wei*, et al. &quot;Multi-Time Scale Market Participation Strategy of Wind-Energy Storage Combined System Considering Uncertainty.&quot; <i>Electric Power Automation Equipment</i>. 2024.'
---

**ABSTRACT**:The significant uncertainty of wind power output severely hinders the accurate execution of electric market reporting plans, and the resulting power deviations may lead wind farms equipped with storage systems to incur high deviation penalties and wind curtailment losses. To mitigate the economic losses caused by incorrect bidding decisions, a multi-time scale market bidding model for wind farms is developed. Based on the existing market mechanisms in the United States, benefit and cost models for wind farms participating in the energy market and frequency regulation market are established. To improve the accuracy of bidding strategies, a quantitative model for wind power output uncertainty is developed using the Copula function, reserving part of the storage output capacity to reduce economic risks caused by power deviations. Aiming to maximize the expected net income of wind farms, day-ahead bidding strategies for the energy market and frequency regulation market are formulated, with bidding decisions adjusted based on ultra-short-term wind power forecast data in the intra-day stage. <u>A multi-time scale market participation strategy for wind farm equipped with energy storage is proposed, considering the uncertainty of wind power output.</u> Using a real-world wind farm in China as a case study, the results demonstrate that the proposed strategy can effectively enhance the economic benefits of wind farms while avoiding resource waste.

**Key Step 1: Model the uncertainty of wind power output with Copula Functions**

Based on the Copula function, we developed an uncertainty model to obtain the confidence interval of wind power. The specific steps are as follows:
<div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/流程图.png' alt="sym" width="100%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">The formulation process of the wind power uncertainty model</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">
The prediction accuracy of the static Copula function is relatively low, but it can obtain the confidence intervals of wind power for all time periods of the next day in one step. The dynamic Copula function offers higher prediction accuracy, but it can only model the wind power uncertainty for period l+1 based on the actual wind power output of period l, making it impossible to determine the confidence intervals for the remaining periods. Therefore, in our work, the static Gaussian Copula function, combined with day-ahead wind power forecast data, is used for the day-ahead bidding strategy, while the dynamic Copula function, together with ultra-short-term wind power forecast data, is employed for the intraday bidding strategy.
<div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/日前Copula.png' alt="sym" width="70%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">Interval prediction results based on day-ahead wind power forecast data</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">

<div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/日内Copula.png' alt="sym" width="70%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">Interval prediction results based on intraday wind power forecast data</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">

Then, in **Key Step 3**, we determine the reserved power of energy storage  based on the interval prediction results we obtained.

**Key Step 2: Establish market bidding model for wind farm equipped with energy storage**


Referring to the PJM market rules in the United States, we developed a benefit and cost model for wind farm (equipped with energy storage). The specific functions are presented in Equations (1) to (6) in this paper. 

Subsequently, we developed the bidding model based on the benefit and cost analysis. The relevant functions are presented in Equations (7) to (21) in this paper.

Additionally, the time framework for market bidding is illustrated in the figure below. By combining the time framework with the bidding model, a multi-time scale market participation strategy for wind farm equipped with energy storage is proposed in **Key Step 3**.

<div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/能量市场.png' alt="sym" width="70%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">Time frame of day-ahead energy market</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">

  <div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/调频市场.png' alt="sym" width="70%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">Time frame of frequency regulation market</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">
  
**Key Step 3: Multi-time scale market participation strategy**

Wind power exhibits significant uncertainty, and the accuracy of its point forecasts (including interval prediction results) gradually improves over time. In view of this, we have developed a multi-time-scale market participation strategy for wind farm (equipped with energy storage), tailored to different markets and their respective clearing time windows.

On the day-ahead stage, we formulated a day-ahead bidding strategy and determined the bidding power for the energy market.

In the intraday stage, we first re-quantified the wind power uncertainty based on ultra-short-term wind power forecast data and adjusted the reserved power of the energy storage (which was determined by the interval prediction results in **Key Step 1**). Secondly, considering the requirement that the bidding power in the energy market cannot be changed after day-ahead market clearing, along with the updated ultra-short-term wind power forecast data, we adjusted the output power of the energy storage to meet the requirements. Finally, after completing the adjustments to the reserved power and output power, the energy storage had more available capacity, which we then utilized to participate in the frequency regulation market.

<div class='paper-box'>
  <div class='paper-box-image'>
    <img src='../images/多时间尺度3.png' alt="sym" width="100%" style="display: block; margin: 0 auto;">
    <p style="text-align: center;">Flowchart of multi-time scale bidding strategy</p>
  </div>
</div>
<div class='paper-box-text' markdown="1">
