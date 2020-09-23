<div align="center">

## A password program with a small difference


</div>

### Description

Yet another password program!! This one takes into account the backspace key, a feature which i didn't find in the other password programs on this site.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Shahab Faruqi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/shahab-faruqi.md)
**Level**          |Intermediate
**User Rating**    |3.0 (9 globes from 3 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__3-14.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/shahab-faruqi-a-password-program-with-a-small-difference__3-2549/archive/master.zip)

### API Declarations

```
#include<iostream.h>
#include<conio.h>
```


### Source Code

```
#include<iostream.h>
#include<conio.h>
void main()
{
clrscr();
cout<<"Enter password: \n";
restart:int x[100],x1[100],i,j=0,k=0,l;
for(i=0;i<=100;i++)
  {
  shahab:l=getch();
  if(((l>=48)&&(l<=126))||(l==8)||(l==13))x[i]=l;
  else goto shahab;
  if(x[i]==13)break;
  else if(x[i]==8)
      {
      gotoxy(1,2);
      clreol();
      for(i=0;i<100;i++)
      x[i]='\0';
      goto restart;
      }
  else
    {
    cout<<"*";
    k++;
    }
  }
cout<<"\nRe enter password: \n";
for(i=0;i<=k;i++)
  {
  x1[i]=getche();
  if(x1[i]==13)break;
  }
for(i=0;i<=k;i++)
if(x[i]!=x1[i])j++; if(j==0)cout<<"\nPasswords match!!\n";
else cout<<"\nPasswords do not match!!\n";
getch();
}
```

