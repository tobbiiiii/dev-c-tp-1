
#include <stdio.h>

int main()
{
    int num, max, position;
    int i;

    i = 0;

    printf("Enter a number (0 to stop): ");
    scanf("%d", &num);

    if (num != 0)
    {
        max = num;
        position = 1;
        i = 1;

        while (num != 0)
        {
            printf("Enter a number (0 to stop): ");
            scanf("%d", &num);

            if (num != 0)
            {
                i++;

                if (num > max)
                {
                    max = num;
                    position = i;
                }
            }
        }

        printf("Largest number = %d\n", max);
        printf("Position = %d\n", position);
    }
    else
    {
        printf("No numbers were entered.\n");
    }

    return 0;
}
