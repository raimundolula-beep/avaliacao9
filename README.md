import java.util.ArrayList;
import java.util.Scanner;

public class Atividade2 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        ArrayList<String> nomes = new ArrayList<>();
        ArrayList<Double> medias = new ArrayList<>();

        System.out.println("----- Sistema Escolar - Atividade 2 -----");

        while (true) {
            System.out.print("Digite o nome do aluno (ou 'sair' para encerrar): ");
            String nome = sc.nextLine();

            if (nome.equalsIgnoreCase("sair")) {
                break;
            }

            System.out.print("Digite a primeira nota: ");
            double n1 = Double.parseDouble(sc.nextLine());

            System.out.print("Digite a segunda nota: ");
            double n2 = Double.parseDouble(sc.nextLine());

            double media = (n1 + n2) / 2;

            nomes.add(nome);
            medias.add(media);

            System.out.println("Aluno cadastrado com sucesso!\n");
        }

        System.out.println("\n===== BOLETIM FINAL =====");
        for (int i = 0; i < nomes.size(); i++) {
            String nome = nomes.get(i);
            double media = medias.get(i);
            String situacao = media >= 7 ? "Aprovado" : "Reprovado";

            System.out.println("\nAluno: " + nome);
            System.out.println("Média: " + media);
            System.out.println("Situação: " + situacao);
        }

        sc.close();
    }
}
