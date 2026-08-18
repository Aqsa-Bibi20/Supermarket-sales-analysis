Exploratory Data Analysis of Retail Transaction Dynamics and Consumer Behavior in Supermarket Chains
Abstract
This paper investigates transactional patterns, customer demographic segmentation, payment method distributions, and revenue-generating drivers across multi-branch supermarket retail operations. Using exploratory data analysis (EDA), feature engineering on temporal variables, and bivariate categorical distributions, we evaluate sales performance and customer satisfaction. The findings reveal critical peak operational hours, category preferences stratified by gender, and distinct branch-level gross margin contributions, providing actionable data-driven strategies for inventory management, workforce scheduling, and branch-specific service optimization.
1. Introduction
Modern retail enterprises generate high-velocity transaction data containing vital signals regarding buyer psychology and operational efficiency. The primary objective of this empirical study is to process raw point-of-sale (POS) records to uncover:
	Category-level revenue drivers and profitability variance.
	Temporal shopping distributions to identify operational bottlenecks.
	Consumer payment channel adoption.
	Gender-based product preferences and branch customer satisfaction scores.
2. Methodology & Data Preprocessing
2.1 Dataset Ingestion and Structural Audit
The dataset comprises point-of-sale transaction logs capturing invoice IDs, branch identifiers, product classifications, unit costs, purchase volumes, tax assessments, payment instruments, temporal stamps, cost of goods sold (COGS), gross margins, and customer satisfaction ratings.
Total Ingested Dimensions: n rows × 17 features
Missing Values: Null count = 0 across all attributes
Duplicate Entries: Deduplicated (Unique invoice instances verified)
2.2 Feature Engineering
Temporal strings were standardized into machine-readable datetime structures. Two derivative variables were generated:
	Hour (H_i): Extracted from time string 〖"Time" 〗_i→H_i∈[0,23]to isolate hourly demand surges.
	Month (M_i): Derived from date parameters for periodic longitudinal grouping.
"Gross Income"="Total Revenue"-"COGS" 
3. Empirical Results & Findings
3.1 Revenue Generation by Product Vertical
Aggregated gross billings across product classifications demonstrate variable performance:
	High-volume contributors: Sports and Travel, Home and Lifestyle, and Health and Beauty.
	Medium-to-stable demand: Electronic Accessories and Fashion Accessories.
	Inventory optimization models must prioritize reorder frequency in top-tier categories to avoid stockout friction.
3.2 Temporal Distribution & Peak Shopping Hours
Aggregating revenue by the derived feature H_ireveals a bimodal traffic curve:
	Morning Surge: 10:00 AM – 11:00 AM.
	Afternoon Surge: 1:00 PM – 2:00 PM.
	Evening Taper: Gradual stabilization with consistent basket sizes toward 8:00 PM.
3.3 Transactional Settlement Channels
Analysis of settlement mechanisms indicates an equitable tripartite distribution among consumers:
	E-wallets: ~33.3% adoption, reflecting growing digital wallet penetration.
	Cash & Credit Cards: Account for the remaining volume in nearly equal proportions, emphasizing the requirement for persistent multi-channel point-of-sale infrastructure.
3.4 Demographic Segmentation & Branch Satisfaction
	Gender Preferences: Distinct clustering was observed where specific lines (e.g., Fashion Accessories vs. Electronic Accessories) displayed demographic skews, providing a baseline for targeted programmatic promotions.
	Branch Ratings: Branch C and Branch A maintained competitive customer satisfaction scores (>7.0/10.0), with gross income contributions aligning directly with transaction volume per location.
4. Strategic Recommendations
	Workforce Scheduling: Align cashier desks and floor staff allocations to the identified peak hours (10:00–11:00 AM and 1:00–2:00 PM) to reduce wait times and checkout abandonment.
	Targeted Merchandising: Tailor digital and in-store promotional campaigns around demographic product preferences identified in the categorical cross-tabulations.
	Operational Continuity: Maintain high-speed digital POS terminals given that electronic and card-based settlements constitute the majority of transactional throughput.
5. Conclusion
Through structured data preprocessing and systematic visualization, this study successfully converted granular retail records into high-level business intelligence. Future extensions of this work may incorporate predictive machine learning models, such as time-series demand forecasting and customer lifetime value (CLV) regression models.

