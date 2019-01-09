# cs509-2019-x-mario-less

#include <cs50.h>
#include <stdio.h>
int get_integer (void);
void print_pyramid (int n);

int main(void)
{
    int n = get_integer ();
    printf("Great! \n");
    print_pyramid (n);
}

// Declare function print_pyramid
void print_pyramid (int n)
{
    //Print all rows
    for (int i=1; i<n+1; i++)
    {

        //Print Spaces
        for (int k=1; k<n-i+30; k++)
        {
            printf(" ");
        }

        //Print each row
        for (int j=1; j<i+1; j++)
        {
            printf("#");
        } printf("\n");
    }
    printf("\n");
}

// Declare get_integer
int get_integer (void)
{
    int n= get_int("positive integer [1,8]: ");
    // Check condition
    while (n<1 || n>8)
    {
        if (n>8)
        {
            printf ("Too big \n");
        }
        else
        {
            printf ("Too small \n");

        }
    int y= get_int("Try again:");
    n = y;
    }   return(n);
}
