
#include <stdio.h>

int main()
{
    long long N, temp;
    long long decimal, power;
    int digit, valid;

    printf("Enter a binary number: ");
    scanf("%lld", &N);

    temp = N;
    decimal = 0;
    power = 1;
    valid = 1;

    if (N < 0)
    {
        valid = 0;
    }

    while (temp > 0)
    {
        digit = temp % 10;

        if (digit != 0 && digit != 1)
        {
            valid = 0;
            break;
        }

        decimal = decimal + digit * power;

        power = power * 2;
        temp = temp / 10;
    }

    if (valid == 1)
    {
        printf("Decimal equivalent = %lld\n", decimal);
    }
    else
    {
        printf("Invalid binary number!\n");
    }

    return 0;
}

            
