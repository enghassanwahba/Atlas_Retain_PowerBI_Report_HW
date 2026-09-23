   📊 HR Analytics & Employee Attrition Enterprise Power BI Readme File

📊 Overview
An enterprise-grade, high-precision data analytics solution designed, engineered, and fully developed utilizing **Power BI Desktop** for (Atlas_Lab_Retain Analytics & Insights). This dynamic application provides proactive, multi-dimensional exploratory intelligence on workforce health, attrition anomalies, and turnover risk factors (`Employee Attrition`), equipping executive stakeholders with data-driven strategic retention insights to safeguard human capital and replace arbitrary business forecasting.
---
<img width="1347" height="590" alt="Overview" src="https://github.com/user-attachments/assets/a7d82662-a375-4446-8c52-347bbc6a3a6f" />
---
 📐 The Main Layout for All Project
Unified Left Sidebar Master Panel Anatomy
The overall operational interface relies on a strict **General Layout Form** featuring a persistent **Fixed Left Sidebar Navigation & Filter Control Panel (on the left side)** that remains uniform across all four analytical canvases. This workspace layout acts as an isolated, standalone operational control cockpit structured vertically into four dedicated quadrants from top to bottom:
---
<img width="1231" height="547" alt="The Main Layout" src="https://github.com/user-attachments/assets/21dc4610-8018-4bb1-97df-0dcb89c8f675" />
----
 1️⃣ Quadrant I 
Header Node & Corporate Identity* **Embedded Asset:** The official operational emblem configured and registered via internal workspace descriptors under the name (`attrition-icon-trendy-design`).* **UI/UX Visual Purpose:** Acts as the primary application brand anchor and corporate logo. Positioned at the apex of the left panel to instantly establish an authoritative visual baseline, verifying that all cross-filtered variables and adjacent visual metrics are entirely dedicated to evaluating **Workforce Turnover Risk & Employee Attrition** with zero outside distortion.

 2️⃣ Quadrant II
 Dynamic Sheet-less Page Navigation System* **Embedded Asset:** A matrix row consisting of **4 custom interactive navigation nodes** programmatically hardcoded to completely override and hide native Power BI sheet tab arrays.
* **UI/UX Interactivity Engine:** Every selector node is linked via workspace triggers to the exact page sequences ordered sequentially as follows: (`Overview` ➡️ `Demographics` ------------------> `Performance Tracker` ➡️ `Attrition`). This engine employs conditional visual states (`Active State Configuration`), illuminating the active sheet marker in a sharp **Neon Lime Hue** while damping non-active keys into a muted Charcoal profile to reduce visual distraction.

 3️⃣ Quadrant III
Integrated Global Filter Grid (Slicers Panel)* **Embedded Asset:** A dedicated vertical slicer stack housed under the (Filter) node that channels logical expressions and triggers cross-filtering queries across right-hand analytical charts instantly. It contains the following calibrated parameters:
  * **Temporal Filter (`Year Slicer`):** Filters the reporting layer across specific fiscal years to track turnover velocity and volumetric trends across time.
  * **Organizational Filter (`Department Slicer`):** Restricts data queries to map explicit corporate divisions (e.g., `Sales`, `Technology`, `Human Resources`).
  * **Demographic Filter (`Gender Slicer`):** Splits transactional employee records by gender classifications (`Male`, `Female`, `Non-Binary`) to perform gender-balanced retention audits.

 4️⃣ Quadrant IV
Master Operations Reset Node (Clear Filters)* **Embedded Asset:** The operational clear filter macro icon colored in a crisp Orange and White theme, registered inside layout resource folders as `234-2349519_clear-filter-icon`.
* **Programmatic Architecture:** Placed at the base of the panel as a final control node. It is mapped to a macro command (`Bookmark Action`) that instantly purges all selected criteria inside the Quadrant III filter stack and forces right-hand reporting canvases to refresh back to their baseline un-filtered raw states within milliseconds.

--- 📊 Dataset Scale, Volumetric Metrics & Scope
The reporting application is powered by an extensive, high-fidelity relational corporate database detailing the longitudinal professional lifecycles of workforce cohorts across separate tables:
* **The Employee Registry Dimension (`DimEmployee`):** Contains the complete demographic, baseline financial, and contractual operational records of **1,470 distinct employee profiles**, mapping 23 unique data attributes per row (including Age, Department, Salary, Job Role, and Hire Date).
* **The Longitudinal Performance & Morale Ledger (`PerformanceRating`):** A high-density transactional ledger compiling **thousands of recurring yearly performance reviews** (Longitudinal Panel Records) that capture fluctuations in workspace satisfaction, morale scores, and output quality from 2012 to 2022.

--- 🏗️ Data Architecture & Relational Schema Modeling
The back-end relational architecture is engineered around a clean **Snow Schema** blueprint to maximize query processing speeds, ensure instantaneous cross-filtering responses, and protect the calculation boundaries of advanced DAX measures:
---
<img width="1160" height="742" alt="Snow Schema" src="https://github.com/user-attachments/assets/dde3d107-0ab7-4abd-985c-332f57599c7a" />
----
[DimEducation] [RatingLevel] [SatisfiedLevel]
(EducationLevel) (RatingLevel) (SatisfactionLevel)
| | |
| (1:N) | (1:N) | (1:N)
v v v
[DimEmployee] -------------> [PerformanceRating] <------------+
(Fact/Dim) (1:N) (Fact Table)
^ ^
| (1:N) | (1:N)
+------------ [DimDate] -----+
(Calendar)


---  🧠 Architectural Breakdown of Schema Relationships
1. **The Core Central Fact Table (`PerformanceRating`):** Tracks seasonal employee review transactions. It functions as the absolute star center of the data model schema where metrics for job satisfaction, manager feedback, and peer interactions are computed (e.g., `JobSatisfaction`, `ManagerRating`, `SelfRating`). It connects to surrounding boundary dimension tables via optimized one-to-many (`1:N`) keys.
2. **The Hybrid Employee Dimension (`DimEmployee`):** Engineered with a dual structural persona; it acts as a dimension table supplying employee properties to the central rating table using `EmployeeID` across a `1:N` relationship, and simultaneously functions as a fact logging terminal for exit events filtered explicitly via the binary attribute (`Attrition: YES / NO`).
3. **The Automated Calendar Dimension (`DimDate`):** A time-intelligence table generated via DAX scripting based on the historical hire boundaries of the workforce. It maps calendar dates to fiscal periods (`Years`, `Quarters`, `Months`, `Days`) and connects directly to date keys inside the operational logs to secure clean time-series intelligence.
4. **The Structural Reference Lookup Dimensions:**
   * **`DimEducation`:** Direct lookup file mapping academic achievements from Index 1 to 5 (Bachelors, Masters, Doctorate, etc.) via the `EducationLevelID` bridge key.
   * **`RatingLevel`:** Normalizes operational scale keys to evaluate year-over-year corporate output performance.
   * **`SatisfiedLevel`:** Normalizes indices tracking workspace morale from Index 1 to 5 (Very Dissatisfied up to Very Satisfied) via `SatisfactionID`.

---

--- 📂 Deep-Dive Reporting Architecture (The 4 Dashboards)

The application structures analytical workflows across 4 dedicated, data-dense right-hand presentation canvases arranged in the following verified order:

--- 1️⃣ Presentation Canvas I: Executive Overview (Overview)
---
<img width="1347" height="590" alt="Overview" src="https://github.com/user-attachments/assets/3ac0464c-32b6-4f47-9d61-f0f56407cd0d" />
---
* **Analytical Mandate:** Functions as the primary landing canvas and executive summary page, providing c-suite stakeholders with macro headcount metrics, current active operational capacity, and systemic attrition rates.
* **Reporting Components & Visual Framework:**
  * **Macro KPI Card Cluster:** An explicit multi-row visualization aggregating total operational headcount figures computed from the `Total Employee` metric, active workers on payroll from `Active Employee`, cumulative departed personnel from `InActive Employee`, and the aggregate historical attrition velocity via `Attrition Rate`.
  * **Total Employee Hiring Trend Chart:** A Stacked Column Chart plotting structural years (2012 to 2022) on the horizontal X-axis against absolute headcount totals on the vertical Y-axis. Columns are segmented internally using the `Attrition` state (**No / Yes**) to isolate historical exit waves in Green against retained personnel in a darker contrast wash.
  * **Active Employee Partition Tree (Decomposition Tree):** A tree visual mapping the granular distribution of active organizational headcount (`1233`). It fractures the parent total down by business units (`Technology`, `Sales`, `Human Resources`) and lets users slice further into specific job roles (e.g., Software Engineer, Data Scientist) to monitor resource allocation density.

--- 2️⃣ Presentation Canvas II: Demographics (Demographics)
---
<img width="1346" height="595" alt="Demographics" src="https://github.com/user-attachments/assets/74e35c60-ddab-49da-993a-99551c92c5ab" />
---
* **Analytical Mandate:** Explores structural workforce diversity and personal background factors, correlating attributes like age buckets, ethnicity groupings, and marital status parameters against the general payroll register.
* **Reporting Components & Visual Framework:**
  * **Boundary Age KPI Monitors:** Mapped digital counters detailing age milestones across active staff registers; tracking the organization's youngest asset (`Youngest Employee: 18`) against its senior resource (`Oldest Employee: 51`).
  * **Total Employee Diversity Tree (Gender - Age Bins):** A Decomposition Tree charting the complete employee population base (`1470`) across documented gender identities (Female: 675, Male: 651, Non-Binary: 124, Prefer Not To Say: 20) and drilling into localized age buckets (20-29, 30-39, 40-49, <20).
  * **Marital Status Donut Matrix:** A Donut Chart calculating population percentages by marital status tiers: Married (`Married: 624 - 42%`), Single (`Single: 549 - 37%`), and Divorced (`Divorced: 297 - 20%`).
  * **Total Employee & Wage Equity Grid (Total Employee and Average of Salary by Ethnicity):** A Line and Clustered Column Chart tracking workforce ethnicity along the X-axis. Column bars represent absolute headcount density per background category (led by White cohorts at 860 staff), while a high-contrast Neon Lime trend line charts the *Average of Salary* to verify equity in compensation across diverse demographic groups.

---3️⃣ Presentation Canvas III: Performance Tracker (Performance Tracker)
---
<img width="1353" height="597" alt="Performance Tracker" src="https://github.com/user-attachments/assets/6a2272ac-7f0f-4f17-b500-6d7ef8545d47" />
---
* **Analytical Mandate:** Acts as an individual employee profile auditing workspace. It allows HR business partners to call up an individual staff record and inspect satisfaction trends, behavioral changes, and assessment metrics over time.
* **Reporting Components & Visual Framework:**
  * **Individual Profile Selector Slicer (`select Employee Slicer`):** A top-anchored dropdown list allowing immediate selection of an individual staff record to overwrite the canvas data layer (pre-set in the report to employee: `Adan Fradgley`).
  * **Employee Milestone Date Monitors:** Three Orange card monitors reporting individual corporate historical timelines calculated by DAX measures: `Start Date`, `Last Review Date`, and the targeted automated `Next Review` date.
  * **The Core Workspace Satisfaction Quadrant (Satisfaction Trends):** Four independent Line Charts mapping yearly sentiment scores from 2015 to 2021 across four vital workplace metrics: *Job Satisfaction*, *Work-Life Balance*, *Relationship Satisfaction*, and *Environment Satisfaction*.
  * **The Performance Alignment Graph (Rating Trends):** Dual-line graphs plotting historical evaluations from 2015 to 2021 to compare *Manager Rating* scores against the employee's *Self Rating* entries, flag mismatch gaps, and protect employee engagement.
  * **Score Definition Legends:** Side-docked lookup maps indexing score fields from 1 to 5 to clearly define qualitative metrics for review ratings and workplace comfort scales.

--- 4️⃣ Presentation Canvas IV: Attrition Analytics (Attrition)
---
<img width="1349" height="598" alt="Attrition" src="https://github.com/user-attachments/assets/0f5c6a26-ef1d-415c-a430-d89cc47e2df4" />
---
* **Analytical Mandate:** A specialized investigative interface dedicated to studying the exited employee profile dataset (`237 InActive Records`). It isolates correlation models across distance barriers, structural roles, and compensation gaps to eliminate turnover.
* **Reporting Components & Visual Framework:**
  * **Exited Workforce Partition Tree (InActive Employee By Department & Job Role):** A Decomposition Tree that breaks down the complete departed staff volume (`237`) into business divisions (Technology: 133, Sales: 92, Human Resources: 12) and highlights high-turnover roles like Data Scientist and Software Engineer.
  * **InActive Employee Age Bracket Split:** A Donut Chart illustrating exit vulnerabilities by age group. It proves that younger talent tiers aged 20-29 represent the highest turnover bracket with `183 exit cases (77%)`, followed by the 30-39 group at `27 cases (11%)`.
  * **Geographic Attrition Rate Map (Attrition Rate By State):** A geographic visual connected to *Microsoft Maps* that renders regional exit events across domestic boundaries (focusing on CA, IL, NY clusters), scaling bubble vectors to match local turnover volume and active headcounts.
  * **Commute Friction Column Grid (InActive Employee by DistanceFromHome KM bins):** A Column Chart plotting binned travel distances in kilometers on the horizontal axis against exit cases on the vertical axis to measure the direct toll of long commutes on voluntary resignations.
  * **Income-Tenure Longevity Scatter Map (Income vs Attrition):** A Scatter Plot displaying *Monthly Income* distributions along the horizontal axis against *Years at Company* values along the vertical axis, color-coding markers by exit status to evaluate the relationship between wage structures and early employee turnover.
  * **Master Operational Ledger Table & Local Slicers:** A detail ledger logging records (ID, Role, Salary, Performance Score, Division) paired with specialized slice controls (Education Field, Contract Type) to allow quick cross-filtering.

---

---💻 Full Core Programmatic Code Repository: DAX Measures (`_Measure`)

The calculations, filtering constraints, and relational overrides inside your reporting applications are driven by the following optimized **DAX Expressions** saved within the `_Measure` container table:

---🔹 1. Total Employee
Computes total corporate hiring footprint while forcing an alternative relationship path between the employee registry and the central date calendar:
```dax
Total Employee = 
CALCULATE(
    COUNT(DimEmployee[EmployeeID]),
          USERELATIONSHIP(DimEmployee[HireDate],DimDate[Date])
)
```

--- 🔹 2. Active Employee
Isolates active workers currently on payroll by filtering the workforce table down to records where attrition equals "NO":
```dax
Active Employee = 
CALCULATE(
    [Total Employee],
    FILTER(
        DimEmployee,
    DimEmployee[Attrition]="NO"
    ),USERELATIONSHIP(DimEmployee[HireDate],DimDate[Date])
)
```

--- 🔹 3. InActive Employee
Filters total records down to voluntary and involuntary exit accounts matching the "YES" criteria:
```dax
InActive Employee = 
CALCULATE(
    [Total Employee],
    FILTER(
        DimEmployee,
    DimEmployee[Attrition]="YES"
    ),USERELATIONSHIP(DimEmployee[HireDate],DimDate[Date])
)
```

--- 🔹 4. Attrition Rate

Computes the structural loss coefficient by dividing total inactive exit volume by the aggregate employee footprint:
dax Attretion Rate = [InActive Employee]/[Total Employee] 

--- 🔹 5. Last Review Date
Retrieves the most recent evaluation date logged for an employee, and returns a placeholder text string if no record exists:
dax Last Review Date = IF( MAX(PerformanceRating[ReviewDate])= BLANK(), "no rewiew yet", MAX(PerformanceRating[ReviewDate]) ) 

--- 🔹 6. Next Review Date
An advanced measure that utilizes a local variable (Var) to check an employee's history. It calculates the next review deadline by adding a fixed 365-day fiscal window to either their last review date or their original hire date:
dax Next Review = Var hire_or_review= IF( MAX(PerformanceRating[ReviewDate])=BLANK(), MAX(DimEmployee[HireDate]), MAXA(PerformanceRating[ReviewDate]) ) RETURN 365+hire_or_review 

--- 🔹 7. Job Satisfaction Index (JobSatisfaction)
Extracts the maximum recorded satisfaction score per cohort while forcing a relationship override with the dimension lookup file:
dax JobSatisfaction = CALCULATE( MAX(PerformanceRating[JobSatisfaction]), USERELATIONSHIP(PerformanceRating[JobSatisfaction],SatisfiedLevel[SatisfactionID]) )

--- 🔹 8. Environment Comfort Index (EnvironmentSatisfaction)
Extracts physical workspace comfort parameters while activating the non-active relationship line leading to the satisfaction mapping table:
dax EnvironmentSatisfaction = CALCULATE( MAX(PerformanceRating[EnvironmentSatisfaction]), USERELATIONSHIP(PerformanceRating[EnvironmentSatisfaction],SatisfiedLevel[SatisfactionID]) ) 

--- 🔹 9. Relationship Morale Index (RelationshipSatisfaction)
Tracks internal peer relationship sentiment scores while managing relationship pathways down to the target dimension table:
dax RelationshipSatisfaction = CALCULATE( MAX(PerformanceRating[RelationshipSatisfaction]), USERELATIONSHIP(PerformanceRating[RelationshipSatisfaction],SatisfiedLevel[SatisfactionID]) )

--- 🔹 10. Work-Life Balance Index (WorkLifeBalanceSatisfaction)
Computes personal and professional alignment scores while routing data validation queries down to the centralized satisfaction lookup index:
dax WorkLifeBalanceSatisfaction = CALCULATE( MAX(PerformanceRating[WorkLifeBalance]), USERELATIONSHIP(PerformanceRating[WorkLifeBalance],SatisfiedLevel[SatisfactionID]) ) 

--- 🔹 11. Manager Evaluation Score (ManagerRating)
Tracks annual employee performance scores assigned by their direct line manager while applying relationship overrides to the evaluation table:
dax ManagerRating = CALCULATE(MAX(PerformanceRating[ManagerRating]), USERELATIONSHIP(PerformanceRating[ManagerRating],RatingLevel[RatingID]) ) 

--- 🔹 12. Self Evaluation Score (SelfRating)
Retrieves the maximum performance rating an employee assigns to their own output, utilizing an alternative relationship path to the lookup table:
dax SelfRating = CALCULATE(MAX(PerformanceRating[SelfRating]), USERELATIONSHIP(PerformanceRating[SelfRating],RatingLevel[RatingID]) ) 
------------------------------
--- 🚀 Execution, Environment Settings & Local Data Mapping

   1. Confirm Microsoft Power BI Desktop (latest stable release) is installed on your local windows client station.
   2. Clone this Git repository or download the source .pbix report file to your local drive.
   3. Open the .pbix report asset; the unified layout form, sidebar filters, Snow schema relationships, and all 12 core DAX measures will initialize instantly.
   4. To link local data tables to your network directories, navigate to the upper Ribbon layout, select Transform Data ➡️ Data Source Settings, modify the file directory paths to match your local storage structure, and click Refresh.


---



