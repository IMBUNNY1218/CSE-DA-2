# CSE-DA-2

#include <stdio.h>
int sumOfDigits(int n) {
 int sum = 0;
 while (n > 0) {
 sum += n % 10;
 n /= 10;
 }
 return sum;
}
int main() {
 int sum = 0;
 for (int i = 1000; i <= 9998; i += 2) {
 sum += i;
 }
 while (sum > 9) {
 sum = sumOfDigits(sum);
 }
 if (sum % 2 == 0) {
 printf("Even found\n");
 } else {
 printf("Odd found\n");
 }
 return 0;
}
>>>>> G3
#include <stdio.h>
#include <string.h>
int main()
{
 char password[] = "aeiceg";
 char input[3][3];
 char diagonal[5];
 int i, j, k = 0;

 printf("Enter the input characters:\n");
 for(i=0; i<3; i++)
 {
 for(j=0; j<3; j++)
 {
 scanf(" %c", &input[i][j]);
 }
 }

 diagonal[k++] = input[0][0];
 diagonal[k++] = input[1][1];
 diagonal[k++] = input[2][2];
 diagonal[k++] = input[0][2];
 diagonal[k] = input[2][0];

 if(strcmp(diagonal, password) == 0)
 {
 printf("Password matched. The locker is opened successfully.\n");
 }
 else
 {
 printf("Password not matched. The locker cannot be opened.\n");
 }

 return 0;
} 
