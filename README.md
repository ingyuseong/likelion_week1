# likelion_week1
# Homework1
# R project Code

### 데이터 불러오기
```r
install.package("readxl")
library("readxl")
custo_real <- read_excel("C://forhw/pois_custo.xlsx")
clerk_real <- read_excel("C://forhw/pois_clerk.xlsx")
```

### ggplot
```r
ggplot(cafe_anova, aes(x = time_interval, y = order)) + 
+ geom_boxplot(fill = "grey80", col = "blue") +
+ scale_x_discrete() + xlab("Time Interval") +
+ ylab("Order")
```
