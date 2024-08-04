#include<iostream>
using namespace std;
class booking
{
    public:
    string from;
    string to;
    int id;
      void data()
    {
        cout<<"WELCONE TO RAJ HOTEL"<<endl;
        cout<<"CHECK IN DATE:"<<endl;
      cin>>from;
        cout<<"CHECK OUT DATE:"<<endl;
        cin>>to;
        cout<<"id number (last 4 digit of adharno.)"<<endl;
        cin>>id;
     }
      void get()
    {
        cout<<"VERIFY YOUR ACCOUNT"<<endl;
       cout<<"ENTRY DATE: "<<from<<endl;
       cout<<"CHECK OUT DATE: "<<to<<endl;
       cout<<"YOUR ID NUMBER: "<<id<<endl;
       cout<<"NEXT STEP:     "<<endl;
    }
};
class room:public booking{
    public:

        int type;
            int amount;
    void typeR()
    {
               int rate=0;
     cout<<"ROOM BOOKING"<<endl;
        cout<<"1AcRoom 2 SimpleRoom"<<endl;
        cin>>type;
        switch(type)
        {
            case 1:
            rate=600;
            cout<<"per day cost:  "<<endl;            
            cout<<rate<<endl;
            cout<<"room booked"<<endl;
            break;
            case 2:
            rate=500;
            cout<<"per day cost"<<endl;            
             cout<<rate<<endl;
            cout<<"room booked "<<endl;
            break;
            default:
            cout<<"wrong choice";
            }
        
         int n;
         cout<<"number of days"<<endl;
         cin>>n;       
        amount=n*rate;
        cout<<"total amount:  "<<amount;
          cout<<endl;
   }
};

   class guest : public booking
    {
public:
    string customerName;
 
     int age;      
    void gst() 
    {
        cout<<" FIRST Name Of Customer"<<endl;
   cin>>customerName;
       cout<<"Your Age"<<endl;
        cin>>age;   
}
   };

   class payment:public room{
    public:
       int *ptr=&amount;
    void pay()
    {
        int *ptr=&amount;
            cout<<endl;
    int mehod;
    cout<<"1 for cash,2for online payment"<<endl;
    cout<<"enter ur choice";
    cin>>mehod;
    switch(mehod)
    {
        case 1:
        cout<<amount;
         cout<<"payment succesffuly"<<endl;
       
        break;
         case 2:
     cout<<"payment succesffuly"<<endl;   
        break;
        default:
        cout<<"wrong";
    }
    cout<<"thanku    visit again";
    }
   };
int main()
{
    booking b1;
    b1.data();
   b1.get();
   room r1;
   r1.typeR();
   guest g1;
   g1.gst();
payment p1;
p1.pay();
}
