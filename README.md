# INTRODUCCION A C#

vusing System; using System.Collections.Generic;

namespace myApp { class menu{

  public void iniciar(){ 
      //JUGADORES
    Console.WriteLine("Ingrese un caracter1");
     String player1 = Console.ReadLine();
     Console.WriteLine("su eleccion fue {0}", player1);
     Console.WriteLine("Ingrese un caracter2");
     String player2 = Console.ReadLine();
     Console.WriteLine("su eleccion fue {0}", player2);
    //TABLERO
List<string> primeraFila = new List<string>(new string[] { "1", "2", "3" });
List<string> segundaFila = new List<string>(new string[] { "4", "5", "6" });
List<string> tercerFila = new List<string>(new string[]  { "7", "8", "9" });
foreach(var f1 in primeraFila){
           if(f1==primeraFila[2]){
               Console.Write(f1);
           }
           else{Console.Write(f1+" | ");}
       }
       Console.WriteLine();
       foreach(var f2 in segundaFila){
           if(f2==segundaFila[2]){
               Console.Write(f2);
           }
           else{Console.Write(f2+" | ");}
       }
       Console.WriteLine();
       foreach(var f3 in tercerFila){
           if(f3==tercerFila[2]){
               Console.Write(f3);
           }
           else{
           Console.Write(f3+" | ");
           }
       }
       Console.WriteLine();
    //INICIO DE PARTIDA
            //
    Boolean noEstaOcupado=true;
    while(noEstaOcupado){
    System.Console.WriteLine("Jugador {0} ingrese su eleccion",player1); 
    String eleccion = Console.ReadLine();
    if(primeraFila.Contains(eleccion)){
        for(int i=0;i<primeraFila.Count;i++){
            if(eleccion==primeraFila[i]){
                primeraFila[i]=player1;
                noEstaOcupado=false;
            }
            }

} if(segundaFila.Contains(eleccion)){ for(int i=0;i<segundaFila.Count;i++){ if(eleccion==segundaFila[i]){ segundaFila[i]=player1; noEstaOcupado=false; } }} if(tercerFila.Contains(eleccion)){ for(int i=0;i<tercerFila.Count;i++){ if(eleccion==tercerFila[i]){ tercerFila[i]=player1; noEstaOcupado=false;

                 }
            } 
            }  
    else{
        System.Console.WriteLine("Ese lugar esta ocupado, seleccione otro");
         foreach(var f1 in primeraFila){
           if(f1==primeraFila[2]){
               Console.Write(f1);
           }
           else{Console.Write(f1+" | ");}
       }
       Console.WriteLine();
         
    }
 



    }


class Program
{
    static void Main(string[] args)
    {
        //Console.WriteLine("Hello World!"+ DateTime.Now);
        menu m1 = new menu();
        m1.iniciar();
    }
}

} }
