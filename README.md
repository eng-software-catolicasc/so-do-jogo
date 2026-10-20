# SO.DO.JOGO v1.5.4

- 5 decks × 16 cartas = 80 cartas.
- Cartas revisadas conceitualmente a partir de *Sistemas Operacionais: Conceitos e Mecanismos* (Carlos Maziero, 2019).
- Estrutura: **Frente (conceito lúdico) → Verso (fundamento conceitual referenciado)**.
- Sem bloco “Investigue” e sem pistas que entreguem diretamente o diagnóstico do case.
- Favoritos persistentes por grupo.
- Finalização de deck com confirmação explícita: se a equipe tentar concluir sem enviar suas favoritas, o jogo abre um popup e a orienta a voltar ao deck, selecionar ao menos 2 cartas e enviá-las.
- Se uma escolha for alterada após o envio, o deck volta ao estado “favoritas não enviadas” até nova confirmação.
- Pontuação preservada: duas cartas de referência valem +50 cada; as demais retiram -5 ou -10. O estudante não vê a pontuação.

## Executar
```bash
npm install
npm run dev
```

- 10 grupos de acesso (G01 a G10).
- Ao finalizar cada deck, o resultado e a nota são gravados imediatamente e aparecem no painel do professor.
