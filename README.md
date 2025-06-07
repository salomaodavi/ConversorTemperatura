# 🌡️ Conversor de Temperatura em Java

🚀 Projeto simples e didático de um **Conversor de Temperatura**, desenvolvido em Java, para praticar conceitos fundamentais da linguagem e aprimorar meus conhecimentos na jornada como **Desenvolvedor Java Júnior**.

---

## 🧠 Funcionalidades

- ✅ Conversão de temperaturas entre:
  - Celsius (°C)
  - Fahrenheit (°F)
  - Kelvin (K)
- ✅ Interface simples via terminal
- ✅ Validação de entrada
- ✅ Código limpo, organizado em funções

---

## 🔧 Tecnologias e Ferramentas

- ☕ **Java** (versão 8 ou superior)
- 💻 IDE: IntelliJ, Eclipse, VSCode ou qualquer de sua preferência
- 🖥️ Terminal/Prompt de Comando

---

## ▶️ Como Executar o Projeto

1️⃣ Clone este repositório:

2️⃣ Acesse o diretório:
````
cd seu-repositorio
````
3️⃣ Compile o código:
````
javac Main.java
````
4️⃣ Execute:
````
java Main
````
📜 Exemplo de Uso

🌡️  Conversor de Temperatura - Java 🚀
----------------------------------------
➡️  Digite o valor da temperatura: 100
Escolha a unidade de origem:

1 - Celsius (°C)

2 - Fahrenheit (°F)

3 - Kelvin (K)

➡️  Sua escolha: 1

Escolha a unidade de destino:

1 - Celsius (°C)

2 - Fahrenheit (°F)

3 - Kelvin (K)

➡️  Sua escolha: 2

✅ Resultado: 212.00


💡 Aprendizados:

✔️ Entrada e saída de dados no terminal em Java

✔️ Estruturas condicionais (if, switch)

✔️ Declaração e uso de métodos/funções

✔️ Organização de código e boas práticas

🔥 Código:
````
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("🌡️  Conversor de Temperatura - Java 🚀");
        System.out.println("----------------------------------------");

        System.out.print("➡️  Digite o valor da temperatura: ");
        double temperatura = input.nextDouble();

        System.out.println("Escolha a unidade de origem:");
        System.out.println("1 - Celsius (°C)")
        System.out.println("2 - Fahrenheit (°F)");
        System.out.println("3 - Kelvin (K)");
        System.out.print("➡️  Sua escolha: ");
        int origem = input.nextInt();

        System.out.println("Escolha a unidade de destino:");
        System.out.println("1 - Celsius (°C)");
        System.out.println("2 - Fahrenheit (°F)");
        System.out.println("3 - Kelvin (K)");
        System.out.print("➡️  Sua escolha: ");
        int destino = input.nextInt();

        double resultado = converterTemperatura(temperatura, origem, destino);

        if (Double.isNaN(resultado)) {
            System.out.println("❌ Opção inválida.");
        } else {
            System.out.printf("\n✅ Resultado: %.2f\n", resultado);
        }

        input.close();
    }

    // Função para conversão
    public static double converterTemperatura(double valor, int origem, int destino) {
        if (origem == destino) {
            return valor;
        }

        // Converter para Celsius como base
        double tempCelsius = switch (origem) {
            case 1 -> valor;
            case 2 -> (valor - 32) * 5 / 9;
            case 3 -> valor - 273.15;
            default -> Double.NaN;
        };

        // Converter de Celsius para destino
        return switch (destino) {
            case 1 -> tempCelsius;
            case 2 -> (tempCelsius * 9 / 5) + 32;
            case 3 -> tempCelsius + 273.15;
            default -> Double.NaN;
        };
    }
}
````
Este projeto está sob licença MIT.

