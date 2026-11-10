# Data dictionary and provenance

These CSVs reproduce the **embedded values in `index.html` V24** for reference. They are **not new downloads or independently verified extracts**. Do not describe this repository as fully audited without checking against the original World Bank tables.

- `external_debt_2024.csv`: five-country aggregate external debt stocks and annual debt-service flows, in USD billions. Stock indicator `DT.DOD.DECT.CD`; service indicator `DT.TDS.DECT.CD`. `service_to_stock_pct_derived` = annual debt service / end-year debt stock × 100; **not** an interest rate or a debt-distress indicator.
- `creditor_shares_2024.csv`: named and residual creditor categories for Senegal and Samoa; percentages of **public and publicly guaranteed (PPG) external debt**, **not** all external debt or ultimate beneficial ownership.
- `creditor_group_shares_2024.csv`: published headline group percentages as encoded in V24.

**Important rounding discrepancy:** Senegal's displayed detailed creditor rows sum to 42% multilateral and 18% bilateral, while the encoded headline group shares are 41% and 19% respectively. The website's V24 values have been preserved rather than silently changed. Confirm the precise published source values before treating this breakdown as audited.

**Runtime data:** The HTML also requests five-economy PPG creditor-category observations from the World Bank API. Those live responses are **not included** in these CSVs and may change or fail to load. The dashboard currently reads its five-country values and Senegal/Samoa cases from embedded JavaScript; CSVs are archival reference files, not runtime dependencies.

Sources to check:
- World Bank International Debt Statistics: https://www.worldbank.org/en/programs/debt-statistics/ids
- World Bank Data API: https://api.worldbank.org/v2/
- World Bank International Debt Report 2025 country profiles (2024 data).

The map geometry is embedded inside the HTML; no separate map asset is needed. Poppins loads from Google Fonts and the additional World Bank API table needs an internet connection.
