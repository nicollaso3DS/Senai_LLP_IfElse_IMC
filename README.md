# Senai_LLP_IfElse_IMC

import java.util.Scanner;

public class CalculoIMC {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Entrada de dados
        System.out.print("Informe sua altura (em metros): ");
        double altura = Double.parseDouble(scanner.nextLine());

        System.out.print("Informe seu peso (em kg): ");
        double peso = Double.parseDouble(scanner.nextLine());

        // Cálculo do IMC
        double imc = peso / (altura * altura);

        // Interpretação
        String interpretacao;

        if (imc < 18.5) {
            interpretacao = "Abaixo do peso";
        } else if (imc < 25.0) {
            interpretacao = "Peso normal";
        } else if (imc < 30.0) {
            interpretacao = "Sobrepeso";
        } else {
            interpretacao = "Obesidade";
        }

        // Saída
        System.out.printf("Seu IMC é: %.2f%n", imc);
        System.out.println("Interpretação: " + interpretacao);
    }
}
