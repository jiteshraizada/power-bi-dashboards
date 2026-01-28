# BFSI Data Analytics Portfolio

## Daily Progress
| Date | Task | Status | GitHub Commit |
|------|------|--------|---------------|
| 2026-01-27 | WiseOwl DAX Videos 1-2 | ✅ Complete | [feat: KPI slicer] |

## DAX Learning Journey
**Video 2 - Disconnected KPI Slicer**

**KPI_Slicer Table:**
| KPI |
|-----|
| Total Sales |
| Avg Order Value |
| Delivered Orders |

**Dynamic KPI Measure:**
```dax
VAR SelectedKPI = SELECTEDVALUE(KPI_Slicer[KPI], "Total Sales")
VAR DeliveredAmount = [Delivered Sales]
RETURN SWITCH(SelectedKPI,
    "Total Sales", DeliveredAmount,
    "Avg Order Value", AVERAGE(Sales[Amount]),
    "Delivered Orders", CALCULATE(COUNTROWS(Sales), DeliveredAmount > 0),
    DeliveredAmount
)

## Daily Progress
| Date | Task | Status | Commit |
|------|------|--------|--------|
| 2026-01-27 | WiseOwl DAX Videos 1-2 | ✅ | KPI slicer |
| 2026-01-28 | Day 3 Production Updates | ✅ | [Page 3 Combo Chart] |
<img width="1188" height="650" alt="Profit and Delivered Sales By Brand" src="https://github.com/user-attachments/assets/d8ed12ee-e8b9-4944-900c-fa9ca0478d75" />

## Page 3: Updated Sales Dashboard
**Combo Chart**: Profit bars vs Delivered Sales line (by Brand)
- Top profit contributor auto-colored
- Negative profit risk detection  
- Dual-axis executive summary style
