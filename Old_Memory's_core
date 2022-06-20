#include<stdio.h>
#include<stdlib.h>
int judge_leap_year(int year1){/*判断是不是闰年的函数，如果是，返回1，如果不是返回0*/   
    int judge;    
    if((year1%4==0&&year1%100!=0)||year1%400==0){    
        judge=1;    
    }else{    
        judge=0;    
    }    
    return judge;    
}   
int first_date(int year2){/*判断该年的第一天到底是星期几，从星期日~星期六分别返回0123456*/ 
   
    int this_year_first_date;    
    int judgement=judge_leap_year(year2-1);    
    if(year2==1900){    
        this_year_first_date=1;    
    }else if(year2!=1900&&judgement==0){    
        this_year_first_date=first_date(year2-1)+1;    
    }else if(year2!=1900&&judgement==1){    
        this_year_first_date=first_date(year2-1)+2;         
    }    
        this_year_first_date=this_year_first_date%7;    
    return this_year_first_date;    
}  
int calculatedate(int leap_year,int first,int month,int day){/*传入是不是闰年，并且根据该年第一天的星期，所输入的月份，日期，返回星期数目，从星期日~星期六分别返回0123456*/    
    int num;    
    int feb,date;    
    if(leap_year==1){    
      feb=29;    
    }else{    
      feb=28;       
    }    
    /* the calculation of date*/    
    if(month==1){    
        num=day;    
    }else if(month==2){    
        num=day+31;    
    }else if(month==3){    
        num=day+31+feb;    
    }else if(month==4){    
        num=day+31+feb+31;    
    }else if(month==5){    
        num=day+31+feb+31+30;    
    }else if(month==6){    
        num=day+31+feb+31+30+31;    
    }else if(month==7){    
        num=day+31+feb+31+30+31+30;    
    }else if(month==8){    
        num=day+31+feb+31+30+31+30+31;    
    }else if(month==9){    
        num=day+31+feb+31+30+31+30+31+31;    
    }else if(month==10){    
        num=day+31+feb+31+30+31+30+31+31+30;            
    }else if(month==11){    
        num=day+31+feb+31+30+31+30+31+31+30+31;             
    }else if(month==12){    
        num=day+31+feb+31+30+31+30+31+31+30+31+30;              
    }    
    date=(num-1)%7+first;    
    if(date>=7){    
        date=date-7;    
    }else    
    {    
        /**/    
    }    
    return date;     
} 
int GCD(int n,int m){/*输入两个整数求最大公约数*/  
    int GCDMAX;   
    if(m<=n&&n%m==0){  
        GCDMAX=m;  
    }else if(n<m){  
        GCDMAX=GCD(m,n);  
    }else{  
        GCDMAX=GCD(m,n%m);   
    }  
    return GCDMAX;  
}
int LCM(int n,int m){/*输入两个整数求最小公倍数*/ 
	return n*m/GCD(n,m);
}
