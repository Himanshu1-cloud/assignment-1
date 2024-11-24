# assignment-1
/ question 1 xWAP to check number is armstrong or not

#include<stdio.h>

#include<math.h>

int main(){

int n,original,r,digits=0,sum=0; 

printf("enter number:"); 

scanf("%d",&n); 

original=n; 
while(original>0){

original/=10; 

digits++; 
}

original=n;

while(original>0){

r=original%10; 

sum+=(int)pow(r,digits); 

original/=10; 
}

if(sum==n){

printf("%d is armstrong number",n); 
}

else{

printf("%d is not armstrong number",n); 
}

return 0;

}

//wap to read two integers and print hcf

#include<stdio.h>

#include<math.h>

int main(){

int n1,n2,min,hcf; 

printf("enter two numbers:"); 

scanf("%d %d",&n1,&n2); 

min=(n1<n2)?n1:n2; 

for(int i=1;i<=min;i++){ 

    if(n1%i==0 && n2%i==0){ 

        hcf=i; 

    } 

} 

printf("hcf of %d and %d is %d\n",n1,n2,hcf); 

return 0; 
}

// queation3 wap to subtract two integers without minus operator(bitwise operator)

#include<stdio.h>

int main(){

int a,b; 

printf("enter a and b:"); 

scanf("%d %d",&a,&b); 

while(b!=0){ 

int udhar=(~a)&b; 

a=a^b; 

b=udhar<<1; 

} 

printf("the result of subtraction is %d\n",a); 

return 0; 
}

//wap to to swap two numbers 1 st method

#include<stdio.h>

int main(){

int n1,n2,temporary_variable; 

printf("enter n1,n2:"); 

scanf("%d %d",&n1,&n2); 

temporary_variable=n1; 

n1=n2;  
n2=temporary_variable;

printf("numbers after swapping is %d and %d\n",n1,n2); 

return 0; 
}

//wap to to swap two numbers 2nd method

#include<stdio.h>

int main(){

int n1,n2; 

printf("enter n1,n2:"); 

scanf("%d %d",&n1,&n2); 

n1=n1+n2; 

n2=n1-n2; 

n1=n1-n2; 

printf("number after swapping is %d and %d\n",n1,n2); 

return 0; 
}

//wap to to swap two numbers 3rd method

#include<stdio.h>

int main(){

int n1,n2;

printf("enter n1,n2:");

scanf("%d %d",&n1,&n2);

n1=n1^n2;

n2=n2^n1;

n1=n1^n2;

printf("number after swapping is %d and %d\n",n1,n2);

return 0; 
}

//wap to to swap two numbers 4th method

#include<stdio.h>

int main(){

int n1,n2;

printf("enter n1,n2:");

scanf("%d %d",&n1,&n2);

n1=n1*n2;

n2=n1/n2;

n1=n1/n2;

printf("number after swapping is %d and %d\n",n1,n2);

return 0; 
}

///wap to check number is perfect number or not

#include<stdio.h>

int main(){

int n,sum=0;

printf("enter n:");

scanf("%d",&n);

for(int i=1;i<=n/2;i++){

  if(n%i==0){ 

      sum+=i; 

  } 
}

if(sum==n ){

  printf("%d is perfect number",n); 
}

else{

  printf("%d is not perfect number",n); 
}

return 0; 
}

//wap to determine quadrant for coordinate x and y

#include<stdio.h>

int main(){

int x,y;

printf("enter x and y:");

scanf("%d %d",&x,&y);

if(x>0 && y>0){

 printf("x=%d & y=%d in 1st quadrant",x,y); 
}

else if(x<0 && y>0){

printf("x=%d & y=%d in 2nd quadrant",x,y); 
}

else if(x<0 && y<0){

printf("x=%d & y=%d in 3rd quadrant",x,y); 
}

else if(x>0 && y<0){

printf("x=%d & y=%d in 4th quadrant",x,y); 
}

else if(x=0 && y!=0){

printf("point on y axis y=%d",y); 
}

else if(y=0 && x!=0){

printf("point on x axis",x); 
}

else{

 printf("point on origin"); 
}

return 0; 
}

// converting decimal to binary ,binary to decimal

#include <stdio.h>

#include<math.h>

int binarytodecimal(long long binary);

long long decimaltobinary(int decimal);

int main() {

int choice; 

printf("Enter choice:"); 

//choice=1 binarytodecimal choice=2 decimaltobinary 

scanf("%d",&choice); 

if(choice==1){ 

    long long binary; 

    printf("enter binary "); 

    scanf("%11d",&binary); 

    printf("decimal=%d\n",binarytodecimal(binary)); 

} 

else if(choice==2){ 

    int decimal; 

    printf("enter decimal :"); 

    scanf("%d\n",&decimal); 

    printf("binary=%11d\n",decimaltobinary(decimal)); 

} 

  else{ 

      printf("invalid choice"); 

  } 

  return 0; 
}

  int binarytodecimal(long long binary){ 

      int decimal=0,r,i=0; 

      while(binary!=0){ 

          r=binary%10; 

          decimal+=r*pow(2,i); 

          binary/=10; 

          i++; 

  } 

  return decimal; 

  } 

  long long decimaltobinary(int decimal){ 

      long long binary=0,r,i=1; 

      while(decimal!=0){ 

          r=decimal%2; 

          binary+=r*i; 

          decimal/=2; 

          i*=10; 

      } 

      return binary; 

  } 

  // making pattern of 1;0 1;1 0 1; 0 1 0 1;1 0 1 0 1 
#include <stdio.h>

#include<math.h>

int main(){

int n=5; 

for(int i=1;i<=n;i++){ 

    for(int j=1;j<=i;j++){ 

        if((i+j)%2==0){ 

            printf("1"); 

        } 

        else{ 

            printf("0"); 

        } 

    } 
printf("\n");

}

return 0;

}

// making pattern of 1;0 1;1 0 1; 0 1 0 1;1 0 1 0 1

#include <stdio.h>

#include<math.h>

int main(){

int n=5;// n=number of rows 

for(int i=1;i<=n;i++){ 

    for(int j=0;j<i;j++){ 

        printf("%d",j%2); 

    } 

            printf("  "); 

     

       for(int j=0;j<i;j++){ 

            printf("%d",j%2); 

       } 
printf("\n");

}

return 0;

}

//pascal’s triangle #include <stdio.h> //c =coefficient int main() { int rows, c= 1, space, i, j;

printf("Enter the number of rows: ");
scanf("%d", &rows);

for(i = 0; i < rows; i++) {
    for(space = 1; space <= rows - i; space++)
        printf("  ");

    for(j = 0; j <= i; j++) {
        if (j == 0 || i == 0)
            c = 1;
        else
            c = c* (i - j + 1) / j;

        printf("%4d", c);
    }
    printf("\n");
}

return 0;
} //assignment 2

//question 1

#include <stdio.h>
int main() { int marks[5];

for(int i=0;i<=4;i=i+1) { 
    printf("Enter marks %d :",i+1); 
    scanf("%d",&marks[i]); 
} 
 
printf("\n new list of marks\n"); 

for(int j=0;j<=4;j=j+1) { 
    printf("Final marks of student-%d : %d\n",j+1,marks[j]+5); 
} 
return 0; 
}

//question 2

#include <stdio.h> int main() { int marks[5];

for( int i=0;i<=4;i=i+1) { 
    printf("Enter marks %d :",i+1); 
    scanf("%d",&marks[i]); 
} 

printf("\n list of grade\n"); 

for(i=0;i<=4;i=i+1) { 
    if (marks[i]>=75) 
    printf("Grade-A\n",i+1); 
    else if (marks[i]>=60 && marks[i]<75) 
    printf("Grade-B\n",i+1); 
    else if (marks[i]>=40 && marks[i]<60) 
    printf("Grade-C\n",i+1); 
    else if (marks[i]>=0 && marks[i]<40) 
    printf(" Grade-D\n",i+1); 
    else 
    printf("NOTE--Enter marks on scale of 0-100.\n"); 
} 
return 0; 
}

//question 3

#include <stdio.h>
int main() { int marks[5];

for( int i=0;i<=4;i=i+1) { 
    printf("Enter marks %d :",i+1); 
    scanf("%d",&marks[i]); 
} 

for(i=0;i<=4;i=i+1) { 
    if (marks[i]==99){ 
        printf("Student-%d has scored first 99 marks",i+1); 
        break; 
    } 
} 
return 0; 
}

//question 4

#include <stdio.h>
int main() { int marks[5],sum=0;

for(int =0;i<=4;i=i+1) { 
    printf("Enter marks of student-%d :",i+1); 
    scanf("%d",&marks[i]); 
} 

for( int i=0,sum;i<=4;i=i+1) { 
    if (marks[i]==99){ 
        printf("\nStudent-%d has scored 99 marks",i+1); 
        sum+=1; 
    } 
} 
printf("\n\n%d student's has scored 99 marks",sum); 
return 0; 
}

//question 5

#include <stdio.h>
int main() { int marks[5],sum=0;

for(int i=0;i<=4;i=i+1) { 
    printf("Enter marks of student-%d :",i+1); 
    scanf("%d",&marks[i]); 
} 

for(int i=0,sum;i<=4;i=i+1) { 
    sum=sum+marks[i]; 
} 
printf("\nSum of mark's of all student's is %d",sum); 
}

//question 6

#include <stdio.h> int average (int sum) { int a; a=sum/5; return a; }; int main() { int marks[5],i,sum=0;

for(i=0;i<=4;i=i+1) { 
    printf("Enter marks of student-%d :",i+1); 
    scanf("%d",&marks[i]); 
} 

for(i=0,sum;i<=4;i=i+1) { 
    sum=sum+marks[i]; 
} 
printf("\nSum of mark's of all student's is %d\n",sum); 

printf("Average of total marks is %d",average(sum)); 
return 0; 
}

//question 7

#include <stdio.h> int main() { int score[5];

for(int i=0;i<=4;i=i+1) { 
    printf("Enter score-%d :",i+1); 
    scanf("%d",&score[i]); 
} 

printf("\n"); 

for (i=0;i<=4;i=i+1) { 
    if (score[i]%2==0) 
    printf("Score-%d (%d) is even\n",i+1,score[i]); 
    else 
    printf("Score-%d (%d) is odd\n",i+1,score[i]); 
} 
return 0; 
}

//question 8

#include <stdio.h>

int main() {

int rows, coef = 1, space, i, j; 

 

printf("Enter the number of rows: "); 

scanf("%d", &rows); 



for(i = 0; i < rows; i++) { 

    for(space = 1; space <= rows - i; space++) 

        printf("  "); 



    for(j = 0; j <= i; j++) { 

        if (j == 0 || i == 0) 

            coef = 1; 

        else 

            coef = coef * (i - j + 1) / j; 



        printf("%4d", coef); 

    } 

    printf("\n"); 

} 

 

return 0; 
}

//question 9

#include <stdio.h>

int main() {

int rows, coef = 1, space, i, j; 

 

printf("Enter the number of rows: "); 

scanf("%d", &rows); 



for(i = 0; i < rows; i++) { 

    for(space = 1; space <= rows - i; space++) 

        printf("  "); 



    for(j = 0; j <= i; j++) { 

        if (j == 0 || i == 0) 

            coef = 1; 

        else 

            coef = coef * (i - j + 1) / j; 



        printf("%4d", coef); 

    } 

    printf("\n"); 

} 

 

return 0; 
}

//question 10

#include <stdio.h>

int main() {

int i, j, space, value;

for(i=1; i <= 4; i++) {

for(space = 1; space <= (4-1); space++) {

printf(" ");

}

value = 1;

for(j = 1; j <= 1; j++) { printf("%2d", value);

value = value (ij) / (j);

} //assignment 3

#include <stdio.h> #include <math.h> int main() { int choice,i,digit,num2; float num[20]={0},sum,sub,mult,div,num1,num3;

printf("\t# To add number's enter 1\n"); 
printf("\t# To subtract number's enter 2\n"); 
printf("\t# To multiply number's enter 3\n"); 
printf("\t# To divide number's enter 4\n"); 
printf("\t# To calculate logarithmic value enter 5\n"); 
printf("\t# To calculate square of number's enter 6\n"); 
 
printf("\nEnter your choice :"); 
scanf("%d",&choice); 
 
if (choice!=4 && choice<=6 && choice>=1) { 
printf("\nEnter on how many digit's you want to perform above mentioned operation :"); 
scanf("%d",&digit); 

for(i=0;i<=digit-1;i=i+1) { 
    printf("Enter digit-%d :",i+1); 
    scanf("%f",&num[i]); 
} 
} 
if (choice>=1 && choice<=6) { if (choice==1) { for(i=0,sum=0;i<=digit-1;i=i+1) { sum=sum+num[i]; } printf("Addition of number's is %f\n",sum); } else if (choice==2) { for(i=0,sub=0;i<=digit-1;i=i+1) { sub=sub-num[i]; } printf("Subtraction of number's is %f\n",sub); } else if (choice==3) { for(i=0,mult=1,num;i<=digit-1;i=i+1) { mult=mult*num[i]; } printf("Multiplication of number's is %f",mult); } else if (choice==4) { printf("Enter a number to be divided :"); scanf("%f",&num1); printf("Enter how many time's you want to divide %.2f :",num1); scanf("%d",&num2); for(i=0,div=1;i<=num2-1;i=i+1) { printf("Enter divisor-%d :",i+1); scanf("%f",&num3); div=num1/num3; printf("Divison = %f\n",div); } } else if (choice==5) { for(i=0;i<=digit-1;i=i+1) { printf("Logarithmic value of %.2f is %f\n",num[i],log(num[i])); } } else if (choice==6) { for(i=0;i<=digit-1;i=i+1) { printf("Square of %.2f is %f\n",num[i],num[i]*num[i]); } } } else { printf("# INVALID CHOICE"); } return 0; }

printf("\n"); }

return 0;

} //assignment 4

#include<stdio.h>

int main()

{

char user, comp;

int c, flagA=0, flagB=0,i;

printf("enter 'R' for rock, 's' for Scissor, 'P' for Paper.");

for(int i=0;i<=2;i++)

{

printf("\nenter (R, S, P): ");

scanf("%c", &user);

printf("\nenter no. for computer choice from 0-100:");

scanf("%d", &c);

if(c<=33 && c>=0){

comp='R';

}

else if(c>33 && c<=66){

comp='P';

}

else if(c>66 && c<=100){

comp='S';

}

if (user =='R' && comp==’P'){

printf("\ncomputer wins this round");

flagB++;

}

else if (user=='R' && comp=='S'){

printf("\nuser wins this round");

flagA++;

}

else if (user='R' && comp=='R'){

printf("\nits a tie");

}

else if (user=='P' && comp=='S'){

printf(“\n computer wins this round”);

flagB++;

}

else if (user=='P' && comp=='R') {

printf("\nuser wins this round");

flagA++;

}

else if (use=='S' && comp=='P'){

printf("\nuser wins this round");

flagA++;

}

else if (user=='S' && comp=='S'){

printf("\nits a tie");

}

else if (user=='S' && comp=='R'){

printf("\ncomputer wins this round");

flagB++;

}

}

if(flagA >flagB)

printf("\nUser wins the game");

else if(flagA<flagB)

printf("\nComputer wins the game");

else

printf("\nThe game is a tie");

return 0;

}
//assignment 5

#include <stdio.h>

#include <string.h>

#include <ctype.h>

int main(){

char word [] = "feminine";

char guessed [9] = "________”;

int chances = 3;

char guess;

printf("Welcome to Hangman!\n");

while (chances > 0) {

printf("Word: %s\n", guessed);

printf("Enter your guess: ");

scanf("%c", &guess);

guess =tolower(guess);

int correctGuess = 0;

for (int i = 0; i < strlen(word); i++) {

if (word[i]== guess) {

guessed [i] = guess;

correctGuess = 1;

}

}

if (!correctGuess) {

chances--;

printf("Incorrect! You have %d chances left.\n", chances);

}

if (strcmp(word, guessed) ==0) {

printf("Congratulations! You've guessed the word: %s\n", word:%s\n”,word);

return 0;

}

}

printf("Game over! The word was '%s'.\n", word);

return 0;

}

                                                                                               assignment 6
#include <stdio.h>

void displayBoard(char board[3][3]) { for (int i = 0; i < 3; i++) { for (int j = 0; j < 3; j++) { printf("%c ", board[i][j]); if (j < 2) printf("|"); } printf("\n"); if (i < 2) printf("---------\n"); } printf("\n"); }

int checkWinner(char board[3][3]) { for (int i = 0; i < 3; i++) { if ((board[i][0] == board[i][1] && board[i][1] == board[i][2] && board[i][0] != ' ') || (board[0][i] == board[1][i] && board[1][i] == board[2][i] && board[0][i] != ' ')) { return 1; } } if ((board[0][0] == board[1][1] && board[1][1] == board[2][2] && board[0][0] != ' ') || (board[0][2] == board[1][1] && board[1][1] == board[2][0] && board[0][2] != ' ')) { return 1; } return 0; } int isBoardFull(char board[3][3]) { for (int i = 0; i < 3; i++) { for (int j = 0; j < 3; j++) { if (board[i][j] == ' ') { return 0; } } } return 1; } int makeMove(char board[3][3], int player, int row, int col) { if (board[row][col] == ' ') { board[row][col] = (player == 1) ? 'X' : 'O'; return 1; } return 0; }

int main() { char board[3][3] = {{' ', ' ', ' '}, {' ', ' ', ' '}, {' ', ' ', ' '}}; int row, col; int player = 1;
int gameOver = 0;

printf("Welcome to Tic Tac Toe!\n"); 

while (!gameOver) { 
    displayBoard(board); 

    printf("Player %d (%c), enter your move (row and column): ", player, (player == 1) ? 'X' : 'O'); 
    scanf("%d %d", &row, &col); 

    row--; col--; 

    if (!makeMove(board, player, row, col)) { 
        printf("Invalid move! Try again.\n"); 
        continue; 
    } 

    if (checkWinner(board)) { 
        displayBoard(board); 
        printf("Player %d (%c) wins!\n", player, (player == 1) ? 'X' : 'O'); 
        gameOver = 1; 
    } 
    else if (isBoardFull(board)) { 
        displayBoard(board); 
        printf("It's a draw!\n"); 
        gameOver = 1; 
    } 
     
    player = (player == 1) ? 2 : 1; 
} 

return 0; 
