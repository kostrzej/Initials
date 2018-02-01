# Initials
Need a solution how to get out of printing "first space" when typing for example: "   Jack Sparrow".
Thanks for help.



#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <ctype.h>

int main(void)
{
    printf("Tell me your full name, please:\n");
    string fullname = get_string();
    printf("%c", toupper(fullname[0]));
    for(int i=0, n = strlen(fullname); i < n ;i++)
    if ((fullname[i] == ' ') && (fullname[i+1] != '\0' && fullname[i+1] != ' '))
    {
            printf("%c", toupper(fullname[i+1]));
            i++;
    }
    printf("\n");

}
