package contatoagenda;

public class Contato {
private String nome;
private String telefone;
private String dataDeAniversario;
private String email;
public Contato(String nome, String telefone2, String dataAniversario, String email) {
	this.dataDeAniversario=dataAniversario;
	this.email=email;
	this.nome=nome;
	this.telefone=telefone2;
}
public String getnome() {
	return nome;
}
public String gettelefone() {
	return telefone;
}
public String getdataDeAniversario() {
	return dataDeAniversario;
}
public String getemail() {
	return email;
}


}
*******
******
package contatoagenda;

public class Agenda {
	public static void main(String[] args) {
	}
	private Contato[] contatos;
	private int quantidadedeContatos;
		public Agenda() {
			this.contatos = new Contato[50];
			this.quantidadedeContatos=0;
		}
		public void adicionarContatos(Contato contato) {
			if(quantidadedeContatos<50) {
				contatos[quantidadedeContatos]=contato;
				quantidadedeContatos++;
				System.out.println("Contato adicionado com sucesso!");
			}else {
				System.out.println("Agenda cheia! Não é possivel adicionar mais contatos. ");
			}
		}
		public Contato consultarContato(String nome) {
			for(int i = 0; i < quantidadedeContatos; i++) {
				if(contatos[i].getnome().equalsIgnoreCase(nome)) {
					return contatos[i];
				}
			}
			return null;
		}
		public void listarTodosContatos() {
			if(quantidadedeContatos==0) {
				System.out.println("Agenda vazia.");
			}else {
				for(int i = 0;i<quantidadedeContatos;i++) {
					System.out.println(contatos[i]);
				}
			}
		}
		public void listarAniversariantesDoMes(String nome) {
			boolean encontrou = false;
			for(int i = 0;i<quantidadedeContatos; i++) {
				if(contatos[i]==contatos[i]) {
					System.out.println(contatos[i]);
					encontrou = true;
				}
			}
			if(!encontrou) {
				System.out.println("Nenhum aniversariante encontrado no mes");
		}
		}
		}
       *********
       *********
       package appAgenda;
import java.util.Scanner;
import contatoagenda.Contato;
public class Agenda {
	public static void main(String[] args) {
		Agenda agenda = new Agenda();
		Scanner sc = new Scanner(System.in);
		int opçao;
	  int opcao;
	do {
          System.out.println("\n--- Menu da Agenda ---");
          System.out.println("1. Adicionar Contato");
          System.out.println("2. Consultar Contato");
          System.out.println("3. Listar Todos os Contatos");
          System.out.println("4. Listar Aniversariantes do Mês");
          System.out.println("0. Sair");
          System.out.print("Escolha uma opção: ");
          opcao = sc.nextInt();
          sc.nextLine(); // Limpa o buffer do scanner
          switch (opcao) {
              case 1:
                  System.out.println("Adicionar Contato");
                  System.out.print("Nome: ");
                  String nome = sc.nextLine();
                  System.out.print("Telefone: ");
                  String telefone = sc.nextLine();
                  System.out.print("Data de Aniversário (DDMMAAAA): ");
                  String dataAniversario = sc.nextLine();
                  System.out.print("Email: ");
                  String email = sc.nextLine();
                  Contato contato = new Contato(nome, telefone, dataAniversario, email);
                  agenda.adicionarContato(contato);
                  break;
              case 2:
                  System.out.println("Consultar Contato");
                  System.out.print("Nome: ");
                  String nomeConsulta = sc.nextLine();
                  Contato contatoConsultado = agenda.consultarContato(nomeConsulta);
                  if (contatoConsultado != null) {
                      System.out.println("Contato encontrado: " + contatoConsultado);
                  } else {
                      System.out.println("Contato não encontrado.");
                  }
                  break;
              case 3:
                  System.out.println("Listar Todos os Contatos");
                  agenda.listarTodosContatos();
                  break;
              case 4:
                  System.out.println("Listar Aniversariantes do Mês");
                  System.out.print("Informe o mês (MM): ");
                  String mes = sc.nextLine();
                  agenda.listarAniversariantesDoMes(mes);
                  break;
              case 0:
                  System.out.println("Saindo...");
                  break;
              default:
                  System.out.println("Opção inválida! Tente novamente.");
          }
      } while (opcao != 0);
      sc.close();
  }
private void listarAniversariantesDoMes(String mes) {
	}
	private void listarTodosContatos() {
	}
	private Contato consultarContato(String nomeConsulta) {
		return null;
	}
	private void adicionarContato(Contato contato) {
	}
}

	

