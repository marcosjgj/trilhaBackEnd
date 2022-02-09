# <b>trilhaBackEnd</b>

Repositório destinado a entrega dos desafios da trilha de Java + Spring

<br>

## <b>Desafio 1 - Git</b>


### <b>A)</b> Com suas palavras defina o que é um sistema de controle de versões (VCS)?
```
É um sistema de controle de versões de arquivos, onde é possível manipular versões específicas ao longo 
do tempo.
```

### <b>B)</b> Cite 5 vantagens em utilizar um VCS:
```
- Poder reverter arquivos ou projetos inteiros para uma versão anterior
- Comparar modificações
- Mesclar modificações 
- Gerenciar possíveis problemas de versões
- Verificar qual usuário pode ter inserido uma ou mais versões com problemas
```

### <b>C)</b> Cite 3 exemplos de VCS:
```
- Git
- SVN
- CVS
```

### <b>D)</b> Crie um repositório no seu git pessoal “trilhaBackEnd” e utilize para entrega de todos os desafios.
```
OK, criado e em uso
```

<br>

## <b>Desafio 2 - POO</b>

### <b>A)</b> Com suas palavras defina o que é programação orientada a objetos (POO) e cite seus pilares?
```
É um modelo de interação baseado no conceito de objetos que contém dados na forma de atributos, códigos e códigos na forma de métodos. 

Seus pilares são:
- Abstração
- Encapsulamento
- Herança
- Polimorfismo
```
### <b>B)</b> Exemplifique e explique um cenário de abstração;
```java
Abstração é uma classe que define um tipo, e não pode ser instanciada. Uma classe abstrata serve de modelo para outras classes que serão extendias a ela e herdarão os atributos pré definidos.

Segue exemplo:

public abstract class Funcionario {

	protected double salario;

	public double getBonificacao() {
		return this.salario * 1.2;
	}
}

public class Gerente extends Funcionario {

	public double getBonificacao() {
		return this.salario * 1.4 + 1000;
	}
}
```
### <b>C)</b> Exemplifique e explique um cenário de encapsulamento;
```java
Encapsulamento é quando resumimos um procedimento complevo em apenas um método.

Ao invés de todas as vezes que eu quiser cadastrar um livro eu precisar instanciá-lo, abrir uma conexão, salvar o livro e fechar a conexão, eu mudo esse procedimento de salvar para um único método.

Segue exemplo:

public class Livro {

    private final String nome; 
    private final double preco;

    public Livro(String nome, double preco) { 
        this.nome = nome; 
        this.preco = preco; 
    }
}

Livro livro = new Livro("Java", 27.83);

salvaLivro(livro);

public void salvaLivro(Livro livro){
     Conexao conexao = pegaConexaoComOBancoDeDados(); 
     if(!conexao.existeLivro(livro)){
         conexao.cadastraLivro(livro);
    } else{ 
        conexao.atualizaLivro(livro); 
    } 
    conexao.fechaConexao(); 
}
```


### <b>D)</b> Exemplifique e explique um cenário de herança;
```java
Herança é quando criamos uma classe herdando caracteristicas de outras ja existentes, porém podemos adicionar mais atributos além dos herdados.

Segue exemplo:

public class Funcionario {
    private String nome;
    private String cpf;
    private double salario;
}

public class Gerente extends Funcionario {
    private int senha;
    private int numeroDeFuncionariosGerenciados;
}

public class TestaGerente {
    public static void main(String[] args) {
        Gerente gerente = new Gerente();

        // podemos chamar métodos do Funcionario:
        gerente.setNome("Marcos João");

        // e também métodos do Gerente!
        gerente.setSenha(4231);
    }
}
```

### <b>E)</b> Exemplifique e explique um cenário de polimorfismo;

```java
Polimorfismo é a propriedade de duas ou mais classes derivadas de uma mesma superclasse responderem a mesma mensagem, cada uma de uma forma diferente. Ocorre quando uma subclasse redefine um método existente na superclasse, ou seja, quando temos os métodos sobrescritos.

Segue exemplo:

// Superclasse Mamífero:
locomoverSe() {
    // A ser implementado em alguma subclasse. 
}
// Subclasse Macaco
locomoverSe() {
     pulandoDeGalhoEmGalho; 
}
// Subclasse Homem:
locomoverSe() {
    andando; 
}
// Subclasse Baleia
locomoverSe() {
     nadando;
}
```






