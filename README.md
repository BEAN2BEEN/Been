# Been
금융데이터경진대회
![image](https://user-images.githubusercontent.com/87536808/126027541-ed2c1bfa-51bb-499b-be0c-22513df74aca.png)
![image](https://user-images.githubusercontent.com/87536808/126027553-70b1fece-2ca3-4c70-a3fb-b009699d45cb.png)
![image](https://user-images.githubusercontent.com/87536808/126027554-07e6e7b2-6a2b-4fbe-82bf-4801a5b127ab.png)
![image](https://user-images.githubusercontent.com/87536808/126027558-733a9f25-c8fb-4748-94fb-c8f7e0d2ef6c.png)
![image](https://user-images.githubusercontent.com/87536808/126027572-d76c2577-cce0-4fc7-93e8-96056f54febe.png)
![image](https://user-images.githubusercontent.com/87536808/126027576-fe5f3c6f-3cd3-4b21-bc1b-69791b8c69a0.png)
![image](https://user-images.githubusercontent.com/87536808/126027577-f638a98a-138c-4f80-a9c2-a77978d283ec.png)
![image](https://user-images.githubusercontent.com/87536808/126027584-06112976-18eb-4f4b-9ebb-fe46605eeb11.png)
![image](https://user-images.githubusercontent.com/87536808/126027586-c583ddaf-f464-4fc2-94f3-5ac6036c4875.png)
![image](https://user-images.githubusercontent.com/87536808/126027592-6626c463-ee8b-4c25-8642-ee2299d3d3a1.png)
![image](https://user-images.githubusercontent.com/87536808/126027599-1fdcfcf7-1303-404d-bfd1-82101ef21fe6.png)


```r
install.packages("dplyr")
library(dplyr)
install.packages("ggplot2")
library(ggplot2)
install.packages("UsingR")
library(UsingR)

shin<-read.csv("C:\\Users\\Hanbeen Cho\\Desktop\\신한은행_경진대회.csv", quote= "")
shin

dim(shin)
dim(shin[complete.cases(shin),])
head(shin)

aggregate(신용대출금액~기준년월, shin, mean)
##갈수록 신용대출금액이 올라감 // 코로나로 인한 것인지, 아니면 단순 투자용?

aggregate(신용대출금액~기준년월+가맹점매출입금, shin, mean)
##신용대출금액이 0인, 가맹정매출입금도 0인 곳을 지우고 싶은데 그걸 못찾았어요...

summary(shin$신용대출금액)
```
