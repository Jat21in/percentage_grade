# percentage_grade
#include<stdio.h>
float percentage(float m1,float m2, float m3 , float m4 , float m5);
float total(float m1,float m2, float m3,float m4, float m5);
float main() {
   printf("****************** Welcome To Program To Display Student's Total Marks in 5 Subjects , Percentage and Grade *************************");
    printf("\n");
    char studentname[100] ;
    char studentclass[3];
    int rollno ;
    
    float m1;float m2; float m3; float m4; float m5;
    printf("Enter Student's Name :");
    fgets(studentname, 100 , stdin);

    printf("Enter Class :");
    fgets(studentclass , 3 ,stdin);
   
   printf("Enter Roll Number :");
   scanf("%d/n",& rollno);
    
    printf(" Enter Marks in 3 Subjects :\n");
    printf(" Marks in 1st Subjects :");
    scanf("%f/n",&m1);
    printf(" Marks in 2nd Subjects :");
     scanf("%f/n",&m2);
    printf(" Marks in 3rd Subjects :");
     scanf("%f/n",&m3);
    printf(" Marks in 4th Subjects :");
     scanf("%f/n",&m4);
    printf(" Marks in 5th Subjects :");
     scanf("%f/n",&m5);
   float t =total(m1,  m2,  m3, m4 , m5);
   printf("Total Marks of Student is :%f\n",t);
   float p =percentage(m1,  m2,  m3, m4,m5);
   printf("Percentage of Student is :%f\n",p);


    if(p >= 95 )
      printf("Grade : A+");
    else if ((p >=85 ) && (p < 95))
      printf("Grade : A");
    else if ((p>=75 ) && (p< 85))
      printf("Grade : B");
    else if ((p >=55 ) && (p< 75))
      printf("Grade : C");
    else if ((p >=40 ) && (p < 55))
      printf("Grade : D");
    else 
       printf("Grade : E");

}
 float total(float m1, float m2, float m3,float m4, float m5) {
  return m1+m2+m3+m4+m5 ;

}

float percentage(float m1, float m2, float m3,float m4,float m5) {
  float p = ((m1+m2+m3+m4+m5)/5) ;
  return p;
}
