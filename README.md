# Linear-regression-in-R
#Import the data
x=read.csv("C:\\Users\\DELL\\Desktop\\task1.csv")
 x

#fit simple linear regression to given data
model=lm(scores~Hours,data=x)
summary(model)

#prediction of scores on basis of no. of study hours
new.Hours<-data.frame(Hours=c(9.25))
predict(model,newdata=new.Hours)

#Graphical representation of data
plot(x,pch=16,col="blue")
abline(model)
