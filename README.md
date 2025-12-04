# Summation-of-Each-electrical-appliance-of-their-consumed-units-using-recursion-function-in-c-
#include <stdio.h>
int powerUsage(int *n);
int main() {
    int appliances;
    int total;
    printf("How many appliances do you want to enter? ");
    scanf("%d", &appliances);
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
    printf("Enter electricity usage for appliance %d in units: ", current);
    scanf("%d", &usage);
    (*n)--;
    return usage + powerUsage(n);
}

