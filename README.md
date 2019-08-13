# IIT-ASSIGNMENT-

import java.util.Scanner;

public class LoadBalancer

 {
static void printLoad (int servers,int Processes)

{

int each = Processes/servers;
int extra = Processes%servers;
int total =0;

for(int i = 0; i<servers; i++)
{

if(extra-->0) total =each+1;
else total = each;
System.out.println("server "+(char)('A'+i)+" has "+total+" Processes");
  }
 }

public static void main(String[] args)
{
 Scanner sc = new Scanner(System.in);
System.out.println("Enter the number of servers and processes:");
int servers= sc.nextInt();
int Processes= sc.nextInt();
while(true){
printLoad(servers, Processes);
System.out.println("1.Add servers 2.Remove Servers 3. Add Processes 4. Remove Processes 5.Exit");

switch(sc.nextInt()){

case 1:
System.out.println("How many more Servers?:");
                    servers+=sc.nextInt();
break;


case 2:
System.out.println("How many Servers to remove?:");
                    servers-=sc.nextInt();
break;


case 3:
System.out.println("How many Processes?:");
                    Processes+=sc.nextInt();
break;


case 4:
System.out.println("How many Processes to remove?:");
                    Processes-=sc.nextInt();
break;


case 5:
return;
            }
        }
    }
}

