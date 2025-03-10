# **COVID-19 Mortality Analysis: Impact of Comorbidities and Healthcare System Capacity**  

## **Project Overview**  
This project analyzes the factors influencing COVID-19 mortality, focusing on **age, comorbidities, and healthcare system conditions**. Using a dataset from Mexico, I examine how **pre-existing health conditions (e.g., hypertension, diabetes, chronic kidney disease)** and hospital resource availability impact patient outcomes.  

The dataset includes **demographic and health-related factors**, such as age, gender, smoking status, chronic diseases, ICU admission, and intubation status. I applied **statistical analysis and data visualization** using Python libraries (**Pandas, Seaborn, Matplotlib, SciPy**) to uncover meaningful patterns in COVID-19 mortality.  

## **Data Source**  
- **Dataset:** [COVID-19 Mexico Patient Health Dataset (Kaggle)](https://www.kaggle.com/datasets/riteshahlawat/covid19-mexico-patient-health-dataset)  
- **Origin:** Mexican government health records  

## **Objectives**  
1. **Data Preprocessing:**  
   - Removed duplicates and handled incorrect values  
   - Renamed columns for clarity  
   - Filtered out patients who tested negative for COVID-19  
2. **Statistical Analysis of Mortality Factors:**  
   - **Age & mortality correlation:** Point-biserial correlation  
   - **Comorbidities, gender, and smoking status:** Chi-square test & Cramér’s V  
   - **Comorbidities co-occurrence impact:** Tetrachoric correlation  
3. **Visualization & Insights:**  
   - Bar plots, boxplots, and histograms for mortality distribution  
   - Heatmaps to analyze comorbidity relationships  

## **Methodology**  
### **1. Data Cleaning & Preprocessing**  
- **Handling Invalid Values:** Replaced incorrect values (e.g., 97, 98, 99) with NaN.  
- **Column Transformations:**  
  - Mapped categorical variables (e.g., SEX: 1 → Male, 2 → Female)  
  - Converted mortality status into binary (0 = Alive, 1 = Dead)  
- **Filtering Criteria:** Removed patients with **negative COVID-19 test results** to ensure data relevance.  

### **2. Exploratory Data Analysis (EDA)**  
- **Age Analysis:**  
  - Computed **point-biserial correlation (R = 0.33, p < 0.001)** to measure the association between **age and mortality**.  
  - Older patients showed a higher mortality risk, though correlation strength was **moderate**.  
- **Comorbidities & Mortality:**  
  - **Chi-square test** confirmed significant relationships between mortality and **comorbidities (e.g., diabetes, hypertension, chronic kidney disease)**.  
  - **Cramér’s V** was used to measure the strength of these associations. While many conditions showed **statistically significant p-values**, their effect sizes were **weak to moderate**, emphasizing the importance of effect size over raw significance.  
- **Comorbidity Co-occurrence:**  
  - **Tetrachoric correlation** revealed that **having multiple comorbidities increases mortality risk beyond the sum of individual risks**, particularly in younger patients (30-44).  
  - No significant correlation was observed in **patients above 60**, suggesting **other factors dominated mortality risk** in this group.  

### **3. Hospital Resource Impact on Mortality Patterns**  
- **In hospitals with a 30% mortality rate:**  
  - Comorbidities had a **stronger correlation** with mortality.  
  - Suggests that **patients had better access to medical care**, allowing pre-existing conditions to be a clearer predictor of outcomes.  
- **In hospitals with a 50% mortality rate:**  
  - Correlations between comorbidities and mortality were **weaker**, implying that factors like **resource availability** played a bigger role.  
- **In hospitals with an 80% mortality rate:**  
  - **No correlation** was found between comorbidities and mortality, even when conditions co-occurred.  
  - Suggests **resource shortages and overwhelmed medical staff** were the primary mortality drivers rather than patient health factors.  

---

## **Key Findings & Insights**  

### **1. Age & Mortality**  
- **Older individuals had a higher mortality risk (R = 0.33, moderate correlation).**  
- However, other factors (e.g., hospital resources, disease severity) also played a role in determining outcomes.  

### **2. Comorbidities & Mortality (Varying by Age Group)**  
- **Young patients (30-44):** Having multiple comorbidities (e.g., diabetes + CKD) had a **synergistic effect**, increasing mortality risk beyond the sum of individual conditions.  
- **Middle-aged patients (45-60):** Weaker correlation, suggesting additional health or treatment factors influenced outcomes.  
- **Elderly patients (60+):** No significant correlation, likely due to high baseline mortality rates regardless of health status. Some patients may have **died before reaching the hospital**, leading to **survival bias** in the dataset.  

### **3. Hospital Overcrowding & Mortality**  
- In well-resourced hospitals, **comorbidities were clear risk factors** for mortality.  
- In overwhelmed hospitals (80% mortality rate), **comorbidities did not influence outcomes**, likely due to **resource scarcity** and the inability to provide adequate care.  

---

## **Implications & Real-World Applications**  

### **Healthcare & Research**  
- **Comorbidity effects depend on hospital capacity.** Public health strategies should **prioritize resource allocation** to hospitals experiencing extreme patient overload.  
- **Age should be considered alongside hospital conditions.** Younger patients with comorbidities may require **earlier interventions** due to compounded risks.  

### **Public Health & Policy**  
- **Healthcare systems in overwhelmed hospitals need better crisis planning.** Mortality risk is not just about comorbidities—**resource shortages play a critical role**.  
- **Comorbidities alone do not dictate mortality risk.** Policymakers should avoid **one-size-fits-all** approaches and instead **consider hospital conditions when allocating resources.**  

---

## **Tools & Libraries Used**  
- **Data Handling:** Pandas, NumPy  
- **Statistical Analysis:** SciPy, chi-square test, point-biserial correlation, tetrachoric correlation  
- **Visualization:** Seaborn, Matplotlib  

---

## **Collaboration & Additional Resources**  
This project was conducted in collaboration with Bartłomiej Brzostek [@bartbrzost](https://github.com/bartbrzost), Katarzyna Donaj [@donajkatarzyna](https://github.com/donajkatarzyna) and Tomasz Mazur [@Tom-Mazur](https://github.com/Tom-Mazur), who worked on different aspects of the analysis. However, **all files and analyses presented in this repository were solely created by me**.

The full project, including additional insights and discussions from the team, can be explored in our **Prezi presentation**: [Prezi Link](https://prezi.com/view/TObuunzj42D090Gz6ovn/)

---

## **Conclusion**  
This analysis provides key insights into **COVID-19 mortality risk factors**, emphasizing that **hospital conditions, rather than comorbidities alone, play a major role in survival outcomes**.  

While comorbidities **increase mortality risk**, their impact is **highly dependent on hospital resource availability**. **Overwhelmed medical units experience high mortality regardless of patient health status**, suggesting that **effective crisis management and resource distribution** are crucial for reducing pandemic deaths.  

---

