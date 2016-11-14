# MatLab

h=0.1;
x=0:h:10;
y(1)=3;
for n=1:length(x)-1
    y(n+1) = y(n)+h*cos(x(n))*y(n);
end
plot(x,y)
hold on
clear
h=0.1;
x=0:-h:-7;
y(1)=3;  
for m=1:length(x)-1
    y(m+1) = y(m)- h*cos(x(m))*y(m);
end
plot(x,y,'r')
clear
[x,y] = ode45(@f1,[0,10],3);
plot(x,y)


-------------------------------------------


function res=f1(x,y)
res=cos(x)*y;

-------------------------------------------


x=0:0.1:9;
for k =1:30
xx==x+k;
yy=sin(xx);
plot(xx,yy)
axis([9,30,-3,3])
M(k)=getframe;
end
movie(M,3)

----------------------------------------


