#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>
#include <string.h>
#include <ctype.h>

int main(void)
{
    char string[256];
    unsigned int count = 0;
    bool isInsideWord = false;
    bool isValidWord = false;

    fgets(string, 256, stdin);
    for (size_t i = 0; i < strlen(string); i++)
    {
        if (!isInsideWord && !isspace(string[i]))
        {
            isInsideWord = true;
            isValidWord = true;
        }
        if (isInsideWord && isspace(string[i]))
        {
            isInsideWord = false;
            if (isValidWord)
            {
                count++;
            }
        }
        if (isInsideWord && !isalpha(string[i]))
        {
            isValidWord = false;
        }
    }
    
    if (isValidWord)
    {
        count++;
    }

    printf("%u", count);
}
