# Hands-on-2

1:
public class Exercicio1 {
    public static void main(String[] args) {
        System.out.println("+\"\"\"\"\"+");
        System.out.println("[| o o |]");
        System.out.println(" |  ^  |");
        System.out.println(" | '-' |");
        System.out.println("+-----+");
    }
}

2:
import java.util.Scanner;

public class Exercicio2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Raio da Terra em km
        double raio = 6371.01;

        // Entrada de dados
        System.out.print("Latitude 1: ");
        double lat1 = Math.toRadians(sc.nextDouble());

        System.out.print("Longitude 1: ");
        double lon1 = Math.toRadians(sc.nextDouble());

        System.out.print("Latitude 2: ");
        double lat2 = Math.toRadians(sc.nextDouble());

        System.out.print("Longitude 2: ");
        double lon2 = Math.toRadians(sc.nextDouble());

        // Fórmula
        double distancia = raio * Math.acos(
                Math.sin(lat1) * Math.sin(lat2) +
                Math.cos(lat1) * Math.cos(lat2) * Math.cos(lon1 - lon2)
        );

        System.out.println("Distância: " + distancia + " km");

        3:

        import java.util.Scanner;

public class Exercicio3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Digite uma string: ");
        String texto = sc.nextLine();

        int letras = 0, espacos = 0, numeros = 0, outros = 0;

        for (int i = 0; i < texto.length(); i++) {
            char c = texto.charAt(i);

            if (Character.isLetter(c)) {
                letras++;
            } else if (Character.isDigit(c)) {
                numeros++;
            } else if (Character.isWhitespace(c)) {
                espacos++;
            } else {
                outros++;
            }
        }

        System.out.println("Letras: " + letras);
        System.out.println("Números: " + numeros);
        System.out.println("Espaços: " + espacos);
        System.out.println("Outros caracteres: " + outros);

        sc.close();
    }
}

4:

import java.util.Scanner;

public class Exercicio4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        char resposta;
        int tentativas = 0;
        boolean acertou = false;

        do {
            System.out.println("\nPergunta:");
            System.out.println("Qual linguagem é amplamente usada para desenvolvimento Android?");
            System.out.println("(a) Python");
            System.out.println("(b) Java");
            System.out.println("(c) C++");
            System.out.println("(d) Ruby");
            System.out.println("(e) PHP");

            System.out.print("Sua resposta: ");
            resposta = sc.next().toLowerCase().charAt(0);

            tentativas++;

            switch (resposta) {
                case 'b':
                    System.out.println("Resposta correta!");
                    System.out.println("Você acertou na tentativa " + tentativas);
                    acertou = true;
                    break;
                case 'a':
                case 'c':
                case 'd':
                case 'e':
                    System.out.println("Resposta incorreta.");
                    break;
                default:
                    System.out.println("Opção inválida.");
            }

        } while (!acertou && tentativas < 3);

        if (!acertou) {
            System.out.println("Resposta incorreta nas 3 tentativas.");
        }

        sc.close();
    }
}
        sc.close();
    }
}
