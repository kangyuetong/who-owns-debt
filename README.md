# Who owns the world’s debt?

An interactive financial research dashboard exploring external debt stocks, annual debt-service flows, country comparisons, and selected reported creditor relationships. Built as a static website for GitHub Pages.

**[Explore the interactive Debt Atlas](https://kangyuetong.github.io/REPOSITORY-NAME/)**

> **Before publishing:** Replace `REPOSITORY-NAME` in the link above with the exact name of your GitHub repository. If you publish from a custom domain or a different Pages configuration, replace the entire URL with your actual live site link.

## What you can explore

The dashboard compares Indonesia, India, Brazil, Mexico and South Africa using 2024 World Bank-attributed aggregate external debt statistics. Its interactive map and debt-profile similarity network support cross-country exploration. Separate creditor diagrams and comparisons examine Senegal and Samoa's reported 2024 public and publicly guaranteed external debt by creditor and creditor group. A refinancing sensitivity tool illustrates hypothetical changes in annual interest expense.

**Important distinction:** The similarity network does not represent actual creditor-to-borrower loans. Named creditor data cover only Senegal and Samoa; the project does not identify the ultimate beneficial owners of all global debt.

## Repository structure

```text
.
├── index.html
├── README.md
└── data/
    ├── README.md
    ├── external_debt_2024.csv
    ├── creditor_shares_2024.csv
    └── creditor_group_shares_2024.csv
```

`index.html` is self-contained for its core visuals and embedded data. The CSV files are included for transparency and future reference; **the current site does not read them**. The page loads Poppins from Google Fonts and optionally retrieves additional creditor-category observations from the World Bank API.

## Sources and limitations

The figures were carried over from the previous V24 HTML and attributed there to [World Bank International Debt Statistics](https://www.worldbank.org/en/programs/debt-statistics/ids) and the World Bank *International Debt Report 2025* country profiles. They have **not been independently revalidated during repository packaging**. See [data documentation](data/README.md) for indicators, definitions, limitations and a Senegal rounding discrepancy that should be checked before academic or professional citation. World Bank series may be revised.

## Publish with GitHub Pages

1. Upload `index.html`, `README.md`, and the complete `data` folder to the repository root.
2. Open **Settings → Pages** in GitHub.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. When GitHub provides your site URL, update the **Explore the interactive Debt Atlas** link at the top of this README.

No installation, build process, Python server, or backend is required.
