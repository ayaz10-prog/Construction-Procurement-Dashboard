# Construction Procurement Dashboard: Value & Risk Analysis

**Power BI project: financial and risk analysis for a construction supply chain**

## Objective

To transform raw ERP procurement data into a dynamic business intelligence tool in Power BI, shifting the focus from simply tracking costs to actively managing value, efficiency, and supply chain risk across construction projects.

## Dataset

`Construction_Procurement_Data.xlsx` holds a sample ERP extract modeled on SAP MM procurement data:

| Sheet | Contents |
|---|---|
| `Purchase_Orders_GR` | 20 purchase orders with goods receipts across 3 projects (Burj-2025, Euro-HQ, KSA-Res), Jan–May 2025 |
| `Supplier_Master` | 8 suppliers with region, category, pre-qualification status, safety index and payment terms |
| `Material_Master` | 7 materials with material group, project cost code, unit of measure and standard price |
| `Contracts_RFQ` | MAS and RFQ contracts with negotiated rates, end dates and order limits |

Total spend in the dataset: **$1,008,500**.

## Key Technical Skills Demonstrated

- **Data Modeling:** Cleaned, linked, and integrated four separate data sources (Purchase_Orders_GR, Supplier_Master, Material_Master, Contracts_RFQ) using One-to-Many relationships.
- **DAX & Analysis:** Developed three custom procurement KPIs: **TotalSpend**, **OTDPercent** (On-Time Delivery rate) and **TotalPPV** (Purchase Price Variance) to measure financial performance against contractual standards.
- **Data Integrity:** Solved external data integration challenges and internal Power BI naming conflicts (e.g., using SUMX for TotalSpend) to ensure a single, reliable source of truth.

## Actionable Insights & Value Delivered

### 1. Cost Control (PPV)

The **Cost Management & Value** page tracks Purchase Price Variance against each material's standard price. It reveals a net **−$12,000 cost overrun** (Total PPV). The overrun is driven mainly by **Dry Material** (cement bags at $5.50–$5.80 against a $5.00 standard, −$10,800), followed by **Subcontractor** services (−$4,000). Structural Steel, by contrast, came in **$2,000 under** standard thanks to the negotiated MAS rate, showing the value of contract coverage.

### 2. Supplier Risk & Efficiency

The vendor scorecard on the **Supplier Reliability & Risk** page ranks suppliers by performance. Overall on-time delivery is **60%**. It identifies **Al-Nujum Aggregates** as the highest risk: only **25% OTD** across 4 orders, 2 quality rejections, a "Pending" pre-qualification status and the lowest safety index (2/5). It is also the supplier behind most of the PPV overrun, which makes it the clearest candidate for mitigation or replacement.

### 3. Strategic Insight

The geographic spend distribution shows **64%** of total spend concentrated in the **Middle East (KSA 41%, UAE 23%)**. This indicates a dependency risk and suggests diversifying the supplier base toward **Europe** (currently 36% across the UK, Germany and Italy) to strengthen supply chain resilience.

## Dashboard Preview

<img width="1008" height="583" alt="Cost Management & Value page" src="https://github.com/user-attachments/assets/49ed61b6-d68d-49e2-a6b5-2054bdb231df" />
<img width="1028" height="603" alt="Supplier Reliability & Risk page" src="https://github.com/user-attachments/assets/d4069db4-4dea-446e-b165-f692da205280" />

## Files

- `Construction_Procurement_Dashboard.pbix` — the Power BI report and data model (open in Power BI Desktop)
- `Construction_Procurement_Data.xlsx` — the source data
