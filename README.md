# cpp-student-report-form
cpp student report form for 5 students OOP
#include<iostream>
#include<conio.h>
using namespace std;

class student{
	char rlno[10];
	char name[10];
	float m1,m2,m3,m4,m5;
	float avg,sum;
	public :
		void read_data();
		void compute();
		void display();
};
void student::read_data(){
	cout<< "\nEnter the student roll number: ";
	cin>>rlno;
	cout<<"Enter the Student Name:";
	cin>>name;
	cout<<"\nEnter marks for Maths ";
	cin>>m1;
    cout<<"\nEnter marks for English ";
    cin>>m2;
    cout<<"\nEnter marks for Swa ";
    cin>>m3;
    cout<<"\nEnter marks for Sci ";
    cin>>m4;
    cout<<"\nEnter marks for S/S ";
	cin>>m5;
}
void student::compute()
{
    avg=(m1+m2+m3+m4+m5)/5;
    sum=m1+m2+m3+m4+m5;
}
void  student::display()
{
    cout<<"\n ------------------------------------------------------\n";
    cout<<name<<" details\n";
    cout<<"\n ------------------------------------------------------\n";
    cout<<"\n Rollno is "<<rlno;
    cout<<"\n Name of student is "<<name;
    cout<<"\n Maths is "<<m1;
    cout<<"\n English is "<<m2;
    cout<<"\n Swa is "<<m3;
    cout<<"\n Sci is "<<m4;
    cout<<"\n S/S is "<<m5;
    cout<<"\n The average mark of five subjects is "<<avg;
    cout<<"\n Sum of five subjects is "<< sum;
    if(avg>=90 && avg <=100)
    	cout<<"\nYour grade is A" <<endl;
    else if(avg>=80 && avg<=89)
		cout<<"\nYour grade is B"<<endl;
    else if(avg>=70 && avg<=79)
		cout<<"\nYour grade is C"<<endl;
	else if(avg>=60 && avg<=69)
		cout<<"\nYour grade is D"<<endl;
	else
		cout<<"\nYour grade is E"<<endl;
	cout<<"\n ------------------------------------------------------\n";
	cout<<"PRESS ENTER TO CONTINUE..."<<endl;
}
int main()
{
    student s[10];
    int i;
    system ("cls");
    for(i=0;i<5;i++){
    s[i].read_data();
    s[i].compute();
    s[i].display();
    getch();
	}
   return 0;
}


