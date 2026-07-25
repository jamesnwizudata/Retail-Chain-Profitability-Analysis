# Retail-Chain-Profitability-Analysis

Executive Summary

The company is profitable overall (8.69% margin), but that number hides real, identifiable profit loss driven largely by unmanaged discounting. This analysis modeled transaction-level sales data in Power BI to pinpoint exactly where that profit was going, verifying each finding down to the individual transaction before recommending action. The recommended next steps are to cap discounting above 20% on the affected product lines and require manager approval for large discounts on high-value orders. The impact: discounts of 21% or higher erased $13,753 in profit during the analyzed period, nearly matching the company's total profit of $14,635, and a single unapproved transaction discounted 50% accounted for $3,840 of that loss on its own.

The Problem Statement

Aggregate profitability metrics can look healthy while masking specific, fixable sources of loss. This project set out to answer three questions: where is the company losing profit that it doesn't need to lose, is that loss a broad pattern or a handful of outlier transactions, and what specific, low-risk action would recover it. The goal was concrete, quantified recommendations rather than general advice like "increase sales" or "cut costs."

Methodology

Power BI Desktop: primary platform for data modeling, calculation, and dashboard delivery.

Power Query: used to reshape a single flat transaction file into a star schema (fact table plus customer, product, and location dimensions), which is faster and more reliable to analyze than one wide table.

DAX: used for profit, margin, and discount-tier calculations that don't exist in the raw data.

Skills

Power Query: data cleaning, star-schema design, composite key creation, duplicate and missing-key resolution, column type management.

DAX: calculated columns, measures, conditional logic (SWITCH), aggregation functions (DISTINCTCOUNT, DIVIDE), date/time extraction.

Power BI modeling and visualization: relationship cardinality and cross-filter configuration, matrix and bar chart design, cross-filter drill-down analysis, dashboard layout.

Analysis: root-cause investigation, outlier-versus-pattern verification, translating data findings into quantified business recommendations.

Results & Recommendations

Finding 1: Deep discounting is a direct, measurable drag on profit. Orders discounted 21% or more lost money overall, while orders with no discount were the most profitable segment in the business. This pattern held consistently across several product lines (Tables, Bookcases, Appliances, Binders), not just one, which points to a policy issue rather than a one-time event.

Recommendation: Cap discretionary discounting at 20% for the affected product lines. This alone addresses a loss of $13,753 in the period analyzed, a meaningful recovery against $14,635 in total profit, without cutting prices or margin anywhere else in the business.

Finding 2: A single unapproved transaction distorted performance reporting at multiple levels. One order, an $8,000 piece of equipment discounted 50%, lost $3,840 in profit. That one order was large enough that it initially looked like evidence of a struggling region and a weak sales day. Once isolated, it turned out to be one transaction, not a regional or weekly trend. This is a control gap, not a market problem: nothing in the current process stops a large discount like this from going through unreviewed.

Recommendation: Require manager approval for any discount above 20-30% on high-value orders. This is a low-cost operational control, not a pricing or market strategy change, and would have caught this specific transaction before it affected the bottom line.

Next Steps to Implementation

Pilot the 20% discount cap on the identified product lines for one full quarter and measure the margin change directly.

Add an approval step to the ordering process for discounts above the threshold on high-value orders.

Move this analysis from a static file to a live, refreshed dashboard so leadership can monitor discount-driven profit loss on an ongoing basis rather than discovering it after the fact.

Re-run this analysis once a full year or more of data is available to confirm these patterns hold over time and aren't seasonal.

Limitations

This project uses a public sample retail dataset for methodology demonstration, not a real company's proprietary data. The technique transfers directly; the dollar figures are illustrative of scale, not a real chain's actual financials.
The dataset does not include a direct cost field. Total Cost was derived algebraically from Sales and Profit rather than sourced from actual vendor or COGS data, a reasonable but simplifying assumption.
The dataset covers a fixed historical window, so seasonality and multi-year trend could not be tested.
