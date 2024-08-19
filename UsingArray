#include<iostream>
#include<iomanip>
#include<string>
#include<cstring>
using namespace std;
int choice,i=0,n=1;
struct student {
    char ids[100];
    int id;
    int cla;
    char nam[100];
    float sco1;
    float sco2;
    float sco3;
    float zsco;
    int mark;
};
void xuanze(int choice,struct student stu[]);
void caidan(int *choice)
{
    int t;
    cout<<"1.input"<<endl;
    cout<<"2.delete"<<endl;
    cout<<"3.select"<<endl;
    cout<<"4.order"<<endl;
    cout<<"5.output"<<endl;
    cout<<"6.quit"<<endl;
    cout<<"please input your option"<<endl;
    cin>>t;
    *choice=t;
    return;
}
void input(struct student stu[])
{
    while(choice==1)
    {
         cout<<"Id ";
         cin>>stu[i].id;
         cout<<"class ";
         cin>>stu[i].cla;
         cout<<"name ";
         cin.get();
         cin.getline(stu[i].nam,100);
         cout<<"score1 ";
         cin>>stu[i].sco1;
         cout<<"score2 ";
         cin>>stu[i].sco2;
         cout<<"score3 ";
         cin>>stu[i].sco3;
         stu[i].mark=1;
         stu[i].zsco=stu[i].sco1+stu[i].sco2+stu[i].sco3;
         string t1;
         t1=to_string(stu[i].id);
         strcpy(stu[i].ids,t1.c_str());
         cout<<"continue?(yes/no)"<<endl;
         char rep[100];
         cin.get();
         cin.getline(rep,100);
         if(strcmp(rep,"yes")==0)choice=1;
         if(strcmp(rep,"no")==0)break;
         i++;
         n++;
    }
    caidan(&choice);
    xuanze(choice,stu);
}
void del(struct student stu[],int choice)
{
    while(choice==2)
    {
        char shu[100];
		cout<<"Input ID or name."<<endl;
        cin.get();
        cin.getline(shu,100);
        for(int j=0;j<n;j++)
        {
            if((strcmp(shu,stu[j].nam)==0)||(strcmp(shu,stu[j].ids)==0))
            {
                stu[j].mark=0;
            }
        }
        for(int j=0;j<n;j++)
        {
            if(stu[j].mark)
            {
                cout<<fixed<<setprecision(1)<<stu[j].id<<","<<stu[j].cla<<","<<stu[j].nam<<","<<stu[j].sco1<<","<<stu[j].sco2<<","<<stu[j].sco3<<","<<stu[j].zsco<<endl;
            }
        }
        cout<<"continue?(yes/no)"<<endl;
        char rep[100];
        cin.getline(rep,100);
        if(strcmp(rep,"yes")==0)choice=2;
        if(strcmp(rep,"no")==0)break;
    }
    caidan(&choice);
    xuanze(choice,stu);
}
void sel(int choice,struct student stu[])
{
    while(choice==3)
    {
        for(int j=0;j<n;j++)
        {
            if(stu[j].mark!=0)
            {
                stu[j].mark=1;
            }
        }
		cout<<"Input id or class."<<endl;
        int shu,flag=1;
        cin>>shu;
        for(int j=0;j<n;j++)
        {
            if((shu==stu[j].id||shu==stu[j].cla)&&stu[j].mark!=0)
            {
                stu[j].mark=2;
                flag=0;
            }
        }
        for(int j=0;j<n;j++)
        {
            if(stu[j].mark==2)
            {
                cout<<fixed<<setprecision(1)<<stu[j].id<<","<<stu[j].cla<<","<<stu[j].nam<<","<<stu[j].sco1<<","<<stu[j].sco2<<","<<stu[j].sco3<<","<<stu[j].zsco<<endl;
            }
            if((shu==stu[j].id||shu==stu[j].cla)&&stu[j].mark==0)flag=1;
        }
        if(flag)
        {
            cout<<"there is no eligible student"<<endl;
        }
        cout<<"continue?(yes/no)"<<endl;
        char rep[100];
        cin.get();
        cin.getline(rep,100);
        if(strcmp(rep,"yes")==0)choice=3;
        if(strcmp(rep,"no")==0)break;
    }
    caidan(&choice);
    xuanze(choice,stu);
}
void ord(struct student stu[])
{
    struct student tmp;
    for(int j=0;j<n;j++)
    {
        for(int k=0;k<n-j-1;k++)
        {
            if((stu[k].cla>stu[k+1].cla)||(stu[k].cla==stu[k+1].cla&&stu[k].zsco<stu[k+1].zsco))
            {
                tmp=stu[k];
                stu[k]=stu[k+1];
                stu[k+1]=tmp;
            }
        }
    }
    for(int j=0;j<n;j++)
    {
        if(stu[j].mark!=0)
        {
            cout<<fixed<<setprecision(1)<<stu[j].id<<","<<stu[j].cla<<","<<stu[j].nam<<","<<stu[j].sco1<<","<<stu[j].sco2<<","<<stu[j].sco3<<","<<stu[j].zsco<<endl;
        }
    }
    caidan(&choice);
    xuanze(choice,stu);
}
void xuanze(int choice,struct student stu[])
{
    if(choice==1)
    {
        input(stu);
    }
    if(choice==2)
    {
        del(stu,choice);
    }
    if(choice==3)
    {
        sel(choice,stu);
    }
    if(choice==4)
    {
        ord(stu);
    }
    if(choice==5)
    {
        for(int j=0;j<n;j++)
        {
            if(stu[j].mark)
            {
                cout<<fixed<<setprecision(1)<<stu[j].id<<","<<stu[j].cla<<","<<stu[j].nam<<","<<stu[j].sco1<<","<<stu[j].sco2<<","<<stu[j].sco3<<","<<stu[j].zsco<<endl;
            }
        }
        caidan(&choice);
        xuanze(choice,stu);
    }
    if(choice==6)return;
}
int main()
{
    int nn=100;
    struct student stu[nn];
    cout<<"1.input"<<endl;
    cout<<"2.delete"<<endl;
    cout<<"3.select"<<endl;
    cout<<"4.order"<<endl;
    cout<<"5.output"<<endl;
    cout<<"6.quit"<<endl;
    cout<<"please input your option"<<endl;
    cin>>choice;
    xuanze(choice,stu);
    return 0;
}
