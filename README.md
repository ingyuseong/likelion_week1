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

### bartlett.test
```r
bartlett.test(order ~ time_interval, data = cafe_anova)
```

### 데이터 익스포팅 & 임포팅
```r
write.xlsx(random_1, file = "C://forhw/1.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> write.xlsx(random_2, file = "C://forhw/2.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> write.xlsx(random_3, file = "C://forhw/3.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> cafe_anova <- read_excel("C://forhw/anova_cafe.xlsx")
> out <- aov(order ~ time_interval, data = cafe_anova)
> out
```
