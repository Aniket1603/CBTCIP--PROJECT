\\STUDENT MANAGEMENT SYSTEM
#include<iostream>
using namespace std;
string arr1[20],arr2[20],arr3[20],arr4[20],arr5[20];
int total=0;
void enter()
{
int choice;
cout<<"How many students do you want to enter";
cin>>choice;
if(total==0)
{
total=total+choice;
for(int i =0;i<choice;i++)
{
    cout<<"\nEnter data of student : "<<i+1<<endl<<endl;
    cout<<"\nEnter name: ";
    cin>>arr1[i];
     cout<<"\nEnter Roll no: ";
    cin>>arr2[i];
     cout<<"\nEnter cource: ";
    cin>>arr3[i];
     cout<<"\nEnter  class: ";
    cin>>arr4[i];
     cout<<"\nEnter contact: ";
    cin>>arr5[i];
}
}
else{
    for(int i =total;i<total+choice;i++)
{
    cout<<"\nEnter data of student : "<<i+1<<endl<<endl;
    cout<<"\nEnter name: ";
    cin>>arr1[i];
     cout<<"\nEnter Roll no: ";
    cin>>arr2[i];
     cout<<"\nEnter cource: ";
    cin>>arr3[i];
     cout<<"\nEnter  class: ";
    cin>>arr4[i];
     cout<<"\nEnter contact: ";
    cin>>arr5[i];
}
total=total+choice;
}
}
void show()
{
    if(total==0)
    {
        cout<<"No data is entered"<<endl;
    }
    else{

    
for(int i =0;i<total;i++)
{
    cout<<"Data of student : "<<i+1<<endl<<endl;
    cout<<"Name :"<<arr1[i]<<endl;
    cout<<"Roll no :"<<arr2[i]<<endl;
    cout<<"Cource :"<<arr3[i]<<endl;
    cout<<"Class :"<<arr4[i]<<endl;
    cout<<"Contact :"<<arr5[i]<<endl;
}
}
}
void search()
{
    if(total==0)
    {
        cout<<"No data is entered"<<endl;
    }
    else{
    string rollno;
cout<<"Enter Roll no of student which you want to search";
cin>>rollno;
for(int i =0;i<total;i++)
{
    if(rollno==arr2[i])
    {
     cout<<"Data of student : "<<i+1<<endl<<endl;
    cout<<"Name :"<<arr1[i]<<endl;
    cout<<"Roll no :"<<arr2[i]<<endl;
    cout<<"Cource :"<<arr3[i]<<endl;
    cout<<"Class :"<<arr4[i]<<endl;
    cout<<"Contact :"<<arr5[i]<<endl;   
    }
}
}
}
void update()
{
    if(total==0)
    {
        cout<<"No data is entered"<<endl;
    }
    else{
string rollno;
cout<<"Enter Roll no of student which you want to update ";
cin>>rollno;
for(int i =0;i<total;i++)
{
    if(rollno==arr2[i])
    {
        cout<<"---------Previous Data"<<endl<<endl;
     cout<<"Data of student : "<<i+1<<endl<<endl;
    cout<<"Name :"<<arr1[i]<<endl;
    cout<<"Roll no :"<<arr2[i]<<endl;
    cout<<"Cource :"<<arr3[i]<<endl;
    cout<<"Class :"<<arr4[i]<<endl;
    cout<<"Contact :"<<arr5[i]<<endl; 
    cout<<"---------Enter New Data"<<endl<<endl;
    cout<<"\nEnter name: ";
    cin>>arr1[i];
     cout<<"\nEnter Roll no: ";
    cin>>arr2[i];
     cout<<"\nEnter cource: ";
    cin>>arr3[i];
     cout<<"\nEnter  class: ";
    cin>>arr4[i];
     cout<<"\nEnter contact: ";
    cin>>arr5[i];
    }
}
}
}
void deleterecord()
{
    if(total==0)
    {
        cout<<"No data is entered"<<endl;
    }
    else{
    int a;
    cout<<"press 1 to delete full record"<<endl;
    cout<<"press 2 to delete specific record"<<endl;
    cin>>a; 
    if(a==1)
    {
        total=0;
        cout<<"All record is deleted"<<endl;
    }
    else(a == 2);
    {
        string rollno;
        cout<<"enter the rollno which you want to delete"<<endl;
        cin>>rollno;
        for( int i=0;i<total;i++)
        {
            if(rollno==arr2[i])
            {
                for(int j=i;j<total;j++)
                {
                    arr1[j]=arr1[j+1];
                     arr2[j]=arr2[j+1];
                      arr3[j]=arr3[j+1];
                       arr4[j]=arr4[j+1];
                        arr5[j]=arr5[j+1];

                }
                total--;
                cout<<"Your required record is deleted"<<endl;
            }
        }
    }
}
}
main()
{
    
int value;
cout<<"....................................................";
cout<<"\n\n\t\t\t\*** STUDENT MANAGEMENT SYSTEM ***"<<endl;
cout<<"...................................................."<<endl;
cout<<"______________________________________________"<<endl;
cout<<"______________________________________________"<<endl;
while(true)
{
    cout<<"\t\t\t1. Enter data"<<endl;
    cout<<"\t\t\t2. Show data"<<endl;
    cout<<"\t\t\t3. Search data"<<endl;
    cout<<"\t\t\t4. Update data"<<endl;
    cout<<"\t\t\t5. Delete data"<<endl;
    cout<<"\t\t\t6. Exit"<<endl;
     cout<<"__________________________________________"<<endl;
      cout<<"\t\t\tEnter Your Choice"<<endl;
    cin>>value;
    switch(value)
    {
        case 1:
        enter();
        break;
        case 2:
        show();
        break;
        case 3:
        search();
        break;
        case 4:
        update();
        break;
        case 5:
        deleterecord();
        break;
        case 6:
        exit(0);
        break;
        default:
        cout<<"Invalid input"<<endl;
        break;
    }
}
};
