# 🎮 Web Game User Funnel and Retention Analysis

This project analyzes **user engagement, funnel progression, and retention** in a simulated web game dataset. It also includes a **simulated A/B test** to explore the potential impact of a feature change on user session duration.  

---

## 📊 Project Overview
- **Engagement Analysis** → Distribution of key events (`game_start`, `level_complete`, `ad_view`) per user.  
- **Funnel Analysis** → Conversion from game start → level completion.  
- **Retention Analysis** → Daily Active Users (DAU), with attempt to compute D7 & D30 retention.  
- **A/B Testing Simulation** → Randomly split users into control/experiment groups to compare average session duration.  

---

## 📂 Dataset
- **Type**: Simulated event logs  
- **Events captured**:  
  - `game_start`  
  - `level_complete`  
  - `ad_view`  
- **Users**: 100 (simulated)  
- **Period**: 1 day (2023-01-01)  

⚠️ Since the dataset spans only one day, long-term retention metrics (D7/D30) cannot be computed.  

---

## 🛠️ Analysis Workflow
1. Data exploration and cleaning  
2. User engagement analysis  
3. Funnel conversion analysis  
4. Retention analysis (DAU, D7, D30)  
5. A/B test simulation (session duration)  
6. Visualization and reporting  

---

## 📈 Key Results

### 🔹 Engagement
| Event Type       | Mean per User | Std Dev | Min | Max |
|------------------|---------------|---------|-----|-----|
| **ad_view**      | 4.05          | 1.82    | 0   | 12  |
| **game_start**   | 8.13          | 2.35    | 3   | 14  |
| **level_complete** | 7.82        | 2.41    | 2   | 14  |

---

### 🔹 Funnel
- Users who started a game: **100**  
- Users who completed a level: **100**  
- Conversion Rate: **100%**  

➡️ Smooth onboarding: all users completed at least one level.  

---

### 🔹 Retention
- **DAU (2023-01-01)**: 100 users  
- **D7/D30 retention**: *Not measurable (dataset = 1 day)*  

---

### 🔹 A/B Test (Session Duration)
| Group       | Avg Duration |
|-------------|--------------|
| Control     | ~48 min 58s  |
| Experiment  | ~47 min 38s  |

⚠️ Small difference, not statistically tested. Larger dataset needed.  

---

## ✅ Conclusion & Next Steps
- Strong early engagement and conversion.  
- Retention analysis limited by dataset length.  
- A/B test shows minor differences → requires hypothesis testing.  

**Future improvements:**  
- Collect 30+ days of user activity.  
- Perform statistical significance testing.  
- Expand funnel to multiple levels/milestones.  
- Add churn, LTV, and monetization analysis.  

---

## 🚀 How to Run
```bash
# Clone repository
git clone https://github.com/Lifewitdata/game-funnel-analysis.git
cd game-funnel-analysis

# Install dependencies
pip install -r requirements.txt

# Run analysis
jupyter notebook analysis.ipynb
