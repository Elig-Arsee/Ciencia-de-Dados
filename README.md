# Inrodução Ciência de Dados
Resumo
=======

Este conjunto de dados (ml-latest-small) descreve a classificação de 5 estrelas e a atividade de marcação de texto livre do [MovieLens] (http://movielens.org), um serviço de recomendação de filmes. Ele contém 1.00836 classificações e 3.683 aplicativos de marcação em 9.742 filmes. Esses dados foram criados por 610 usuários entre 29 de março de 1996 e 24 de setembro de 2018. Este conjunto de dados foi gerado em 26 de setembro de 2018.

Os usuários foram selecionados aleatoriamente para inclusão. Todos os usuários selecionados avaliaram pelo menos 20 filmes. Nenhuma informação demográfica é incluída. Cada usuário é representado por um id e nenhuma outra informação é fornecida.

Os dados estão contidos nos arquivos `links.csv`,` movies.csv`, `ratings.csv` e` tags.csv`. Mais detalhes sobre o conteúdo e o uso de todos esses arquivos a seguir.

Este é um conjunto de dados de * desenvolvimento *. Como tal, pode mudar com o tempo e não é um conjunto de dados apropriado para resultados de pesquisa compartilhados. Veja os conjuntos de dados * benchmark * disponíveis se essa for sua intenção.

Este e outros conjuntos de dados GroupLens estão publicamente disponíveis para download em <http://grouplens.org/datasets/>.


Licença de Uso
=============

Nem a Universidade de Minnesota nem qualquer um dos pesquisadores envolvidos pode garantir a exatidão dos dados, sua adequação para qualquer propósito específico ou a validade dos resultados com base no uso do conjunto de dados. O conjunto de dados pode ser usado para quaisquer fins de pesquisa nas seguintes condições:

* O usuário não pode declarar ou sugerir qualquer endosso da University of Minnesota ou do GroupLens Research Group.
* O usuário deve reconhecer o uso do conjunto de dados em publicações resultantes do uso do conjunto de dados (ver informações de citação abaixo).
* O usuário pode redistribuir o conjunto de dados, incluindo transformações, desde que seja distribuído sob as mesmas condições de licença.
* O usuário não pode usar essas informações para fins comerciais ou de geração de receita sem primeiro obter permissão de um membro do corpo docente do GroupLens Research Project da Universidade de Minnesota.
* Os scripts de software executáveis ​​são fornecidos "no estado em que se encontram", sem garantia de qualquer tipo, expressa ou implícita, incluindo, mas não se limitando a, garantias implícitas de comercialização e adequação a um propósito específico. Todo o risco quanto à qualidade e desempenho deles é de sua responsabilidade. Se o programa apresentar defeitos, você assumirá o custo de todos os serviços, reparos ou correções necessários.

Em nenhum caso a Universidade de Minnesota, suas afiliadas ou funcionários serão responsáveis ​​por quaisquer danos decorrentes do uso ou incapacidade de usar esses programas (incluindo, mas não se limitando a perda de dados ou dados imprecisos).

Se você tiver mais perguntas ou comentários, envie um e-mail para <grouplens-info@umn.edu>


Citação
========

Para reconhecer o uso do conjunto de dados em publicações, cite o seguinte artigo:

> F. Maxwell Harper e Joseph A. Konstan. 2015. Os conjuntos de dados MovieLens: História e Contexto. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19: 1–19: 19. <https://doi.org/10.1145/2827872>


Mais informações sobre GroupLens
=======================================

GroupLens é um grupo de pesquisa do Departamento de Ciência da Computação e Engenharia da Universidade de Minnesota. Desde a sua criação em 1992, os projetos de pesquisa do GroupLens exploraram uma variedade de campos, incluindo:

* sistemas de recomendação
* comunidades online
* tecnologias móveis e onipresentes
* bibliotecas digitais
* sistemas de informação geográfica local

O GroupLens Research opera um recomendador de filme baseado em filtragem colaborativa, MovieLens, que é a fonte desses dados. Nós o encorajamos a visitar <http://movielens.org> para experimentar! Se você tiver ideias interessantes para realizar trabalhos experimentais no MovieLens, envie-nos um e-mail para <grouplens-info@cs.umn.edu> - estamos sempre interessados ​​em trabalhar com colaboradores externos.


Conteúdo e uso de arquivos
==========================

Formatação e codificação
-----------------------

Os arquivos do conjunto de dados são gravados como arquivos [valores separados por vírgula] (http://en.wikipedia.org/wiki/Comma-separated_values) com uma única linha de cabeçalho. Colunas que contêm vírgulas (`,`) são escapadas com aspas duplas (`" `). Esses arquivos são codificados como UTF-8. Se caracteres acentuados em títulos de filmes ou valores de tag (por exemplo, Misérables, Les (1995)) são exibidos incorretamente , certifique-se de que qualquer programa lendo os dados, como um editor de texto, terminal ou script, esteja configurado para UTF-8.


IDs de usuário
--------

Os usuários do MovieLens foram selecionados aleatoriamente para inclusão. Seus ids foram tornados anônimos. Os ids de usuário são consistentes entre `ratings.csv` e` tags.csv` (ou seja, o mesmo id se refere ao mesmo usuário nos dois arquivos).


Ids de filmes
---------

Apenas filmes com pelo menos uma classificação ou tag são incluídos no conjunto de dados. Esses ids de filme são consistentes com aqueles usados ​​no site MovieLens (por exemplo, id `1` corresponde ao URL <https://movielens.org/movies/1>). Os ids dos filmes são consistentes entre `ratings.csv`,` tags.csv`, `movies.csv` e` links.csv` (ou seja, o mesmo id se refere ao mesmo filme nesses quatro arquivos de dados).


Estrutura do arquivo de dados de classificações (ratings.csv)
-----------------------------------------

Todas as avaliações estão contidas no arquivo `ratings.csv`. Cada linha deste arquivo após a linha do cabeçalho representa uma avaliação de um filme por um usuário e tem o seguinte formato:

    userId, movieId, rating, timestamp

As linhas dentro desse arquivo são ordenadas primeiro por userId e, em seguida, dentro do usuário, por movieId.

As avaliações são feitas em uma escala de 5 estrelas, com incrementos de meia estrela (0,5 estrelas - 5,0 estrelas).

Os carimbos de data / hora representam os segundos desde a meia-noite do Tempo Universal Coordenado (UTC) de 1º de janeiro de 1970.


Estrutura do arquivo de dados de tags (tags.csv)
-----------------------------------

Todas as tags estão contidas no arquivo `tags.csv`. Cada linha deste arquivo após a linha do cabeçalho representa uma tag aplicada a um filme por um usuário e tem o seguinte formato:

    userId, movieId, tag, timestamp

As linhas dentro desse arquivo são ordenadas primeiro por userId e, em seguida, dentro do usuário, por movieId.

Tags são metadados gerados pelo usuário sobre filmes. Cada tag é normalmente uma única palavra ou frase curta. O significado, o valor e a finalidade de uma tag específica são determinados por cada usuário.

Os carimbos de data / hora representam os segundos desde a meia-noite do Tempo Universal Coordenado (UTC) de 1º de janeiro de 1970.


Estrutura do arquivo de dados de filmes (movies.csv)
---------------------------------------

As informações do filme estão contidas no arquivo `movies.csv`. Cada linha deste arquivo após a linha do cabeçalho representa um filme e tem o seguinte formato:

    movieId, título, gêneros

Os títulos dos filmes são inseridos manualmente ou importados de <https://www.themoviedb.org/> e incluem o ano de lançamento entre parênteses. Erros e inconsistências podem existir nesses títulos.

Os gêneros são uma lista separada por barras verticais e são selecionados a partir do seguinte:

* Açao
* Aventura
* Animação
* Infantil
* Comédia
* Crime
* Documentário
* Drama
* Fantasia
* Film-Noir
* Horror
* Musical
* Mistério
* Romance
* Ficção científica
* Filme de ação
* Guerra
* Ocidental
* (nenhum gênero listado)


Estrutura do arquivo de dados de links (links.csv)
---------------------------------------

Os identificadores que podem ser usados ​​para vincular a outras fontes de dados do filme estão contidos no arquivo `links.csv`. Cada linha deste arquivo após a linha do cabeçalho representa um filme e tem o seguinte formato:

    movieId, imdbId, tmdbId

movieId é um identificador de filmes usado por <https://movielens.org>. Por exemplo, o filme Toy Story tem o link <https://movielens.org/movies/1>.

imdbId é um identificador de filmes usado por <http://www.imdb.com>. Por exemplo, o filme Toy Story tem o link <http://www.imdb.com/title/tt0114709/>.

tmdbId é um identificador para filmes usados ​​por <https://www.themoviedb.org>. Por exemplo, o filme Toy Story tem o link <https://www.themoviedb.org/movie/862>.

O uso dos recursos listados acima está sujeito aos termos de cada provedor.


Validação cruzada
----------------

As versões anteriores do conjunto de dados MovieLens incluíam dobras cruzadas pré-calculadas ou scripts para realizar esse cálculo. Não agrupamos mais nenhum desses recursos com o conjunto de dados, uma vez que a maioria dos kits de ferramentas modernos fornece isso como um recurso integrado. Se você deseja aprender sobre abordagens padrão para computação de dobra cruzada no contexto de avaliação de sistemas de recomendação, consulte [LensKit] (http://lenskit.org) para ferramentas, documentação e exemplos de código-fonte aberto.
