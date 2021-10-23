# MEDICAL-MANAGMENT-SYSTEM
Project in Medical Management System : Medical Shop Management System is an application project developed for medical shops. This system is a field concerned with purchasing and selling medicines, maintaining their inventory, generating sales invoices and generating reminders of expiry date about medicines. It requires more time and effort when all procedures are performed manually.



CODE:-
#include<stdio.h>

#include<conio.h>

int main ()

{

int c_id,age,m_id,qty,x;

float cost,t_cost;

char c_name[20],c_type,m_name[20],comp_name[20],s_name[20];

	
	
	printf("Enter The Following Details :-\n");
	printf("Enter The Customer Name\t : ");
	scanf("%s",&c_name);
	printf("Enter The Customer ID\t : ");
	scanf("%d",&c_id);
	printf("Enter The Customer Age\t : ");
	scanf("%d",&age);
	printf("Enter The Customer Type(R/T)\t : ");
	scanf("%c",&c_type);
	printf("Enter the Medicine Name\t : ");
	scanf("%s",&m_name);
	printf("Enter The Medicine ID\t : ");
	scanf("%d",&m_id);
	printf("Enter The Company Name\t : ");
	scanf("%s",&comp_name);
	printf("Enter The Supplier Name\t : ");
	scanf("%s",&s_name);
	printf("Enter cost the Medicine \t : ");
	scanf("%f",&cost);
	printf("Enter Quantity Required\t : ");
	scanf("%d",&qty); 
	 
	  
	
	t_cost=cost*qty;
	if(c_type=='R'||c_type=='r')
	{
		t_cost=t_cost-((10/100)*t_cost);
	}
	else
	{
		t_cost-=((2/100)*t_cost);
    }
    
        
    printf("1. Supplier Information\n2.Customer Information\n3.Medicine\n4.Bill\n");
    printf("Choose Your Option : ");
    scanf("%d",&x);
    
    if(x==1)
    {
	
    	printf("\t\t\t     MEDICAL STORE MANAGEMENT SYSTEM\n");
		printf("Company Name\t : %s\n",comp_name);
		printf("Supplier Name\t : %s\n",s_name);
		
	}
	else if(x==2)
    {
    	printf("\t\t\t     MEDICAL STORE MANAGEMENT SYSTEM\n");
    	printf("Customer Name\t : %s\n",c_name);
		printf("Customer ID\t : %d\n",c_id);
		printf("Customer Age\t : %d\n",age);
		printf("Customer Type\t : %c\n",c_type);
	}
	else if(x==3)
    {
    	printf("\t\t\t     MEDICAL STORE MANAGEMENT SYSTEM\n");
    	printf("Medicine Name\t : %s\n",m_name);
		printf("Medicine ID\t : %d\n",m_id);
	}
	else if(x==4)
    {
    	printf("\t\t\t     MEDICAL STORE MANAGEMENT SYSTEM\n");
    	printf("Cost Per Item\t\t : %f\n",cost);
    	printf("Quantity Required\t : %d\n",qty);
    	printf("Total Cost Of Items\t : %f\n",t_cost);
    }
	else
		printf("Wrong Input\n");
	
		getch();
}
