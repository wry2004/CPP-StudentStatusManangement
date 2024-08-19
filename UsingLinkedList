#include<iostream>
#include<iomanip>
#include<string>
#include<cstring>
using namespace std;
int choice,i=0,n=1;
struct student {
    string ids;
    int id;
    int cla;
    string nam;
    float sco1;
    float sco2;
    float sco3;
    float zsco;
    int mark;
    struct student *next;
};
void xuanze(int choice,struct student *head);
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
void input(struct student *head)
{
    struct student *p1,*p2;
    p1=p2=new struct student;
    while(choice==1)
    {
        cout<<"Id ";
        cin>>p1->id;
        cout<<"class ";
        cin>>p1->cla;
        cout<<"name ";
        cin>>p1->nam;
        cout<<"score1 ";
        cin>>p1->sco1;
        cout<<"score2 ";
        cin>>p1->sco2;
        cout<<"score3 ";
        cin>>p1->sco3;
        p1->mark=1;
        p1->zsco=(p1->sco1+p1->sco2+p1->sco3);
        p1->ids=to_string(p1->id);
        if(n==1)head=p1;
        else p2->next=p1;
        p2=p1;
        cout<<"continue?(yes/no)"<<endl;
        string rep;
        cin>>rep;
        if(rep=="yes")choice=1;
        if(rep=="no")break;
        n++;
        p1=new struct student;
    }
    p2->next=NULL;
    caidan(&choice);
    xuanze(choice,head);
}
void del(struct student *head,int choice)
{
    struct student *p,*p1,*p2;
    p1=head;
    p2=head;
    p=head;
    while(choice==2)
    {
        int nn=0;
		cout<<"Input id or name."<<endl;
        string shu;
        cin>>shu;
        while(p1->next!=NULL)
        {
            if(shu==p1->nam||shu==p1->ids&&nn==0)
            {
                head=p1->next;
                p1=head;
                p2=head;
            }
            if(shu==p1->nam||shu==p1->ids&&nn!=0)
            {
                p2->next=p1->next;
            }
            p2=p1;
            p1=p1->next;
            nn++;
        }
        if(shu==p1->nam||shu==p1->ids)p2->next=NULL;
        while(p->next!=NULL)
        {
             cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
             p=p->next;
        }
         cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
         cout<<"continue?(yes/no)"<<endl;
         string rep;
         cin>>rep;
         if(rep=="yes")choice=2;
         if(rep=="no")break;
    }
    caidan(&choice);
    xuanze(choice,head);
}
void sel(int choice,struct student *head)
{
    while(choice==3)
    {
        struct student *p;
        p=head;
		cout<<"Input id or class."<<endl;
        int flag=1,shu;
        cin>>shu;
        while(p->next!=NULL)
        {
            if(shu==p->id||shu==p->cla)
            {
                cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
            }
            p=p->next;
        }
        if(shu==p->id||shu==p->cla)
        {
             cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
        }
        cout<<"continue?(yes/no)"<<endl;
        string rep;
        cin>>rep;
        if(rep=="yes")choice=3;
        if(rep=="no")break;
    }
    caidan(&choice);
    xuanze(choice,head);
}
void swapf(float *s1,float *s2)
{
    float tmp=*s1;
    *s1=*s2;
    *s2=tmp;
}
void swapi(int *s1,int *s2)
{
    int tmp=*s1;
    *s1=*s2;
    *s2=tmp;
}
void ord(struct student *head)
{
    struct student *p,*p1,*p2;
    p=head;
    p1=p;
    p2=p1->next;
    for(int b=0;b<n;b++)
    {
        while(p2->next!=NULL)
        {
            if(p1->cla>p2->cla||(p1->cla==p2->cla&&p1->zsco<p2->zsco))
            {
                string t1;
                t1=p1->ids;
                p1->ids=p2->ids;
                p2->ids=t1;
                string t2;
                t2=p1->nam;
                p1->nam=p2->nam;
                p2->nam=t2;
                swapi(&(p1->id),&(p2->id));
                swapi(&(p1->cla),&(p2->cla));
                swapi(&(p1->mark),&(p2->mark));
                swapf(&(p1->sco1),&(p2->sco1));
                swapf(&(p1->sco2),&(p2->sco2));
                swapf(&(p1->sco3),&(p2->sco3));
                swapf(&(p1->zsco),&(p2->zsco));
            }
            p1=p2;
            p2=p2->next;
        }
    }
    while(p->next!=NULL)
    {
        cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
        p=p->next;
    }
    cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
    caidan(&choice);
    xuanze(choice,head);
}
void xuanze(int choice,struct student *head)
{
    if(choice==1)
    {
        input(head);
    }
    if(choice==2)
    {
        del(head,choice);
    }
    if(choice==3)
    {
        sel(choice,head);
    }
    if(choice==4)
    {
        ord(head);
    }
    if(choice==5)
    {
        struct student *p;
        p=head;
        while(p->next!=NULL)
        {
            cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
            p=p->next;
        }
        cout<<fixed<<setprecision(1)<<p->id<<","<<p->cla<<","<<p->nam<<","<<p->sco1<<","<<p->sco2<<","<<p->sco3<<","<<p->zsco<<endl;
        caidan(&choice);
        xuanze(choice,head);
    }
    if(choice==6)return;
}
int main()
{
    struct student *p1,*p2,*head;
    cout<<"1.input"<<endl;
    cout<<"2.delete"<<endl;
    cout<<"3.select"<<endl;
    cout<<"4.order"<<endl;
    cout<<"5.output"<<endl;
    cout<<"6.quit"<<endl;
    cout<<"please input your option"<<endl;
    cin>>choice;
    xuanze(choice,head);
    return 0;
}
