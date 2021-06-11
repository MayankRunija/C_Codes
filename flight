#include<iostream>
#include<conio.h>
using namespace std;

class flight_cal{

private : int flight ;
          char desti[20]; 
          float dis,fuel;
          
public  : feedinfo();
          calfuel();
		  showinfo();
		       
};

int flight_cal::feedinfo()
{
	cout<<"\n enter your flight number :";
	cin>>flight;
	cout<<"\n enter your destination :";
	cin>>desti;
	cout<<"\n enter your travling distace :";
	cin>>dis;
    return 0;
}

int flight_cal::calfuel()
{
	if(dis<=1000)
    {
             fuel=500;
    }	                     
    else if(dis>1000 && dis<=2000)
    {
             fuel=1100;  
	}
    else
    {
            fuel=2200;	
    }

 return 0;
}

int flight_cal::showinfo()
{
	cout<<"Your flight no is :"<<flight;
	cout<<"\nYour destination is :"<<desti;
	cout<<"\nYour distance in km :"<<dis;
    cout<<"\nfuel used in your flight is :"<<fuel;
     return 0;
}

int main()
{
	flight_cal f;
	f.feedinfo();
	f.calfuel();
	f.showinfo();
	
	return 0;

}
