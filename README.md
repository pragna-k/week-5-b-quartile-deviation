# week-5-b-quartile-deviation
x <- scan()
n=length(x)
for (i in 1:n) {
  for (j in 1:(n-1)) {
    if (x[j]>x[j+1]) {
      t=x[j]
      x[j]=x[j+1]
      x[j+1]=t
    }
  }
}
print(x)
if(n%%2==0){
  q3<-x[(3*n)%/%4]
  print(q3)
  q1<-x[n%/%4]
  print(q1)
  qd<-(q3-q1)/2
} else {
  q3<-x[(3*(n+1))%/%4]
  print(q3)
  q1<-x[(n+1)%/%4]
  print(q1)
  qd<-(q3-q1)/2
}
print(" Quartile deviation using program:")
print(qd)



OUTPUT:
> x <- scan()
1: 5
2: 7
3: 4
4: 3
5: 6
6: 4
7: 2
8: 
Read 7 items
> n=length(x)
> for (i in 1:n) {
+   for (j in 1:(n-1)) {
+     if (x[j]>x[j+1]) {
+       t=x[j]
+       x[j]=x[j+1]
+       x[j+1]=t
+     }
+   }
+ }
> print(x)
[1] 2 3 4 4 5 6 7
> if(n%%2==0){
+   q3<-x[(3*n)%/%4]
+   print(q3)
+   q1<-x[n%/%4]
+   print(q1)
+   qd<-(q3-q1)/2
+ } else {
+   q3<-x[(3*(n+1))%/%4]
+   print(q3)
+   q1<-x[(n+1)%/%4]
+   print(q1)
+   qd<-(q3-q1)/2
+ }
[1] 6
[1] 3
> print(" Quartile deviation using program:")
[1] " Quartile deviation using program:"
> print(qd)
[1] 1.5
> 
