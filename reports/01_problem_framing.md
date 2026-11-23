# Step 1 — Problem understanding & framing

**Problem statement.** Group the tiendas de abarrotes of Mexico City and the Valley of Mexico
metropolitan area (ZMVM) into actionable micro-market segments, using store, neighbourhood and
competition data, so a wholesaler can prioritise clients, plan efficient routes, tailor assortment and
prices, and identify expansion zones — without disadvantaging merchants in poorer areas.

**Task type.** Unsupervised clustering (K-Means, Hierarchical, DBSCAN). There is no target variable in
public data (no sales or "good client" label), and the business need is discovery, not prediction.

**Target metric.** Silhouette score, supported by Davies–Bouldin, Calinski–Harabasz, stability
(Adjusted Rand Index across bootstrap samples) and a fairness check (disparate impact across
neighbourhood marginalization levels).

**Business KPIs.** Route efficiency (stores per km² in priority zones), coverage of high-potential
stores, white-space zones for expansion, assortment fit per segment, and merchant success in
low-income areas.

The full write-up lives in the project report; this file is the repo copy of the problem statement.
