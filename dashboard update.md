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
# Day 3 Git Push (9PM)
git add .
git commit -m "feat: **Day 3** production dashboard complete

**Page 3 Updated Sales:**
- 🔄 Dynamic KPI slicer (Page 2)
- 💰 Real Profit calc (UnitPrice×Qty-Shipping, delivered filter)
- 📊 Brand combo chart w/ top performer highlight
- Active products filtered delivered orders > 0"

git push origin main
