 tbl_df/tbl/data.frame)
 $ participant_id            : num [1:2000] 1 2 3 4 5 6 7 8 9 10 ...
 $ sex                       : chr [1:2000] "M" "M" "M" "M" ...
 $ age                       : num [1:2000] 46 25 53 46 32 28 34 34 49 60 ...
 $ measurement_date          : chr [1:2000] "2019-01-19" "2018-03-16" "2017-06-02" "2018-02-11" ...
 $ bmi                       : num [1:2000] 26.5 28.8 25.7 28 25 24.7 24.7 27.8 25 24.6 ...
 $ percent_body_fat          : num [1:2000] 45 45 45 45 57.7 60 60 45 45 45 ...
 $ hand_grip_strength_kg     : num [1:2000] 47 28 37.7 48.9 20 21.2 28.9 38.2 41.9 34.1 ...
 $ sit_and_reach_cm          : num [1:2000] 13.4 -1.2 4.5 9 14.8 13.1 3.9 17.1 9.9 14.6 ...
 $ sit_ups_count             : num [1:2000] 13 19 18 20 23 27 17 12 12 15 ...
 $ vo2_estimate_ml_per_kg_min: num [1:2000] 29.8 46.5 37.2 52.5 24.6 30.1 30 45.7 39.5 28.8 ...   how  can i deal with categorical var
tibble [2,000 × 12] (S3: tbl_df/tbl/data.frame)
 $ participant_id            : num [1:2000] 1 2 3 4 5 6 7 8 9 10 ...
 $ sex                       : Factor w/ 2 levels "F","M": 2 2 2 2 1 1 1 2 2 2 ...
 $ age                       : num [1:2000] 46 25 53 46 32 28 34 34 49 60 ...
 $ measurement_date          : chr [1:2000] "2019-01-19" "2018-03-16" "2017-06-02" "2018-02-11" ...
 $ bmi                       : num [1:2000] 26.5 28.8 25.7 28 25 24.7 24.7 27.8 25 24.6 ...
 $ percent_body_fat          : num [1:2000] 45 45 45 45 57.7 60 60 45 45 45 ...
 $ hand_grip_strength_kg     : num [1:2000] 47 28 37.7 48.9 20 21.2 28.9 38.2 41.9 34.1 ...
 $ sit_and_reach_cm          : num [1:2000] 13.4 -1.2 4.5 9 14.8 13.1 3.9 17.1 9.9 14.6 ...
 $ sit_ups_count             : num [1:2000] 13 19 18 20 23 27 17 12 12 15 ...
 $ vo2_estimate_ml_per_kg_min: num [1:2000] 29.8 46.5 37.2 52.5 24.6 30.1 30 45.7 39.5 28.8 ...
 $ sex_encoded               : num [1:2000] 1 1 1 1 0 0 0 1 1 1 ...
 $ sex_std                   : num [1:2000, 1] 0.69 0.69 0.69 0.69 -1.45 ...
  ..- attr(*, "scaled:center")= num 0.677
  ..- attr(*, "scaled:scale")= num 0.468  here is the result  but sex is transformed to num ?
NO I AM WORKING ON STATIC PROJECT 
NO I WANT TO SEE PLOTS  THEN TAKE A LOOOK THEN I WANT TO DEAL WITH  OUTLIERS IF THER IS 
I MEAN BOXPLOT TO DETECT OUTLIERS NOT SIMPLE PLOT 
FOR BODYFAT 
I WANT  Traitement des valeurs aberrantes :
Boxplots   Avant le Traitement des Valeurs Aberrantes   AND APRES TRAITEMENT  
I WANT  A RESUMEE ABOUT WHAT WE DIT IN ENGLISH 
I WANT SAME PROCESS FOR BMI AND VO2
I WANT NOW FOR HAND GRID
no i want data transfomation  because  some histogram dont show normal distribution 
no iwant using minmax scaler or standrd 
       V1         
 Min.   :-3.0474  
 1st Qu.:-0.4001  
 Median :-0.4001  
 Mean   : 0.0000  
 3rd Qu.: 0.7912  
 Max.   : 1.7464  
but the histogram of percent body fat look unchanged and its not normaly distributed 
no thing change 
yes 
no iwant Supprimer les colonnes fortement corrélées
Error: object 'cor_matrix' not found
 
> num_vars <- a %>% select(age, bmi, percent_body_fat, hand_grip_strength_kg,
+                          sit_and_reach_cm, sit_ups_count, vo2_estimate_ml_per_kg_min)
Error in select(., age, bmi, percent_body_fat, hand_grip_strength_kg,  : 
  unused arguments (age, bmi, percent_body_fat, hand_grip_strength_kg, sit_and_reach_cm, sit_ups_count, vo2_estimate_ml_per_kg_min)
> 
 
> num_vars <- a %>% select(age, bmi, percent_body_fat, hand_grip_strength_kg,
+                          sit_and_reach_cm, sit_ups_count, vo2_estimate_ml_per_kg_min)
Error in select(., age, bmi, percent_body_fat, hand_grip_strength_kg,  : 
  unused arguments (age, bmi, percent_body_fat, hand_grip_strength_kg, sit_and_reach_cm, sit_ups_count, vo2_estimate_ml_per_kg_min)
> 
i want visualise corr matrix 
cor_matrix, method = "color", type = "upper", tl.col = "black",  : 
  could not find function "corrplot"cor_matrix, method = "color", type = "upper", tl.col = "black",  : 
  could not find function "corrplot"
r
Error: object 'clear' not found
> install.packages("corrplot")
Installing package into ‘C:/Users/SOSORDINATEUR/AppData/Local/R/win-library/4.5’
(as ‘lib’ is unspecified)
Warning: unable to access index for repository https://pbil.univ-lyon1.fr/CRAN/src/contrib:
  cannot open the connection
Warning: unable to access index for repository https://pbil.univ-lyon1.fr/CRAN/bin/windows/contrib/4.5:
  cannot open the connection
Warning messages:
1: In gzfile(file, "rb") :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm/repos_https%3A%2F%2Fpbil.univ-lyon1.fr%2FCRAN%2Fsrc%2Fcontrib.rds', probable reason 'No such file or directory'
2: In read.dcf(file = tmpf) :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm\filea1747dda1880', probable reason 'No such file or directory'
3: package ‘corrplot’ is not available for this version of R

A version of this package for your version of R might be available elsewhere,
see the ideas at
https://cran.r-project.org/doc/manuals/r-patched/R-admin.html#Installing-packages 
4: In gzfile(file, "rb") :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm/repos_https%3A%2F%2Fpbil.univ-lyon1.fr%2FCRAN%2Fbin%2Fwindows%2Fcontrib%2F4.5.rds', probable reason 'No such file or directory'
5: In read.dcf(file = tmpf) :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm\filea17456fc7bec', probable reason 'No such file or directory'
> 
stalling package into ‘C:/Users/SOSORDINATEUR/AppData/Local/R/win-library/4.5’
(as ‘lib’ is unspecified)
Warning: unable to access index for repository https://cran.case.edu/src/contrib:
  cannot open the connection
Warning: unable to access index for repository https://cran.case.edu/bin/windows/contrib/4.5:
  cannot open the connection
Warning messages:
1: In gzfile(file, "rb") :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm/repos_https%3A%2F%2Fcran.case.edu%2Fsrc%2Fcontrib.rds', probable reason 'No such file or directory'
2: In read.dcf(file = tmpf) :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm\filea174df03584', probable reason 'No such file or directory'
3: package ‘corrplot’ is not available for this version of R

A version of this package for your version of R might be available elsewhere,
see the ideas at
https://cran.r-project.org/doc/manuals/r-patched/R-admin.html#Installing-packages 
4: In gzfile(file, "rb") :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm/repos_https%3A%2F%2Fcran.case.edu%2Fbin%2Fwindows%2Fcontrib%2F4.5.rds', probable reason 'No such file or directory'
5: In read.dcf(file = tmpf) :
  cannot open compressed file 'C:\Users\SOSORD~1\AppData\Local\Temp\RtmpusbaOm\filea1748fe7824', probable reason 'No such file or directory'
> library(corrplot)
Error in library(corrplot) : there is no package called ‘corrplot’
> 
Supprimer les colonnes fortement corrélées
Après avoir identifié les colonnes corrélées, elles sont
supprimées itérativement jusqu'à ce que la matrice de
corrélation réduite ne contienne que des relations
faibles ou modérées. 
Enfin, une heatmap est générée pour visualiser les
corrélations restantes et sauvegarder les résultats pour
une utilisation future. 
Cette approche assure un dataset compact et optimisé
pour des analyses ultérieures.
analyser les corrélations entre les colonnes numériques d'un dataset et à supprimer les colonnes
redondantes qui présentent une corrélation élevée avec d'autres (supérieure à 0.8
avoir"
> supprimées itérativement jusqu'à ce que la matrice de
Error: unexpected symbol in "supprimées itérativement"
> corrélation réduite ne contienne que des relations
Error: unexpected symbol in "corrélation réduite"
> faibles ou modérées. 
Error: unexpected symbol in "faibles ou"
> Enfin, une heatmap est générée pour visualiser les
Error: unexpected ',' in "Enfin,"
> corrélations restantes et sauvegarder les résultats pour
Error: unexpected symbol in "corrélations restantes"
> une utilisation future. 
Error: unexpected symbol in "une utilisation"
> Cette approche assure un dataset compact et optimisé
Error: unexpected symbol in "Cette approche"
> pour des analyses ultérieures.
Error: unexpected symbol in "pour des"
> analyser les corrélations entre les colonnes numériques d'un dataset et à supprimer les colonnes
Error: unexpected symbol in "analyser les"
> redondantes qui présentent une corrélation élevée avec d'autres (supérieure à 0.8
Error: unexpected symbol in "redondantes qui"
> library(caret)
Error in library(caret) : there is no package called ‘caret’
> 
> # Supprimer les colonnes avec corrélation > 0.8
> high_cor <- findCorrelation(cor_matrix, cutoff = 0.8, names = TRUE)
Error in findCorrelation(cor_matrix, cutoff = 0.8, names = TRUE) : 
  could not find function "findCorrelation"
> high_cor  # colonnes à supprimer
Error: object 'high_cor' not found
no give me a reumee about what we do and the goal  iwant to be short 
 now lets move to 6. Independent Samples Test (Gender Differences)

(Following the ANOVA/Independent t-test structure of your PDF)

A t-test revealed a highly significant difference in mean HGS between genders:

Males > Females, p < 0.001

Effect size: large (Cohen’s d > 0.8)

Anthropometric variables also showed significant gender differences consistent with known biological patterns.
no  shapiro_results
$participant_id

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.95487, p-value < 2.2e-16


$age

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.95524, p-value < 2.2e-16


$bmi

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99871, p-value = 0.1413


$percent_body_fat

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$hand_grip_strength_kg

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.9934, p-value = 8.218e-08


$sit_and_reach_cm

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99911, p-value = 0.441


$sit_ups_count

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99218, p-value = 7.357e-09


$vo2_estimate_ml_per_kg_min

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99956, p-value = 0.9484


$sex_encoded

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.58909, p-value < 2.2e-16


$sex_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.58909, p-value < 2.2e-16


$percent_body_fat_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.81844, p-value < 2.2e-16


$bmi_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99793, p-value = 0.01104


$vo2_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99858, p-value = 0.0935


$hand_grip_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99336, p-value = 7.622e-08


$percent_body_fat_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$percent_body_fat_mm

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$percent_body_fat_sqrt

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.83298, p-value < 2.2e-16


$percent_body_fat_log

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.84085, p-value < 2.2e-16


$percent_body_fat_log_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.84085, p-value < 2.2e-16


> num_vars <- a[, sapply(a, is.numeric)]
> shapiro_results <- lapply(num_vars, shapiro.test)
> 
> # View results
> shapiro_results
$participant_id

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.95487, p-value < 2.2e-16


$age

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.95524, p-value < 2.2e-16


$bmi

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99871, p-value = 0.1413


$percent_body_fat

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$hand_grip_strength_kg

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.9934, p-value = 8.218e-08


$sit_and_reach_cm

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99911, p-value = 0.441


$sit_ups_count

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99218, p-value = 7.357e-09


$vo2_estimate_ml_per_kg_min

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99956, p-value = 0.9484


$sex_encoded

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.58909, p-value < 2.2e-16


$sex_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.58909, p-value < 2.2e-16


$percent_body_fat_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.81844, p-value < 2.2e-16


$bmi_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99793, p-value = 0.01104


$vo2_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99858, p-value = 0.0935


$hand_grip_clean

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.99336, p-value = 7.622e-08


$percent_body_fat_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$percent_body_fat_mm

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.82198, p-value < 2.2e-16


$percent_body_fat_sqrt

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.83298, p-value < 2.2e-16


$percent_body_fat_log

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.84085, p-value < 2.2e-16


$percent_body_fat_log_std

        Shapiro-Wilk normality test

data:  X[[i]]
W = 0.84085, p-value < 2.2e-16

no a ctually my goal here consist of use multi linear regression 

**The dependent variable (Y)** should ideally be approximately normal.

whats  the y in my case 
yes 

Notes
Outils
Déconnexion
Confidentialité
Conditions générales
Accessibilité
Cours
Semestre 1
filter-all-courses
ESE.IA003__4DS2
Aller directement au contenu principal
Statistics__4DS2
Ouvert
Statut du cours Ouvert
Contenu du cours
The objective of this module is to familiarize the student with the main tools offered by statistics to collect, process, interpret real data and then exploit the results obtained. At the same time, students learn a programming language and become familiar with data analysis software (R).
TP 0 : Simulations and hypothesis tests
Correction TP0 : Simulations and hypothesis tests
Data preparation steps: 1 Data collection. 2 Discover and evaluate data. 3 Clean and validate data 4 Transform and enrich data. 5 Store data.
TP 1 : Data Preparation
Correction TP 1 : Data Preparation
Test : Data Preparation
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Quiz : Data Preparation
Date d'échéance : 29/06/2024 11:59 (UTC-11)
20 éléments commencés sur 21

TP2 : Tests with two independent samples
Correction TP 2 : Parametric tests
Devoir : Hypothesis testing for means
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Quiz : Parametric hypothesis testing: Case of two independent Samples
Date d'échéance : 29/06/2024 11:59 (UTC-11)
In this chapter, we explore simple and multiple linear regression.
2 éléments terminés sur 12

Introduction
The steps of a linear regression
Principle
Model
Parameter estimation
Quality of adjustment
Conditions of application
R command and interpretation
TP3 : Simple and multiple linear regression
boston_house_prices (1).prn
ozone.txt
TP3- linear regression.pdf
Correction TP 3 : Simple and multiple linear regression
Linear Regression
Aucune date d'échéance
Quiz : Simple and multiple linear regression
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Devoir : Multiple Linear Regression
Date d'échéance : 29/06/2024 11:59 (UTC-11)
This chapter is dedicated to the study of the dependence between a qualitative variable and a quantitative variable.
3 éléments commencés sur 4

Resistance.txt
TP 4 : One-Way Analysis of Variance
Correction TP4 : One-way analysis of variance
Test : ONE FACTOR ANALYSIS OF VARIANCE
Date d'échéance : 27/06/2024 11:59 (UTC-11)
Quiz : ANOVA
Date d'échéance : 29/06/2024 11:59 (UTC-11)
5 éléments commencés sur 6

TP 5 : Non Parametric Tests
Correction TP 5 : Non parametric Tests
Quiz : Non Parametric test
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Terminé

TP 6 : Measurement of linear dependencies
Correction TP 6 : Measurement of linear dependencies
Quiz : Measurement of linear dependencies
Date d'échéance : 01/07/2024 11:59 (UTC-11)
Test for linear dependence measures between a quantitative variable and a qualitative variable .
Date d'échéance : 01/07/2024 11:59 (UTC-11)
Students will have to reproduce the methodology of the article, analyze and interpret the results obtained on their data, then formulate recommendations.
Theoretical-test
Students will have to reproduce the methodology of the article, analyze and interpret the results obtained on their data, then formulate recommendations.
5 éléments commencés sur 11

Procedures for working
Project 1 : How to choose and interpret a statistical test? An update for budding researchers
Project 5 : Simplifying Statistical Decision Making : A research scholar guide to parametric and non parametric methods
Exam
Corps enseignant du cours
Amel Hedhli
Enseignant

Achref LEMJID
Enseignant

Détails et actions
Annuaire
Afficher tous les membres de votre cours

Présence
Afficher votre présence

Manuels et outils
Afficher les outils du cours et de l'établissement

×
Chapter 3 : Linear regression

Parameter estimation
Estimation of the parameters

We are looking for estimates ﻿beta with hat on top subscript 0 comma beta with hat on top subscript 1 comma horizontal ellipsis comma beta with hat on top subscript k﻿ of parameters ﻿beta subscript 0 comma beta subscript 1 comma horizontal ellipsis comma beta subscript k﻿ 

Least-Squares criterion : Ordinary Least-Squares (OLS) estimate ﻿beta with hat on top subscript 0 comma beta with hat on top subscript 1 comma horizontal ellipsis comma beta with hat on top subscript k﻿ minimizes

  ﻿sum from i equals 1 to n of space left parenthesis y subscript i minus beta subscript 0 minus beta subscript 1 x subscript i 1 end subscript minus horizontal ellipsis minus beta subscript k x subscript i k end subscript right parenthesis squared﻿

﻿beta with hat on top equals left parenthesis X apostrophe X right parenthesis to the power of negative 1 end exponent X apostrophe y﻿

﻿beta with hat on top colon﻿: is the slope coefficient for each independent variable ﻿beta﻿

    ﻿y with hat on top﻿ : ﻿X beta with hat on top space﻿ vector of ﻿y subscript i﻿

    ﻿e﻿ = ﻿y minus y with hat on top space﻿ is the model’s random error (residual) term.

×

Notes
Outils
Déconnexion
Confidentialité
Conditions générales
Accessibilité
Cours
Semestre 1
filter-all-courses
ESE.IA003__4DS2
Aller directement au contenu principal
Statistics__4DS2
Ouvert
Statut du cours Ouvert
Contenu du cours
The objective of this module is to familiarize the student with the main tools offered by statistics to collect, process, interpret real data and then exploit the results obtained. At the same time, students learn a programming language and become familiar with data analysis software (R).
TP 0 : Simulations and hypothesis tests
Correction TP0 : Simulations and hypothesis tests
Data preparation steps: 1 Data collection. 2 Discover and evaluate data. 3 Clean and validate data 4 Transform and enrich data. 5 Store data.
TP 1 : Data Preparation
Correction TP 1 : Data Preparation
Test : Data Preparation
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Quiz : Data Preparation
Date d'échéance : 29/06/2024 11:59 (UTC-11)
20 éléments commencés sur 21

TP2 : Tests with two independent samples
Correction TP 2 : Parametric tests
Devoir : Hypothesis testing for means
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Quiz : Parametric hypothesis testing: Case of two independent Samples
Date d'échéance : 29/06/2024 11:59 (UTC-11)
In this chapter, we explore simple and multiple linear regression.
2 éléments terminés sur 12

Introduction
The steps of a linear regression
Principle
Model
Parameter estimation
Quality of adjustment
Conditions of application
R command and interpretation
TP3 : Simple and multiple linear regression
boston_house_prices (1).prn
ozone.txt
TP3- linear regression.pdf
Correction TP 3 : Simple and multiple linear regression
Linear Regression
Aucune date d'échéance
Quiz : Simple and multiple linear regression
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Devoir : Multiple Linear Regression
Date d'échéance : 29/06/2024 11:59 (UTC-11)
This chapter is dedicated to the study of the dependence between a qualitative variable and a quantitative variable.
3 éléments commencés sur 4

Resistance.txt
TP 4 : One-Way Analysis of Variance
Correction TP4 : One-way analysis of variance
Test : ONE FACTOR ANALYSIS OF VARIANCE
Date d'échéance : 27/06/2024 11:59 (UTC-11)
Quiz : ANOVA
Date d'échéance : 29/06/2024 11:59 (UTC-11)
5 éléments commencés sur 6

TP 5 : Non Parametric Tests
Correction TP 5 : Non parametric Tests
Quiz : Non Parametric test
Date d'échéance : 29/06/2024 11:59 (UTC-11)
Terminé

TP 6 : Measurement of linear dependencies
Correction TP 6 : Measurement of linear dependencies
Quiz : Measurement of linear dependencies
Date d'échéance : 01/07/2024 11:59 (UTC-11)
Test for linear dependence measures between a quantitative variable and a qualitative variable .
Date d'échéance : 01/07/2024 11:59 (UTC-11)
Students will have to reproduce the methodology of the article, analyze and interpret the results obtained on their data, then formulate recommendations.
Theoretical-test
Students will have to reproduce the methodology of the article, analyze and interpret the results obtained on their data, then formulate recommendations.
5 éléments commencés sur 11

Procedures for working
Project 1 : How to choose and interpret a statistical test? An update for budding researchers
Project 5 : Simplifying Statistical Decision Making : A research scholar guide to parametric and non parametric methods
Exam
Corps enseignant du cours
Amel Hedhli
Enseignant

Achref LEMJID
Enseignant

Détails et actions
Annuaire
Afficher tous les membres de votre cours

Présence
Afficher votre présence

Manuels et outils
Afficher les outils du cours et de l'établissement

×
Chapter 3 : Linear regression

Model
Model

Multiple linear regression models are defined by the equation :

﻿Y equals beta subscript 0 plus beta subscript 1 space X subscript 1 plus horizontal ellipsis plus beta subscript k space X subscript k plus epsilon﻿

 où  ﻿beta subscript j﻿ : Parameters

   ﻿epsilon﻿ : the residuals

Response or dependent variable :

Y : Response variable, dependent variable

﻿X subscript 1 comma X subscript 2 comma horizontal ellipsis comma X subscript k﻿ : Explanatory variable, independent variable   Quality of adjustment

﻿stack sum from i equals 1 to n of left parenthesis y subscript i minus y with bar on top right parenthesis squared with underbrace below﻿ =﻿stack sum from i equals 1 to n of left parenthesis y with hat on top subscript i minus y with bar on top right parenthesis squared with underbrace below﻿ + ﻿stack sum from i equals 1 to n of left parenthesis y subscript i minus y with hat on top subscript i right parenthesis squared with underbrace below﻿ 

       SCT. = SCE + SCR

 SCT : Sum of squares of the the deviation of model

SCE : Total Sum of the squares of the deviations

SCR : Residual Sum of squares



Coefficient of determination : It measures the proportion of the total variability that is explained by the model

﻿R squared equals fraction numerator S C E over denominator S C T end fraction﻿



Remark:

﻿R squared﻿ is based on the number of explanatory variables in the model. 

﻿p space north east arrow space ⟹ space R squared space north east arrow﻿  Conditions of application



As for simple linear regression, multiple linear regression requires some conditions of application for the model to be usable and the results to be interpretable. Conditions for simple linear regression also apply to multiple linear regression, that is : 

Linearity of the relationships between the dependent and independent variables
 Independence of the observations
 Normality of the residuals
Homoscedasticity of the residuals
Checking the normality of the residuals

 histogram ﻿space ⟹ space﻿ the distribution must be unimodal and symmetrical.
Testing for normality (Shapiro Wilkis, Kolmogrov-Smirnov,...).
Quantile-quantile plot ﻿space ⟹ space﻿ is a graphical tool to help us assess if a set of data plausibly came from some theoretical distribution such as a Normal.
Checking the homoscedasticity of the residuals

The variance of the errors should be constant. There is a lack of homoscedasticity when the dispersion of the residuals increases with the predicted values (fitted values). 

This condition can be tested visually (by plotting the standardized residuals vs. the fitted values).



residus.png   - Functions



Main generic functions to extract information resulting from an analysis.

﻿
print()
﻿ : returns a summary of the analysis

﻿
summary()
﻿ : returns a detailed summary of the analysis

   ﻿
coef()
﻿: returns the estimated coefficients

 ﻿
residuals()
﻿: returns residuals

  ﻿
fitted()
﻿ : returns the values adjusted by the model

      ﻿
AIC()
﻿: calculates the Akaike information criterion

Multiple Linear Regression Under R

 Linear Regression in R :

 ﻿y subscript i equals X beta plus epsilon subscript i﻿

model<-lm(﻿y space tilde operator space x 1 plus x 2 plus x 3 right parenthesis﻿

The main statistics of the model :

summary(model)

The Error Terms are Normally Distributed

Shapiro-Wilk normality test :

shapiro.test(resid(res))

data: resid(res)

W=0.9951 , p-value=0.3684

$$\Longrightarrow\;$$ The p-value is higher than the threshold and we cannot therefore reject the hypothesis $$\mbox{ H}_0$$. The residuals is therefore compatible with a normal distribution.

The Variance of the Error Terms is Constant Over All X Values

The fitted vs residuals plot is used again to determine if the variance is constant. Here is the plot again for reference :

plot(res\﻿f i t t e d. v a l u e s comma r e s﻿residuals,+xlab="Valeurs prédites par le modèle",+ ylab="Résidus",pch=16,cex=0.75,col="blue")

res.png    now based of the information    i gave u  iwant multi linear regression with  explication of each step  and with code  



×
cor_matrix <- cor(data_reg_scaled[, predictors])
> cor_matrix
                              age          bmi percent_body_fat
age                    1.00000000  0.018642938       0.02918639
bmi                    0.01864294  1.000000000       0.16157729
percent_body_fat       0.02918639  0.161577291       1.00000000
hand_grip_strength_kg  0.02370535  0.340667027      -0.52876285
sit_and_reach_cm      -0.06349720  0.005871172       0.12220711
sit_ups_count         -0.14178288 -0.045219811       0.21502414
                      hand_grip_strength_kg sit_and_reach_cm
age                              0.02370535     -0.063497197
bmi                              0.34066703      0.005871172
percent_body_fat                -0.52876285      0.122207109
hand_grip_strength_kg            1.00000000     -0.115369721
sit_and_reach_cm                -0.11536972      1.000000000
sit_ups_count                   -0.20766573      0.073488691
                      sit_ups_count
age                     -0.14178288
bmi                     -0.04521981
percent_body_fat         0.21502414
hand_grip_strength_kg   -0.20766573
sit_and_reach_cm         0.07348869
sit_ups_count            1.00000000
> 
> # Optional: check Variance Inflation Factor (VIF)
> # install.packages("car")
> library(car)
Loading required package: carData

Attaching package: ‘car’

The following object is masked from ‘package:dplyr’:

    recode

> model_temp <- lm(vo2_estimate_ml_per_kg_min ~ ., data = data_reg_scaled)
> vif(model_temp)
                  age                   bmi 
             1.029157              1.387376 
     percent_body_fat hand_grip_strength_kg 
             1.741146              1.893732 
     sit_and_reach_cm         sit_ups_count 
             1.024695              1.088078 
> 

Check VIF

WHATS VIF 
 
> # Summary
> summary(model)

Call:
lm(formula = vo2_estimate_ml_per_kg_min ~ ., data = data_reg_scaled)

Residuals:
     Min       1Q   Median       3Q      Max 
-20.3477  -4.2002   0.0585   4.2142  19.7266 

Coefficients:
                      Estimate Std. Error t value Pr(>|t|)    
(Intercept)           36.28285    0.13767 263.554  < 2e-16 ***
age                   -1.94827    0.13970 -13.947  < 2e-16 ***
bmi                    0.43100    0.16219   2.657  0.00794 ** 
percent_body_fat      -2.48114    0.18170 -13.655  < 2e-16 ***
hand_grip_strength_kg  0.51017    0.18950   2.692  0.00716 ** 
sit_and_reach_cm       0.04027    0.13939   0.289  0.77268    
sit_ups_count         -0.26285    0.14364  -1.830  0.06741 .  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 6.157 on 1993 degrees of freedom
Multiple R-squared:  0.2409,    Adjusted R-squared:  0.2387 
F-statistic: 105.4 on 6 and 1993 DF,  p-value: < 2.2e-16

>    I?TERPRET THE RESULTS 
YES

Homoscedasticity

whats that 
do we need anova here 

**5\. Final Step: Summary of Diagnostics** ------------------------------------------ * **Normality:** Check histogram/Q-Q plot & Shapiro-Wilk test * **Homoscedasticity:** Residuals vs fitted plot * **Independence:** Durbin-Watson test If all assumptions are met, your **multiple linear regression model is valid** and you can interpret the coefficients confidently.

yes
yes
YES
YES
DO WE NEED PEARSON COROLATION OR N OT 
