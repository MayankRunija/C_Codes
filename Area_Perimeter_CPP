#include<iostream>
using namespace std;

class rectangle
{
float length;
float breadth;

public :

void setdata(float l , float b);

float perimeter();
float area();
void show();
};

void rectangle::setdata(float l,float b)
{
length=l;
breadth=b;
}

float rectangle::perimeter()
{
float peri;

peri=2*(length+breadth);

return (peri);
}

float rectangle::area()
{
float area;

area=length*breadth;

return (area);

}

void rectangle::show()
{
cout<<"\nlength -:"<<length;
cout<<"\nbreath -:"<<breadth;
cout<<"\narea -:"<<area();

}


int main()
{
    rectangle r1,r2;
    r1.setdata(5,2.5);
    r2.setdata(5,18.5);
    cout<<"rectangle 1\n";
    r1.show();
    cout<<"\nPerimeter ="<<r1.perimeter();
 // cout<<"\nArea ="<<r1.area();
    cout<<"\n\nrectangle 2\n";
    r2.show();
    cout<<"\nperimeter="<<r2.perimeter();
//  cout<<"\narea="<<r2.area();

    return 0;
}
