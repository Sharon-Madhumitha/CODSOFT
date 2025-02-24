import java.util.Scanner;
class range
{
public int generate(int max,int min)
{
return(int) (Math.random()*(max-min+1)+min);
}
}
public class Number
{
public static void main(String args[])
{
Scanner sc = new scanner(System.in);
range r = new range();
int T = 0;
int W = 0;
while(true)
{
System.out.println("Enter min number of your choice: ");
int min = sc.nextInt();
System.out.println("Ente max number of your choice: ");
int max = sc.nextInt();
sc.nextLine();
int c = r.generate(max,min);
int a = 0;
while(true)
{
System.out.println("Guess a random number between "+min+" and "+max);
int g = sc.nextInt();
a++;
if(g>c)
{
System.out.println("It is greater number");
}
else if(g<c)
{
System.out.println("It is lower number");
}
else
{
System.out.println("Yeah...its Correct guess");
W++;
break;
}
}
T = T+a;
System.out.println("Number of attempts = "+a);
System.out.println("Wins = "+W);
double Winrate = (double)W/T*100;
 System.out.printf("your winrate is %.2f%%\n",winrate);
System.out.println("Do u want to play again (yes/no) ");
String st = sc.next();
if(!st.equalsIgnoreCase("y"))
{
sc.close();
System.exit(0);
}
sc.nextLine();
}
}
}
