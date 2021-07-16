# Been
금융데이터경진대회


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
