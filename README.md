# Engenharia-de-software
Codigo em C++
Alunos:
Higor de Jesus Francisco.
Klynsman Wandes Santos Nascimento.
Carlos Felipe Silva.
Luan Víctor Leite da Silva.
Géssica Pinheiro Santana e Silva.
Rodriggo Marcelino Santos.
Rickelme Rocha Andrade.
Gabriela Gomes Tavares Santos.
Daniel Lucas Santos Gomes

5 Ferramentas CASE Fundamenteal para o Desenvolvimento de Solfware

1)Postgres: é um sistema gerenciador de banco de dados objeto relacional, desenvolvido como projeto de código aberto.
2)Microsoft Word:pode ser usado para produzir trabalhos escolares e textos acadêmicos. Com recursos comparáveis a outros editores de texto modernos, suporta também a adição e edição básica de imagens e formatação de texto.
3)Microsoft Visual Studio é um ambiente de desenvolvimento integrado da Microsoft para desenvolvimento de software especialmente dedicado ao .NET Framework e às linguagens Visual Basic, C, C++, C# e F#.
4)NetBeans:é um ambiente de desenvolvimento integrado gratuito e de código aberto para desenvolvedores de software nas linguagens Java, JavaScript, HTML5, PHP, C/C++, Groovy, Ruby, entre outras.
5)Java Development Kit significa Kit de Desenvolvimento Java, e é um conjunto de utilitários que permitem criar sistemas de software para a plataforma Java. É composto por compilador e bibliotecas

# inclui <iostream>
usando namespace std;

int main () {
    setlocale (LC_ALL, "português");
	string nome;
	int idade = 0; 
	float nota_1,nota_2,nota_3,nota_4, media, nota_maior = -1, soma;
	char digite;
	bool sair = false;


	cout << "\t---<Controle Acadêmico>---\n\n"; //Distanciamento para Centralizar
	cout << "Escolha as Seguntes Opções:\n\n";

	cout << "(1) <Incluir os dados pessoais do Aluno>\n" << endl;
	cout << "(2) <Incluir as Notas do Aluno> \ n " << endl;
	cout << "(3) <Exibir a Média Global do Aluno> \ n " << endl;
    cout << "(4) <Exibir a Maior Nota do Aluno> \ n " << endl;
    cout << "(5) <Sair> \ n " << endl;

    while(!sair){
    	cout << "\nNúmero Escolhido: ";
    	cin >> digite;

    	switch(digite){
    		caso 1': 
    			 cout << "\n\t--|Dados Pessoais|--\n";
    			 cin.ignore ();
    			 cout << " \ n -> Nome Completo do Aluno: \ n ";
    			 getline (cin, nome);
    			 cout << " \ n -> Idade:";
    			 cin >> idade;
    			 pausa;
    	    caso '2':
    	    	 cout << " \ n \ t - | Nota do Aluno | - \ n ";
    	         cout << "{Aluno:" << nome << "}" << endl;
    	         cout << " \ n 1 ° Nota:";
    	         cin >> note_1;
    	         cout << " \ n 2 ° Nota:";
    	         cin >> note_2;
    	         cout << " \ n 3 ° Nota:";
    	         cin >> note_3;
    	    	 cout << " \ n 4 ° Nota:";
    	     	 cin >> note_4;

    	        if (nota_1> = nota_2 && nota_1> = nota_3 && nota_1> = nota_4) {
   	             nota_maior = nota_1;
                }senão{
   	                if (nota_2> = nota_1 && nota_2> = nota_3 && nota_2> = nota_4) {
   	                nota_maior = nota_2;
                }senão{            
   	                if (nota_3> = nota_1 && nota_3> = nota_2 && nota_3> = nota_4) {
   	                nota_maior = nota_3;
                }senão{
   	                nota_maior = nota_4;
                    }	    
                  }
                }
    	    	pausa;
    	    case '3'://Média global com controle de acesso
    	    	 cout << "\n\t--|Média Global|--\n\n";// Só será acessado com os dados e com as notas do aluno
    	    	if(idade <= 0){                                              
    	    	     cout << "\n|Por Favor, Preencha o Nome do Aluno!|\n\n";
				}senão{
				    if(nota_maior <= -1){	
    			     cout << " \ n | Preencha as Notas de (" << nome << ")! | \ n \ n ";
			     }senão{
    	    	     cout << "Aluno ->" << nome;
    	    	     soma = (nota_1  + nota_2 + nota_3 + nota_4);
    	    	     media = soma/4;
    	    	     cout << " \ n Média:" << nota_1 << "+" << nota_2 << "+" << nota_3 << "+" << nota_4 << "=" << soma << "| 4 ___ = "<< media << endl;

			       }
		       }
    	    	pausa;
    	    case '4': //Maior nota com controle de acesso
    	    	if(idade <= 0 ){
    	    	 	cout << "\n|Por Favor, Preencha o Nome do Aluno!|\n\n";   	    	 	
				}senão{
				    if(nota_maior <= -1){  
				     cout << " \ n | Preencha as Notas de (" << nome << ")! | \ n \ n ";
			    }senão{
    	    	     cout << " \ n \ t - | Maior Nota | - \ n \ n ";
    	    	     cout << "Aluno ->" << nome;
    	    	     cout << " \ n Maior Nota:" << nota_maior << endl;
			       }
			    }
    	    	pausa;
    	    case '5'://Controle para Finalizar
			    if(idade <= 0 && nota_maior != -1 ){
				    cout << "\n\n| Para finalizar, Conclua os Dados do Aluno |\n\n";
				}senão{
					if(nota_maior <= -1 && idade != 0){
				     cout << "\n\n| Para finalizar, Conclua as Notas do Aluno |\n\n";
					}senão{
				     cout << "\n\t--|Controle Acadêmico Finalizado|--\n ";
					 sair = true;
				   }
				}
    	    	pausa;
    		padrão:
    			cout << " \ n \ t - | Tecla Inválida | - \ n \ n ";
    			pausa;	
	  	}	    	  
	}
	return 0;
}
