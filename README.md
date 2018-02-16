# Lab03
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define COLS 9
int main()
{
    int m[][COLS] = {
        {0,0,0,0,1,0,0,0},
        {0,0,0,1,0,1,0,0},
        {0,0,1,0,0,0,1,0},
        {0,1,0,1,0,1,0,1}
    };
    
    
    int *pi = *m;
    int i, mn = sizeof(m)/sizeof(int);
    for (i = 0; i < mn; ++i, ++pi)
    {
        printf("%6d%c", *pi, (i+1) % COLS ? '\t' : '\n');
    }

    return 0;
}
