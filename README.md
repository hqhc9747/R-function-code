# R-function-code
#自己定义的一些R小函数

# r range 利用R来计算极差标准化，又称离差标准化、规范化
# 公式 r=x-x_min/(x_max-x_min)
# 下面给出R软件 求极差标准化的一个函数
scalerange<-function(x){
  x<-as.vector(x)
  x_min<-min(x) 
  x_max<-max(x)
  extreme<-(x_max-x_min)
  y<-(x-x_min)/extreme
  return(y)
}

#ex：
x<-c(1,2,3,4,5,6)
scalestand(x)
#输出结果：
#> scalestand(x)
#[1] 0.0 0.2 0.4 0.6 0.8 1.0
