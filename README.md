# Jogo-C-
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int escolhaJogador, escolhaComputador;
    srand(time(NULL));

    printf("Bem-vindo ao jogo de Pedra, Papel e Tesoura!\n");
    printf("Escolha sua jogada:\n");
    printf("0 - Pedra\n");
    printf("1 - Papel\n");
    printf("2 - Tesoura\n");
    printf("Sua escolha: ");
    scanf("%d", &escolhaJogador);

    escolhaComputador = rand() % 3;

    printf("O computador escolheu: %d\n", escolhaComputador);

    if (escolhaJogador == escolhaComputador) {
        printf("Empate!\n");
    } else if ((escolhaJogador == 0 && escolhaComputador == 2) ||
               (escolhaJogador == 1 && escolhaComputador == 0) ||
               (escolhaJogador == 2 && escolhaComputador == 1)) {
        printf("Você venceu!\n");
    } else {
        printf("Você perdeu!\n");
    }

    return 0;
}
