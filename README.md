# **Diamonds ANOVA Analysis**  

This project examines how diamond characteristics—specifically color grade and cut quality—influence pricing using statistical modeling in Python. The analysis explores relationships between diamond color (D, E, F, H, I), cut (Ideal, Premium, Very Good), and price through ANOVA testing. The goal is to provide data-driven insights about diamond valuation. The project leverages Python libraries including pandas, seaborn, statsmodels, and scikit-learn for data analysis, hypothesis testing, and visualization.

## **Project Overview**  

The **Diamonds ANOVA Analysis** project aims to:  

- **Analyze Price Differences by Color**: Evaluate how diamond prices vary across different color grades (D, E, F, H, I)  
- **Assess Cut Quality Impact**: Determine whether cut types (Ideal, Premium, Very Good) significantly affect pricing  
- **Examine Interaction Effects**: Investigate if color and cut combine to influence diamond prices  
- **Conduct Post Hoc Testing**: Use Tukey's HSD to identify which specific color and cut groups differ significantly  
- **Provide Valuation Insights**: Offer actionable findings about how diamond characteristics affect market prices  

## **Dataset Structure**  

The dataset is the **diamonds dataset** from the **seaborn** library, containing key attributes of diamonds along with their pricing information. The main features used in this analysis include:  

- **Carat**: The weight of the diamond in carats (continuous).  
- **Cut**: The quality of the diamond cut (**Ideal, Premium, Very Good**) (categorical predictor).  
- **Color**: The color grade of the diamond, ranging from **D (colorless) to I (tinted)** (categorical predictor).  
- **Clarity**: The clarity rating, indicating the presence of inclusions or blemishes (not included in this analysis but available in the dataset).  
- **Depth**: The total depth percentage of the diamond (continuous).  
- **Table**: The width of the top facet of the diamond relative to its width (continuous).  
- **Price**: The price of the diamond in US dollars (continuous dependent variable).  
- **X, Y, Z**: The physical dimensions of the diamond (length, width, and depth in mm) (not included in this analysis but available in the dataset).  
- **Log_Price**: The natural logarithm of the price (used for variance stabilization in ANOVA).

## **Data Processing and Analysis Steps**  

The data processing and analysis steps include:  

- **Data Cleaning**:  
  - Subset to relevant color grades (D, E, F, H, I) and cut types (Ideal, Premium, Very Good)  
  - Remove missing values and reset index  
  - Apply log transformation to price variable  
- **Exploratory Data Analysis (EDA)**:  
  - Visualize price distributions across color and cut categories using boxplots  
  - Examine mean price differences between groups  
- **Statistical Modeling**:  
  - **One-Way ANOVA**: Test price differences across color grades and cut types separately  
  - **Two-Way ANOVA**: Analyze combined effects of color and cut including interaction  
- **Post Hoc Testing**:  
  - Apply Tukey's HSD test to identify significantly different groups  
  - Examine specific color-cut interaction pairs
 
## **Key Insights**  

### **ANOVA Results**  
- **Color significantly affects price (p < 0.001)** with higher grades (F, H, I) commanding higher prices than D  
- **Cut significantly affects price (p < 0.001)** with Premium cuts priced higher than Ideal and Very Good  
- **Significant interaction between color and cut (p = 0.00045)** indicating combined effects  

### **Post Hoc Findings**  
- **Premium H-color diamonds** have significantly higher prices than:  
  - Very Good E-color (mean diff = 0.5223, p < 0.001)  
  - Very Good F-color (mean diff = 0.3493, p < 0.001)  
- **No significant difference** between D and E color grades (p = 0.1169)

## **Project Highlights**  

- Conducted **one-way and two-way ANOVA** to rigorously test price differences  
- Identified **key valuation trends**:  
  - Higher color grades (F, H, I) command premium pricing  
  - Premium cuts are valued higher than Ideal/Very Good  
  - Certain color-cut combinations (H_Premium) show significant price premiums  
- Applied **Tukey's HSD test** to pinpoint specific group differences  
- Created **clear visualizations** of price distributions across categories  

## **Future Work**  

- **Expand Predictor Variables**: Incorporate carat weight and clarity into the analysis  
- **Test Alternative Models**: Explore regression approaches with additional predictors  
- **Develop Price Prediction**: Implement machine learning models to forecast diamond prices  
- **Analyze Market Segments**: Cluster diamonds based on multiple characteristics  
- **Optimize Valuation Models**: Build tools to estimate fair market prices  

This analysis provides **data-driven insights into diamond pricing**, helping buyers, sellers, and appraisers understand how color and cut characteristics affect market value. The findings highlight the importance of considering both individual and combined effects when evaluating diamond prices.
