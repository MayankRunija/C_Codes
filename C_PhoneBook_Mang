#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<stdlib.h>
#include<windows.h>
struct details
{
    char name[35];
    char adds[50];
    char fname[35];
    char mname[30];
    long int MB_no;
    char gender[8];
    char email[100];
    char ID_no[20];
};
void menu();
void scan();
void start();
void back();
void add_data();
void list_data();
void modify_data();
void delete_data();
void search_data();
int main()
{
    system("color 5f");
    start();
    return 0;
}
void back()
{
    start();
}
void start()
{
    menu();
}
void menu()
{
    system("cls");
printf("\n\t\tWELCOME TO PHONEBOOK");

printf("\n\n\t\t\t  MENU\t\t\n\n");
printf("\t1.Add New   \t2.List   \t3.Exit  \n\t4.Modify \t5.Search\t6.Delete");

switch(getch())
{
    case '1':add_data();
    break;
    
	case '2': list_data();
    break;
    
	case '3': exit(0);
    break;
    
	case '4': modify_data();
    break;
    
	case '5': search_data();
    break;
    
	case '6': delete_data();
    break;
    
	default:system("cls");
            printf("\nEnter 1 to 6 only");
            printf("\n Enter any key");
            getch();
			menu();
        }
    }
        void add_data()
     {
        system("cls");
        FILE *f;
        struct details p;
        f=fopen("project","ab+");
     
	    printf("\n Enter name: ");
        scan(p.name);
     
	    printf("\nEnter the address: ");
        scan(p.adds);
     
	    printf("\nEnter father name: ");
        scan(p.fname);
     
	    printf("\nEnter mother name: ");
        scan(p.mname);
     
	    printf("\nEnter phone no.:");
        scanf("%ld",&p.MB_no);
     
	    printf("Enter gender:");
        scan(p.gender);
        printf("\nEnter e-email:");
        scan(p.email);
        
		printf("\nEnter citizen no:");
        scan(p.ID_no);
        fwrite(&p,sizeof(p),1,f);

      fflush(stdin);
      printf("\nrecord saved");
	  fclose(f);

    printf("\n\nEnter any key");
	getch();
    system("cls");
    menu();
}

void list_data()
{
    struct details p;
    FILE *f;
    f=fopen("project","rb");

 if(f==NULL)
 {
   printf("\nfile opening error in listing :");
   exit(1);
 }

 while(fread(&p,sizeof(p),1,f)==1)
 {
    printf("\n\n\n YOUR RECORD IS\n\n ");
    printf("\nName=%s\nAdress=%s\nFather name=%s\nMother name=%s\nMobile no=%ld\ngender=%s\nE-email=%s\nCitizen no=%s",p.name,p.adds,p.fname,p.mname,p.MB_no,p.gender,p.email,p.ID_no);

	getch();
	system("cls");
 }
    fclose(f);
    printf("\n Enter any key");
    getch();
    system("cls");
    menu();
   }

void search_data()
{
    struct details p;
    FILE *f;
    char name[100];
    f=fopen("project","rb");

if(f==NULL)
{
    printf("\n error in opening\a\a\a\a");
    exit(1);
}

printf("\nEnter name of person to search\n");
scan(name);

while(fread(&p,sizeof(p),1,f)==1)
{
    if(strcmp(p.name,name)==0)
    {
        printf("\n\tDetail Information About %s",name);
        printf("\nName:%s\naddress:%s\nFather name:%s\nMother name:%s\nMobile no:%ld\ngender:%s\nE-email:%s\nCitision no:%s",p.name,p.adds,p.fname,p.mname,p.MB_no,p.gender,p.email,p.ID_no);
    }
        else
        printf("file not found");

}
    fclose(f);
    printf("\n Enter any key");
	getch();
    system("cls");
	menu();
}

void delete_data()
{
    struct details p;
    FILE *f,*ft;
	int flag;
	char name[100];
	f=fopen("project","rb");
	if(f==NULL)
  {
    printf("CONTACT'S DATA NOT ADDED YET.");
  }
	else
	{
		ft=fopen("temp","wb+");
		if(ft==NULL)
		printf("file opaning error");
		else
	{
	    printf("Enter CONTACT'S NAME:");
		scan(name);
		fflush(stdin);
		while(fread(&p,sizeof(p),1,f)==1)
		{
			if(strcmp(p.name,name)!=0)
				fwrite(&p,sizeof(p),1,ft);
			if(strcmp(p.name,name)==0)
                flag=1;
		}
	fclose(f);
	fclose(ft);
	if(flag!=1)
	{
		printf("NO CONACT'S RECORD TO DELETE.");
		remove("temp.txt");
	}
		else
		{
			remove("project");
			rename("temp.txt","project");
			printf("RECORD DELETED SUCCESSFULLY.");

		}
	}
}
     printf("\n Enter any key");
	 getch();
     system("cls");
	 menu();
}

void modify_data()
{
    int c;
    FILE *f;
    int flag=0;
    struct details p,s;
	char  name[50];
	f=fopen("project","rb+");
	if(f==NULL)
		{
		  printf("CONTACT'S DATA NOT ADDED YET.");
		  exit(1);
		}
	else
	{
	    system("cls");
		printf("\nEnter CONTACT'S NAME TO MODIFY:\n");
            scan(name);
            while(fread(&p,sizeof(p),1,f)==1)
            {
                if(strcmp(name,p.name)==0)
                {
				printf("\n Enter name:");
                scan(s.name);
                printf("\nEnter the adds:");
                scan(s.adds);
                printf("\nEnter father name:");
                scan(s.fname);
                printf("\nEnter mother name:");
                scan(s.mname);
                printf("\nEnter phone no:");
                scanf("%ld",&s.MB_no);
                printf("\nEnter gender:");
                scan(s.gender);
                printf("\nEnter e-email:");
                scan(s.email);
                printf("\nEnter citizen no\n");
                scan(s.ID_no);
                fseek(f,-sizeof(p),SEEK_CUR);
                fwrite(&s,sizeof(p),1,f);
                flag=1;
                    break;
			}
                fflush(stdin);
		}
            if(flag==1)
            {
                printf("\n your data id modified");
			}
            else
            {
                    printf(" \n data is not found");
			}
            fclose(f);
	}
	 printf("\n Enter any key");
	 getch();
	 system("cls");
	 menu();
}

void scan(char *name)
{ 
    int i=0,j;
    char c,ch;
    do
    {
	  c=getch();
    
	if(c!=8&&c!=13)
    {
        *(name+i)=c;
        putch(c);
        i++;
    }
        if(c==8)
        {
            if(i>0)
        {
            i--;
        }
                   // printf("h");
        system("cls");
    for(j=0;j<i;j++)
    {
        ch=*(name+j);
        putch(ch);
        }
    }
    }while(c!=13);
      *(name+i)='\0';
  }
