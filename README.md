package com.mycompany.calculadoraprocesos;

import java.util.Scanner;

public class CalculadoraProcesos {

    public static void main(String[] args) {
    Scanner entrada = new Scanner(System.in);
    
       double numero1;
       double numero2;
       char operacion;
       double resultado = 0;
            
        System.out.print("Ingrese el primer número: ");
        while (!entrada.hasNextDouble()) {
            System.out.println("Entrada invalida");
            entrada.next();
        }
        numero1 = entrada.nextDouble();

        System.out.print("Ingrese el segundo numero: ");
        while (!entrada.hasNextDouble()) {
            System.out.println("Entrada invalida");
            entrada.next();
        }
        numero2 = entrada.nextDouble();
        
        System.out.println("Que tipo de operacion quieres: ");
        System.out.println("+ para suma");
        System.out.println("- para resta");
        System.out.println(" * para multiplicacion");
        System.out.println("/ para division");
        operacion = entrada.next().charAt(0);
        
       
        
        switch (operacion) {
            case '+':
                resultado = numero1 + numero2;
                System.out.println("El resultado de la suma es: " + resultado);
                break;
            case '-':
                resultado = numero1 - numero2;
                System.out.println("El resultado de la resta es: " + resultado);
                break;
            case '*':
                resultado = numero1 * numero2;
                System.out.println("El resultado de la multiplicacion es: " + resultado);
            case '/':
                resultado = numero1 / numero2;
                System.out.println("El resultado de la division es: " + resultado);
                if(numero1 == 0 || numero2 ==0){
                System.out.println("Operacion invalida.");
                }
                break;
            default:
                System.out.println("Operacion invalida.");
                break;
    }
 }
}
