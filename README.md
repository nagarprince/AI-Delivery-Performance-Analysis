# AI-Based Delivery Performance Analysis & Delay Prediction

Predicts which shipments will be delayed and shows delivery performance in an interactive Power BI dashboard, using 25,000+ delivery records.

**Tools:** Python, Pandas, NumPy, Scikit-learn, XGBoost, Power BI (DAX, Power Query), Jupyter Notebook

---

## Business Problem

Late deliveries increase cost and hurt customer satisfaction. This project answers three questions:

1. What share of deliveries are delayed, and where do the delays happen?
2. Which factors (weather, delivery mode, partner, region, distance, weight) drive delays?
3. Can we predict a delay before it happens so operations can act early?

## Dataset

- **Records:** 25,000+ deliveries
- **Source:** [add source here, e.g. Kaggle link or "synthetic dataset created for practice"]
- **Columns:** Delivery ID, Region, Delivery Mode, Delivery Partner, Weather Condition, Package Weight (KG), Distance (KM), Delivery Cost, Delay Severity, Delivery Status

## Approach

1. **Data cleaning:** handled missing values, duplicates and data types
2. **Exploratory analysis:** delay rate by weather, mode, partner and region
3. **Feature engineering and preprocessing:** encoded categorical columns, scaled numeric columns
4. **Model training:** trained and compared three classification models
5. **Evaluation:** compared accuracy, precision, recall, F1 score and ROC AUC
6. **Dashboard:** built a Power BI report to monitor delivery KPIs

## Model Results

| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---|---|---|---|---|---|
| Random Forest | **0.8960** | 0.7975 | **0.8178** | **0.8076** | 0.9653 |
| Logistic Regression | 0.8936 | 0.7949 | 0.8103 | 0.8025 | **0.9672** |
| XGBoost | 0.8916 | 0.7861 | 0.8156 | 0.8006 | 0.9646 |

**Conclusion:** Random Forest gave the best accuracy, recall and F1 score, so it is the preferred model. Recall matters most here because a missed delay (false negative) is more costly than a false alarm. Logistic Regression performed almost as well and is easier to explain.

## Key Business Insights

- About **21%** of deliveries are delayed; the on-time rate is about **79%**.
- **Stormy weather** causes the highest number of delays.
- **Express** delivery has higher average delays than other modes.
- Some delivery partners have a much higher delay rate than others.
- Regional analysis shows where the operational bottlenecks are.

## Recommendations

- Add buffer time or reassign shipments in stormy weather.
- Review the Express service and the high-delay delivery partners.
- Use the model to flag high-risk shipments before dispatch.

## Power BI Dashboard

**KPIs:** Total Deliveries, Delayed Deliveries, Delay %, Average Delivery Time, On-Time Delivery Rate

**Visuals:** Weather impact, delivery mode performance, delay severity, delays by region, partner performance, delivery status

**Filters:** Region, Delivery Mode, Partner, Weather, Delay Severity, Reset button

### Screenshots

![Dashboard overview](images/dashboard_overview.png)
## Repository Files

AI-Delivery-Performance-Analysis/
├── project.ipynb        # data cleaning, EDA, model training and evaluation
├── Delivery_Dash.pbix   # Power BI dashboard
├── Analysis.txt         # analysis notes
├── Report.pdf           # project report
├── pp.pdf               # presentation
└── images/              # dashboard screenshots

## How to Run

1. Open `project.ipynb` in Jupyter Notebook and run all cells.
2. Open `Delivery_Dash.pbix` in Power BI Desktop to explore the dashboard.

## Future Improvements

- Real-time delay alerts
- Route optimization recommendations
- Cloud database integration

---

**Author:** Prince Nagar | [LinkedIn](https://www.linkedin.com/in/prince-nagar-dev/) | [GitHub](https://github.com/nagarprince)
