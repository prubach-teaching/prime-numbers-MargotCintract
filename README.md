# CP_2020_HW1

Please write a program that will print the first n prime numbers separated by comma and space. The output should look like this:
n = 4
2, 3, 5, 7

import java.util.Scanner;

public class homework{
  public static void main(String[] args){
    Scanner s=new Scanner(System.in);
    boolean tab[]=new boolean[100];
    int sum=0;
    
    for(int i=0;i<100;i++){
      tab[i]=false;
    }
    
    for(int l=2;l<100;l++){
      if(tab[l]==false){
        for(int j=l+1;j<100;j++){
          if(j%l==0){tab[j]=true;
        }
      }
    }
      
    System.out.println("How many first prime numbers do you want?");
    int n=Integer.valueOf(s.nextLine());
    System.out.println("n = "+n);
    
    if(n>=1){
      System.out.print("2");
    }
    
    for(int p=3;p<100;p++){
      if(sum<n-1){
        if(tab[p]==false){
          System.out.print(" ,"+p);
          sum=sum+1;
        }
      }
    }
  }
}
