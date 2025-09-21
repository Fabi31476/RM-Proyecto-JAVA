# RM-Proyecto-JAVA
package com.mycompany.calculomc;  
import javax.swing.*;

public class PersonaImc {
    private String Nombre;
    private float Peso;
    private short estatura;
    private byte edad;
    }

    public PersonaImc(String Nombre, float Peso, short estatura, byte edad) {
        this.Nombre = Nombre;
        this.Peso = Peso;
        this.estatura = estatura;
        this.edad = edad;
    }
    
public class CalculoMC {

    public static void main(String[] args) {
        // Pedir datos al usuario con cuadros de diálogo
        String nombre = JOptionPane.showInputDialog("Ingresa tu nombre:");
        String edadStr = JOptionPane.showInputDialog("Ingresa tu edad:");
        String pesoStr = JOptionPane.showInputDialog("Ingresa tu peso en kg:");
        String estaturaStr = JOptionPane.showInputDialog("Ingresa tu estatura en metros:");

        // Convertir datos a números
        int edad = Integer.parseInt(edadStr);
        double peso = Double.parseDouble(pesoStr);
        double estatura = Double.parseDouble(estaturaStr);

        // Calcular IMC
        double imc = peso / (estatura * estatura);

        // Mostrar resultado
        String mensaje = "Hola " + nombre + ", tienes " + edad + " años.\n" +
                         "Según tu peso de " + peso + " kg y tu estatura de " + estatura + " m,\n" +
                         "tu índice de masa corporal es: " + String.format("%.2f", imc);

        JOptionPane.showMessageDialog(null, mensaje, "Resultado IMC", JOptionPane.INFORMATION_MESSAGE);
    }
}
