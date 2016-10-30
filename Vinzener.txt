#include <cs50.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <ctype.h>

int main(int argc,string agv[])

{

if(argc!=2)

{

printf("Try again.");

return 1;

}

int k;

k=atoi(argv[1]);

string p= GetString();
for (int i=0, n=strlen(p); i<n; i++)

{

if (p[i]> 'A' && p[i]<='Z')

{

p[i]=(p[i]-65+k)%26;

p[i]=(p[i]+65);

}else

if(p[i]>='a' && p[i]<='z')

{

p[i]=(p[i]-97+k)%26;

p[i]=(p[i]+97);

}

}

printf("%s\n",p);

}