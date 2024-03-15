# Empregado


package mainempregado;


public class MainEmpregado {

   
    public static void main(String[] args) {
         // Criando instâncias da classe Empregado
        Empregado empregado1 = new Empregado("João", "Silva", 5000);
        Empregado empregado2 = new Empregado("Maria", "Santos", 6000);

        // Exibindo o salário anual de cada empregado
        System.out.println("Salário anual de " + empregado1.getPrimeiroNome() + " " + empregado1.getSobrenome() + ": $" + empregado1.calcularSalarioAnual());
        System.out.println("Salário anual de " + empregado2.getPrimeiroNome() + " " + empregado2.getSobrenome() + ": $" + empregado2.calcularSalarioAnual());

        // Aumentando o salário de cada empregado em 10%
        empregado1.aumentarSalario();
        empregado2.aumentarSalario();

        // Exibindo o salário anual atualizado de cada empregado
        System.out.println("\nApós o aumento de 10%:");
        System.out.println("Novo salário anual de " + empregado1.getPrimeiroNome() + " " + empregado1.getSobrenome() + ": $" + empregado1.calcularSalarioAnual());
        System.out.println("Novo salário anual de " + empregado2.getPrimeiroNome() + " " + empregado2.getSobrenome() + ": $" + empregado2.calcularSalarioAnual());
    }
    
}

package mainempregado;


public class Empregado {
    private String primeiroNome;
    private String sobrenome;
    private double salarioMensal;

    // Construtor
    public Empregado(String primeiroNome, String sobrenome, double salarioMensal) {
        this.primeiroNome = primeiroNome;
        this.sobrenome = sobrenome;
        if (salarioMensal > 0)
            this.salarioMensal = salarioMensal;
        else
            this.salarioMensal = 0.0;
    }

    // Métodos set e get para primeiroNome
    public void setPrimeiroNome(String primeiroNome) {
        this.primeiroNome = primeiroNome;
    }

    public String getPrimeiroNome() {
        return primeiroNome;
    }

    // Métodos set e get para sobrenome
    public void setSobrenome(String sobrenome) {
        this.sobrenome = sobrenome;
    }

    public String getSobrenome() {
        return sobrenome;
    }

    // Métodos set e get para salarioMensal
    public void setSalarioMensal(double salarioMensal) {
        if (salarioMensal > 0)
            this.salarioMensal = salarioMensal;
        else
            this.salarioMensal = 0.0;
    }

    public double getSalarioMensal() {
        return salarioMensal;
    }

    // Método para calcular o salário anual
    public double calcularSalarioAnual() {
        return salarioMensal * 12;
    }

    // Método para aumentar o salário em 10%
    public void aumentarSalario() {
        salarioMensal *= 1.10;
    }
}
