# Summation-of-Each-electrical-appliance-of-their-consumed-units-using-recursion-function-in-c-
#include <stdio.h>
int powerUsage(int *n);
int main() {
    int appliances = 10;
    int total;
    total = powerUsage(&appliances);
    printf("Total Electricity Usage: %d units\n", total);
    return 0;
}
int powerUsage(int *n) {
    int current = *n;
    int usage;
    if (current == 0) {
        return 0;
    }
    printf("Enter electricity usage for appliance in units %d: ", current);
    scanf("%d", &usage);
    (*n)--;
    return usage + powerUsage(n);
}

