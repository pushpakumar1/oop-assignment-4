#include <iostream>
using namespace std;

class Student
{
    public:
        char name[100];
        char college[50];
        char event[50];
        int score;
    
        void get_data()
        {
            cout<<"Enter Name: ";
            cin>>name;
            cout<<"Enter College: ";
            cin>>college;
            cout<<"Enter name of event: ";
            cin>>event;
            cout<<"Enter score in event: ";
            cin>>score;
        }

        void display()
        {
            cout<<"\nName: "<<name;
            cout<<"\nCollege Name: "<<college;
            cout<<"\nEvent Name: "<<event;
            cout<<"\nScore in Event: "<<score;
        }
};

int main()
{
    int n,i;
    cout<<"Enter no. of students participating: ";
    cin>>n;
    
    Student st[n];

    for(i=0;i<n;i++)
        st[i].get_data();

    int max = st[0].score;
    int pos = 0;
    for(i=0;i<n;i++)
    {
        if(st[i].score>max)
        {
            max = st[i].score;
            pos = i;
        }
    }

    for(i=0;i<n;i++)
    {
        cout<<"\n\nDetails of Student "<<(i+1)<<" is: ";
        st[i].display();
    }

    cout<<"\n\nWinner of the event is "<<"Student "<<(pos+1)<<": \n";
    st[pos].display();

}


#include<stdio.h>
struct employee
{
 
char name[30];
int id; 
int salary; 
}; 
int main() 
{ 
int n ,netSalary; 
printf("Enter the number of employuee"); 
scanf("%d",&n); 
struct employee p[n]; 
for(int i=0; i<n; i++){ 
printf("Employee %d:- \n",i+1);
 
//Name 
printf("Name: "); 
scanf("%s",p[i].name); 

//ID 
printf("Id: "); 
scanf("%d",&p[i].id);
 
//Salary 
printf("Salary: "); 
scanf("%d",&p[i].salary); 
p[i].salary = p[i].salary + 
(80*p[i].salary)/100 + (10*p[i].salary)/100; 
} 
//Displaying Employee details 
printf("-------------- All Employees Details ---------------\n"); 
for(int i=0; i<n; i++){
printf("Name \t: "); 
printf("%s \n",p[i].name); 

printf("Id \t: "); 
printf("%d \n",p[i].id);
 
printf("Salary \t: "); 
printf("%d \n",p[i].salary); 
printf("\n"); 
} 
return 0; 
}

#include<iostream>
#include<fstream>
#include<stdio.h>
using namespace std;
int main()
{
    char fileName[30], ch;
    fstream fp;
    cout<<"Enter the Name of File: ";
    gets(fileName);
    fp.open(fileName, fstream::in);
    if(!fp)
    {
        cout<<"\nError Occurred!";
        return 0;
    }
    cout<<"\nContent of "<<fileName<<":-\n";
    while(fp>>noskipws>>ch)
        cout<<ch;
    fp.close();
    cout<<endl;
    return 0;
}



