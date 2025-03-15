package maiornumero;

import javax.swing.JOptionPane;

public class MaiorNumero {

    public static void main(String[] args) {
        
        // Criar um vetor com 10 elementos
        double[] numeros = new double[10];

        // Solicitar ao usuário que insira os 10 números
        for (int i = 0; i < 10; i++) {
            String input = JOptionPane.showInputDialog("Digite o " + (i + 1) + "º número:");
            try {
                // Armazenar o número no vetor após convertê-lo para double
                numeros[i] = Double.parseDouble(input);
            } catch (NumberFormatException e) {
                JOptionPane.showMessageDialog(null, "Entrada inválida. O programa será encerrado.");
                return;
            }
        }

        // Encontrar o maior número no vetor
        double maiorNumero = numeros[0]; // Assumimos que o primeiro número é o maior inicialmente

        for (int i = 1; i < 10; i++) {
            if (numeros[i] > maiorNumero) {
                maiorNumero = numeros[i]; // Atualizamos o maior número
            }
        }

        // Exibir o maior número encontrado
        JOptionPane.showMessageDialog(null, "O maior número inserido é: " + maiorNumero);
    }
}
