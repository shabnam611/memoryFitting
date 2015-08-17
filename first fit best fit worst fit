#include<stdio.h>
#include<math.h>
#include<string.h>
int pos,mem,by,memory[10],byte[10],i,j,k,ans,temp,best,ok;
void firstfit()
{
    pos=0;
    printf("enter the number of memory size: \n");
    scanf("%d", &mem);
    printf("enter the number of byte size: \n");
    scanf("%d", &by);
    printf("enter the memory array: ");
    for(i=0;i<mem;i++)
    {
        scanf("%d", &memory[i]);
    }

    printf("enter the byte array: \n");
    for(i=0;i<by;i++)
    {
        scanf("%d", &byte[i]);
    }

    for(i=0;i<by;i++)
    {
        ok=0;
        for(j=0;j<mem;j++)
        {

              if((memory[j]>=byte[i])&&(ok==0))
               {
                   memory[j]=memory[j]-byte[i];
                    ok=1;
                    //printf("memory %d  ok %d\n", memory[j],ok);
               }
        }
    }
    printf ("so the final memory array is: \n");
    for(i=0;i<mem;i++)
    {
        printf("%d ", memory[i]);
    }
    for(i=0;i<mem;i++)
    {
        memory[i]=0;
    }
    for(i=0;i<by;i++)
    {
       byte[i]=0;
    }

}

void bestfit()
{
    pos=0;
    printf("enter the number of memory size: \n");
    scanf("%d", &mem);
    printf("enter the number of byte size: \n");
    scanf("%d", &by);
    printf("enter the memory size: ");
    for(i=0;i<mem;i++)
    {
        scanf("%d", &memory[i]);
    }
    printf("enter the byte size: \n");
    for(i=0;i<by;i++)
    {
        scanf("%d", &byte[i]);
    }
    for(i=0;i<by;i++)
    {
        for(j=0;j<mem;j++)
        {
            if(byte[i]<=memory[j])
            {
                if(j==0)
                {
                     best=memory[j]-byte[i];
                     pos=0;
                }
                else
                {
                    temp=memory[j]-byte[i];
                    if(best>temp)
                    {
                        best=temp;
                        pos=j;
                        //memory[j]=memory[j]-byte[i];
                    }
                }
            }
        }
        memory[pos]=best;
        best=0;
        temp=0;
    }
    for(i=0;i<mem;i++)
    {
        printf("%d ", memory[i]);
    }
}

void worstfit()
{
    pos=0;
    printf("enter the number of memory size: \n");
    scanf("%d", &mem);
    printf("enter the number of byte size: \n");
    scanf("%d", &by);
    printf("enter the memory size: ");
    for(i=0;i<mem;i++)
    {
        scanf("%d", &memory[i]);
    }
    printf("enter the byte size: \n");
    for(i=0;i<by;i++)
    {
        scanf("%d", &byte[i]);
    }
    for(i=0;i<by;i++)
    {
        for(j=0;j<mem;j++)
        {
            if(byte[i]<=memory[j])
            {
                if(j==0)
                {
                     best=memory[j]-byte[i];
                }
                else
                {
                    temp=memory[j]-byte[i];
                    if(best<temp)
                    {
                        pos=j;
                        best=temp;
                        //memory[j]=memory[j]-byte[i];
                    }
                }
            }
        }
        memory[pos]=best;
        //printf("%d ", memory[pos]);
        best=0;
        temp=0;
    }
    for(i=0;i<mem;i++)
    {
        printf("%d ", memory[i]);
    }
}

int main()
{
    firstfit();
    bestfit();
    worstfit();
}
//done by Mushrit Shabnam
