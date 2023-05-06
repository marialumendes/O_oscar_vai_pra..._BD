<img src= "https://www.tenhomaisdiscosqueamigos.com/wp-content/uploads/2017/02/oscar-logotipo.jpg">

## Bem-vindo a premiação mais aguardada do ano! Venha conferir os ganhadores deste ano de um jeito muito simples, atrás do banco de dados.

##

<h3> 1- Quantas vezes Natalie Portman foi indicada ao Oscar? </h3>
 R: 3 vezes. - <code>SELECT COUNT(*) FROM movies where name like "%Natalie Portman%"; </code>
 
 ##
 <h3> 2- Quantos Orcars Natelie Portman ganhou? </h3>
 R: 1 vez. - <code>SELECT count(*) FROM `movies` where name like "%Natalie Portman%" and winner = "1"; </code>
 
 ##
 <h3> 3- Amy Adams já ganhou algum Oscar?</h3>
 R: Ela não ganhou nenhum oscar. - <code>SELECT count(*) FROM `movies` where name like "%Amy Adams%" AND WINNER = 'true'; </code>
 
 ##
 <h3 > 4- A série de filmes Toy Story ganhou um Oscar em quais anos? </h3>
 R: Nos anos de 2011 e 2020. - <code>SELECT year_ceremony FROM `movies` where film like "%Toy Story%" AND WINNER = '1'</code>
 
 ##
 <h3> 5- Quem tem mais Oscars: a categoria "Melhor Ator" ou "Melhor Filme"?</h3>
 R: Melhor filme com 93 resultados. - <code>SELECT COUNT(id_movie) FROM movies WHERE (category = "BEST PICTURE" OR category like "%PICTURE" OR category like "%PRODUCTION")AND WINNER = 'True'; </code> || - <code>SELECT count(id_movie) FROM movies where category = "ACTOR" AND WINNER = 'True'; </code>
 
 ##
 <h3> 6- O primeiro Oscar para melhor Atriz foi para quem? Em que ano?</h3>
 R: Foi para Janet Gaynor, em 1928. - <code>SELECT * from movies WHERE category = 'actress' and winner = 'true';</code>
 
 ##
 <h3> 7- Na coluna/campo Winner, altere todos os valores com "True" para 1 e todos os valores "False" para 0. </h3>
<code>UPDATE movies SET winner = 0 where winner = 'False';
 UPDATE movies SET winner = 1 where winner = 'True';</code>
 
 ##
 <h3> 8- Em qual edição do Oscar "Crash" ganhou o prêmio principal? </h3>
 R: Foi na edição 78. - <code>select * from movies where film like "%Crash%" and winner = 'True';</code>
