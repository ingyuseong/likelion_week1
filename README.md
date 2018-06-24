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

### 데이터 익스포팅 & 임포팅 & One-way ANOVA
```r
> install.package("xlsx")
> library("xlsx")
> write.xlsx(random_1, file = "C://forhw/1.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> write.xlsx(random_2, file = "C://forhw/2.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> write.xlsx(random_3, file = "C://forhw/3.xlsx", col.names = TRUE, row.names = TRUE, append = FALSE)
> cafe_anova <- read_excel("C://forhw/anova_cafe.xlsx")
> out <- aov(order ~ time_interval, data = cafe_anova)
> out
```

### shapiro.test
```r
> shapiro.test(random_1)
> shapiro.test(random_1)
> shapiro.test(random_1)
```

### 카페 데이터 난수 발생
```r
> random_1 <- rpois(50, lambda = 3.8333)
> random_2 <- rpois(50, lambda = 8.6667)
> random_3 <- rpois(50, lambda = 4)
```

### 카페 포아송 비교 plot
```r
> cafe_real <- read_excel("c://forhw/3.xlsx", col_names = F)
> plot(cafe_real$X__1, cafe_real$X__4, xlab = "nums", ylab = "probs", main = "Cafe Order")
> lines(0:16, dpois(0:16, lambda = 5.5), col ="red")
```

### 난수 회귀분석 및 회귀선 플로팅
```r
> plot(random_data$custo, random_data$clerk, main = "Scatter Plot (RANDOM)", xlim = c(0,20), ylim = c(0,14))
> r <- lm(custo ~ clerk, data = random_data)
> abline(r, col = "red")
> summary(r)
```

### 상관분석 및 corplot
```r
> random_custo <- rpois(50, lambda = 9.8333)
> random_clerk <- rpois(50, lambda = 7.6667)
> random_data <- data.frame(custo = random_custo, clerk = random_clerk)
> random_matrix <- cor(random_data)
> corrplot(random_matrix, method = "circle")
```

### 맘스터치 포아송 비교 plot
```r
> plot(custo_real$X__1, custo_real$X__4, main = "Customer Event")
> lines(0:20, dpois(0:20, lambda = 9.8333), col ="red")
> plot(cafe_real$X__1, cafe_real$X__4, main = "Clerk Event")
> lines(0:14, dpois(0:14, lambda = 7.6667), col ="red")
```
