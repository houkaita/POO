import java.util.Scanner;

public class JogoDaVelha {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		char[][] jogo = new char[3][3];
	
		//Falar quem representa qual
		System.out.println("Jogador 1 eh X");
		System.out.println("Jogador 2 eh O");
	
		for(int i = 0; i < 9; i++) {
			int x = 0, y = 0;
			char j;
			boolean valido = false;
			boolean venceu = false;
			
			//Determinar o jogador da vez
			if(i % 2 == 0) {
				j = 'X';
			}
			else {
				j = 'O';
			}
			
			//Avisar de quem é o turno
			System.out.println("Jogador " + j);
			
			//Pegar as coordenadas e validar se estão dentro do escolpo da matriz
			while(!valido) {
				System.out.println("Posicao que deseja fazer sua jogada na vertical ");
				y = scan.nextInt();
			
				if(y > 3 || y < 1) {
					System.out.println("Numero invalido");
				}
				else { valido = true; y--;}
			}		
			
			valido = false;
			
			while(!valido) {
				System.out.println("Posicao que deseja fazer sua jogada na horizontal ");
				x = scan.nextInt();
				
				if(x > 3 || x < 1) {
					System.out.println("Numero invalido");
				}
				else { valido = true; x--;}
				
			}
			
			//verificar se a casa ja foi preenchida
			if(jogo[x][y] == 'X' || jogo[x][y] == 'O') {
				System.out.println("Casa ja preenchida");
				i--;
			}
			else {
				jogo[x][y] = j;
			}
			
			//imprimir o tabuleiro
			for(int p = 0; p < jogo.length; p++) {
				for(int u = 0; u < jogo[p].length; u++) {
					System.out.print(jogo[p][u] + " ");
				}
				System.out.println();
			}
			
			//verificar se há vencedor na horizontal
			for(int p = 0; p < jogo.length; p++) {
				if(jogo[p][0] == 'X' && jogo[p][1] == 'X' && jogo [p][2] == 'X') {
					System.out.println("Jogador 1 venceu!!");
					break;
				}
				
				if(jogo[p][0] == 'O' && jogo[p][1] == 'O' && jogo [p][2] == 'O') {
					System.out.println("Jogador 2 venceu!!");
					break;
				}
			}
			
			//verificar se há vencedor na vertical
			for(int p = 0; p < jogo.length; p++) {
				if(jogo[0][p] == 'X' && jogo[1][p] == 'X' && jogo [2][p] == 'X') {
					System.out.println("Jogador 1 venceu!!");
					venceu = true;
				}
			
				if(jogo[0][p] == 'O' && jogo[1][p] == 'O' && jogo [2][p] == 'O') {
					System.out.println("Jogador 2 venceu!!");
					venceu = true;
				}
			}
			
			//verficar se há vencedor na diagonal
			if(jogo[0][0] == 'X' && jogo[1][1] == 'X' && jogo [2][2] == 'X') {
				System.out.println("Jogador 1 venceu!!");
				venceu = true;
			}
				
			if(jogo[0][0] == 'O' && jogo[1][1] == 'O' && jogo [2][2] == 'O') {
				System.out.println("Jogador 2 venceu!!");
				venceu = true;
			}
			
			//verificar se há vencedor na diagonal invertida
			if(jogo[2][0] == 'X' && jogo[1][1] == 'X' && jogo [0][2] == 'X') {
				System.out.println("Jogador 1 venceu!!");
				venceu = true;
			}
				
			if(jogo[2][0] == 'O' && jogo[1][1] == 'O' && jogo [0][2] == 'O') {
				System.out.println("Jogador 2 venceu!!");
				venceu = true;
			}
			
			if(venceu) {
				break;
			}
			
		}
		
		System.out.println("Fim do jogo! Espero que tenha gostado!!!");
	}
}
