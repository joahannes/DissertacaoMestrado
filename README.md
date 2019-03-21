# Dissertacao de Mestrado

Template LaTeX utilizado para escrita da dissertação de mestrado requerida pelo Programa de Pós-Graduação em Ciência da Computação, da Universidade Federal do Pará, para obtenção do título de Mestre em Ciência da Computação. O template é genérido e pode ser utilizado tanto para Trabalho de Conclusão de Curso (TCC) quanto para Tese de Doutorado.

Informações sobre a dissertação:
	
* **Instituição**: Universidade Federal do Pará
* **Instituto**: Instituto de Ciências Exatas e Naturais
* **Programa**: Programa de Pós-Graduação em Ciência da Computação
* **Título**: Disseminação de Dados Baseada em Métricas de Redes Complexas para Sistemas de Transporte Inteligentes
* **Autor**: Joahannes Bruno Dias da Costa
* **Ano**: 2018

## Requisitos:

* TexLive Full (Linux):
	> sudo apt-get install texlive-full

* MiKTex (Windows):
	> [Link para MiKTex](https://miktex.org/download)

* Editor LaTeX ou Bloco de Notas:
	> [TeXstudio](http://www.texstudio.org/), [Texmaker](http://www.xm1math.net/texmaker/), [Kile](https://kile.sourceforge.io/), etc.

## Instalação:

> git clone https://github.com/joahannes/DissertacaoMestrado.git 

## Lista de Abreviaturas:

### Via Software

Para criar a lista de abreviaturas seguindo o padrão em ordem alfabética e utilizando uma ferramenta de edição, basta fazer a seguinte configuração no seu editor LaTeX:

1. Adicionar "Comando do usuario":

> makeindex -s nomencl.ist -t %.nlg -o %.nls %.nlo

2. Compilar primeiro "comando do usuario" e depois a compilação normal:

> ALT + SHIFT + F1

Obs: Esse comando é válido no [TeXstudio](http://www.texstudio.org/).

### Via Terminal

Para criar a lista de abreviaturas em ordem alfabética via terminal, basta executar o arquivo Makefile (que está dentro do diretório 1_principal/) usando os seguintes passos:

1. Executar o make para criar os arquivos a partir do .tex:

	> make

2. Executar o make index para criar a lista de abreviaturas:

	> make index

3. Executar o make clean para limpar os arquivos desnecessários criados anteriormente:

	> make clean

4. Executar novamente o make para aplicar finalmente a lista de abreviaturas no .tex:

	> make

Obs: Para a lista de abreviaturas funcionar, você deve adicionar a abreviatura e descrição dela durante a escrita do seu documento, Por exemplo, na primeira vez que aparecer a abreviatura VANETs no texto, basta adicionar o comando:

> \nomenclature{\textbf{VANETs}}{\textit{Vehicular Ad hoc Networks}}

Veja o exemplo no parágrafo:

_Este capítulo introduz os conceitos sobre Redes Veiculares Ad hoc (Vehicular Ad hoc Networks - VANETs\nomenclature{\textbf{VANETs}}{\textit{Vehicular Ad hoc Networks}}) por meio de uma visão geral sobre o tema. Levanta a discussão acerca da motivação para elaboração deste trabalho, ilustrando os principais desafios existentes para a construção de propostas a nível de disseminação de dados eficiente. Apresenta os objetivos que envolvem o trabalho, além de sumarizar as contribuições essenciais do mesmo. Por fim, apresenta o conteúdo dos próximos capítulos._

Feito. :smiley:

### Resultado:

[Link para a Dissertação em PDF](https://github.com/joahannes/DissertacaoMestrado/blob/master/1_principal/mestrado_joahannes.pdf)

## Autores:

> [Denis Rosário](https://www.researchgate.net/profile/Denis_Rosario)

> [André Riker](https://www.researchgate.net/profile/Andre_Riker)

> [Joahannes Costa](http://www.lrc.ic.unicamp.br/~joahannes)
