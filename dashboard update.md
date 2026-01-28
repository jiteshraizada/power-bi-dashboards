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
