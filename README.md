# Campo Minado em Java com Swing

Este é um projeto de **Campo Minado** desenvolvido em Java utilizando a biblioteca gráfica **Swing**.

![Campo Minado Demo](demo.gif)

## Funcionalidades

- **Interface Gráfica Amigável**: Desenvolvida com Swing para uma experiência visual agradável.
- **Jogo Clássico**: Implementação do jogo clássico de Campo Minado.
- **Diferentes Níveis de Dificuldade**: Escolha entre diferentes configurações de tamanho de tabuleiro e número de minas.
- **Contagem de Minas**: Mostra quantas minas restam para serem marcadas.
- **Revelação de Área**: Clique duplo para revelar células sem minas adjacentes de forma automática.
- **Botão de Reinício**: Reinicie o jogo a qualquer momento com o botão dedicado.

## Como Jogar

1. **Iniciando o Jogo**: Execute o arquivo `CampoMinado.jar` ou compile o projeto diretamente.
   
2. **Regras**: Clique em qualquer célula para iniciar o jogo. O objetivo é revelar todas as células que não contêm minas sem revelar nenhuma que tenha uma mina.

3. **Controles**:
   - Clique único para revelar uma célula.
   - Clique com o botão direito para marcar ou desmarcar uma célula como uma mina.
   - Clique duplo em uma célula já revelada para revelar automaticamente células vizinhas seguras.
   - Use o botão de reinício para começar um novo jogo.

## Configurações Personalizadas

Você pode ajustar as configurações do jogo editando as constantes no arquivo `CampoMinado.java`, como o tamanho do tabuleiro e o número de minas.

## Configurações Personalizadas

Você pode ajustar as configurações do jogo editando as constantes no arquivo `CampoMinado.java`, como o tamanho do tabuleiro e o número de minas.

No construtor da classe `TelaPrincipal`, as configurações de dificuldade são definidas da seguinte maneira:

```java
public TelaPrincipal() {
    // Cria um tabuleiro com tamanho 16x16 e 50 minas
    Tabuleiro tabuleiro = new Tabuleiro(16, 30, 50);
    add(new PainelTabuleiro(tabuleiro));
    
    setTitle("Campo Minado");
    setSize(690, 438);
    setLocationRelativeTo(null);
    setDefaultCloseOperation(DISPOSE_ON_CLOSE);
    setVisible(true);
}
