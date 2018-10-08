# Data Science Study
Data Science Course 
/******************************************************************************

                            Online C Compiler.
                Code, Compile, Run and Debug C program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <stdio.h>
#define ACTION_ONE = "1"
#define ACTION_TWO = "2"
#define ACTION_THREE = "3"
#define ACTION_FOUR = "4"
#define ACTION_FIVE = "5"

int main()
{
    char action, convertFrom, convertTo;
    char unit1, unit2
    float conversionFactor, value, result;
    int constant = 0;
    bool terminationStatus = false;
    /* Error handing: 
        > action input
        > conversion input
    */
    while (!terminationStatus)
        while (!terminationStatus) {
            printf("ACTION LIST\n");
            printf("1 for conversion between Kilometer and Mile\n");
            printf("2 for conversion between Meter and Feet\n");
            printf("3 for conversion between Centimetre and Inch\n");
            printf("4 for conversion between Celsius and Fahrenheit\n");
            printf("5 for quit\n");
            printf("Choose an action:");
            // scanf skips over any leading whitespace characters and stops when it en
            // encounters a tab, space, or newline character
            // TEST: if accepts Tabs, spaces, or newlines in second scanf
            scanf("%c", &action);
            
            if ( action == ACTION_ONE ) 
            {
                unit1 = "K";
                unit2 = "M";
                conversionFactor = 1000.0f;
            }
            else if ( action == ACTION_TWO )
            {
                unit1 = "F";
                unit2 = "M";
                conversionFactor = 0.3048f;
            }
            else if ( action == ACTION_THREE)
            {
                unit1 = "I";
                unit2 = "C";
                conversionFactor = 2.54f;
            }
            else if ( action == ACTION_FOUR ) 
            {
                unit1 = "F";
                unit2 = "C";
                conversionFactor = 9.0f/5.0f;
                constant = 32;
            }
            else if ( action == ACTION_FIVE )
            {
                printf("Goodbye!\n");
                terminationStatus = true;
                break;
            }
            else 
            {
                printf("Incorrect input. Please try again.\n")
                continue;
            }
            break;
        }
        while (!terminationStatus) {
            printf("Enter the unit you would like to convert from (%c or %c): ", unit1, unit2);
            scanf("%c", &toupper(convertFrom));
            if (convertFrom != unit1 && convertFrom != unit2) 
            {
                printf("Incorrect input. Please try again.\n");
                continue;
            }
            printf("Enter the value you would like to convert: ");
            scanf("%f", &value);
            if (convertFrom == unit1)
            {
                convertTo = unit2;
                result = value * conversionFactor;
            }
            else 
            {
                convertFrom 
                result = value / conversionFactor;
                constant = constant * -1 / conversionFactor;
            }
            if (action == ACTION_FOUR) {
                result = result + constant;   
            }
            printf("The result of your conversion is %f", result);
        }
    return 0;
}
