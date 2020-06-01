package introducaoClasses;

public class Estudante {
	private String nome;
	private int idade;
	private double[] notas;
	
		public void Print() {
		System.out.println("Nome: " +this.nome);
		
		if (this.idade < 0) {
		System.out.println("Idade incorreta, digite novamente!");
		}else {
			System.out.println(this.idade);
		}
		
		
		if (this.notas != null) {
		for (double media : this.notas)
			System.out.print(media+ " ");

		}
		
	}
	
	public void media() {
		
		double media = 0;
		for (double nota : this.notas) {
			media += nota;
			
		}
		media = (media / this.notas.length);
		
		if (media >= 6 ) {
			
			System.out.println("Aprovado por média!" +media);
		}else {
			System.out.println();
			System.out.println("Reprovado.");
		}
	}
	
	public void setNome(String nome) {
		this.nome = nome;
	}
	public void setIdade(int idade) {
		this.idade = idade;
	}
	public void setNotas(double[] notas) {
		this.notas = notas;
	}
	
	public String getNome() {
		return this.nome;
	}
	public int getIdade() {
		return this.idade;
	}
	public double[] getNotas() {
		return this.notas;
	}

}
