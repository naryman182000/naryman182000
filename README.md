<!---
naryman182000/naryman182000 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

#include <iostream>
#include <bits/stdc++.h>
using namespace std;
template<class t>
class mylist{
public:
    int sizee;
    myclass(int sizee){
        this->sizee=sizee;

    }
    int getsize(){
        return sizee;
    }
    virtual void addelme()=0;
    virtual t getelme()=0;
    virtual bool isempty()=0;
    virtual bool isfull()=0;
    virtual void clearitem()=0;
    ~mylist(){

    }
};
template<class t>
class mystack : public mylist<t>{
public:
    int sizee;
    t *arr;
    mystack(int sizee){
       t *arr=new t[sizee];
    }
    int counter=0;
    void addelme(t element){
        for(int i=sizee;i>0;i--){
            arr[i]=element;
            counter++;
        }
    }
    t getelme(){
        return arr[sizee];
    }
    bool isempty(){
        if(counter<sizee){
            return true;
        }
        else
            return false;
    }
    bool isfull(){
        if(counter == sizee){
            return true;
        }
        else
            return false;
    }
    ~mystack(){
        delete []arr;
    }

};
class rectangle{
public:

};
template<class t>
class myquee : public mylist<t>{
public:
    int sizee;
    t *arr;
    int counter=0;
    void addelme(t element){
        for(int i=0;i<sizee;i++){
            arr[i]=element;
            counter++;
        }
    }
    bool isempty(){
        if(counter<sizee){
           return true;
        }
        else
            return false;
    }
    bool isfull(){
        if(counter==sizee){
            return true;
        }
        else
            return false;
    }
    t getelme(){
        return arr;
    }
    ~myquee(){
        delete []arr;
    }
};
class rectangle{
    int lengh;
    int width;
public:
    rectangle(){
        width=0;
        lengh=0;
    }
    rectangle(int lengh,int width){
        if(lengh>0){this->lengh=lengh;}
        if(width>0){this->width=width;}
    }
    int getlengh(){
        return lengh;
    }
    int getwidth(){
        return width;
    }
    int getarea(){
        return width*lengh;
    }
    friend ostream& operator<<(ostream& os,const rectangle& re){
        os<<"the lengh is:"<<re.getlengh()<<endl<<"the width is:"<<re.getwidth()<<endl<<"the erea is:"<<re.geterea;
    }

};
int main(){
    return 0;

}
