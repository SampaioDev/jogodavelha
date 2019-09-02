# jogodavelha

ALGORITMO BASE:

Início
	Configurar o Estado Inicial
	Fazer o Estado Inicial ser o Estado Atual
	Definir quem inicia o jogo
	Enquanto Estado Atual <> Estado Final
		Se a vez for do Usuário
			Permitir o Usuário Jogar
		Senão 
			Gerar, de modo simulado, todos os estados filhos, 				alternando simulações do jogo do usuário e CPU até 				chegue-se a uma folha que represente Estado Final

			Usar critério de seleção de melhor subárvore a partir do 			Estado Atual ( Sugestão: atribua 1 ponto para cada 				possibilidade de vitória; -1 ponto para cada 					possibilidade de derrota; e 0 para empate. Feito isso, 				some as quantidades.)

			Selecionar a próxima jogada com base no critério 					definido. 
		fimSe
		Fazer a configuração do tabuleiro da próxima jogada ser o 			novo Estado Atual
		Alternar a vez da Jogada.
	FimEnquanto

	Se Estado Final (na perspectiva da CPU) for Vitória então “CPU 										 	  Venceu”
	Senão Se Estado Final for Derrota então “Usuário Venceu”
		 Senão “Houve Empate”
