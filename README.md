# calculadora-peso-ideal-
irá medir realizar o cálculo para saber se o seu peso está de acordo com sua altura e sexo ( peso x altura)
/*
toUpperCase() ---> maiúsculo
toLowerCase() ---> minúsculo

char sexo;
sexo = ler.nextLine().toUpperCase().charAt(0);   //toLowerCase()
sexo = ler.nextLine().charAt(0);  
/*
//------------------------------------------------------------

sexo == 'M' --->  para homens:   72.7 * altura - 58
sexo == 'F'--->   para mulheres: 62.1 * altura - 44.7 
outro sexo ---> sexo inválido
*/
import java.util.Scanner;
class Main 
{
  public static void main(String[] args) 
  {
    char sexo;
    float alt;
    Scanner ler = new Scanner (System.in);

    System.out.print("Digite seu sexo <F/M>: ");
    sexo = ler.nextLine().toUpperCase().charAt(0);  // toLowerCase() 
    System.out.print("Digite sua altura: ");
    alt = ler.nextFloat();

    if (sexo == 'F')       System.out.printf ("Seu peso ideal é  %.2f \n " , (62.1*alt-44.7));
    else  if (sexo == 'M') System.out.printf ("Seu peso ideal é  %.2f \n " , (72.7*alt-58));
          else             System.out.println("Sexo Inválido!!! ");    
  }
}

