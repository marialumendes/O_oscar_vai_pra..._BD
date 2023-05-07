<p align="center"><img src= "https://www.tenhomaisdiscosqueamigos.com/wp-content/uploads/2017/02/oscar-logotipo.jpg"></p>


## Bem-vindo a premiação mais aguardada do ano! Venha conferir os ganhadores deste ano de um jeito muito simples, atrás do banco de dados.

##

<h3> 1- Quantas vezes Natalie Portman foi indicada ao Oscar? </h3>
 R: 3 vezes. <br>
 -<code>SELECT COUNT(*) FROM movies where name like "%Natalie Portman%"; </code>
 
 ##
 <h3> 2- Quantos Orcars Natelie Portman ganhou? </h3>
 R: 1 vez. <br>
 - <code>SELECT count(*) FROM `movies` where name like "%Natalie Portman%" and winner = "1"; </code>
 
 ##
 <h3> 3- Amy Adams já ganhou algum Oscar?</h3>
 R: Ela não ganhou nenhum oscar. <br>
 - <code>SELECT count(*) FROM `movies` where name like "%Amy Adams%" AND WINNER = 'true'; </code>
 
 ##
 <h3 > 4- A série de filmes Toy Story ganhou um Oscar em quais anos? </h3>
 R: Nos anos de 2011 e 2020. <br> 
 - <code>SELECT year_ceremony FROM `movies` where film like "%Toy Story%" AND WINNER = '1'</code>
 
 ##
 <h3> 5- Quem tem mais Oscars: a categoria "Melhor Ator" ou "Melhor Filme"?</h3>
 R: Melhor filme com 93 resultados. <br> 
 - <code>SELECT COUNT(id_movie) FROM movies WHERE (category = "BEST PICTURE" OR category like "%PICTURE" OR category like "%PRODUCTION")AND WINNER = 'True'; </code> || - <code>SELECT count(id_movie) FROM movies where category = "ACTOR" AND WINNER = 'True'; </code>
 
 ##
 <h3> 6- O primeiro Oscar para melhor Atriz foi para quem? Em que ano?</h3>
 R: Foi para Janet Gaynor, em 1928. <br>
 - <code>SELECT * from movies WHERE category = 'actress' and winner = 'true';</code>
 
 ##
 <h3> 7- Na coluna/campo Winner, altere todos os valores com "True" para 1 e todos os valores "False" para 0. </h3>
<code>UPDATE movies SET winner = 0 where winner = 'False';
 UPDATE movies SET winner = 1 where winner = 'True';</code>
 
 ##
 <h3> 8- Em qual edição do Oscar "Crash" ganhou o prêmio principal? </h3>
 R: Foi na edição 78. <br>
 - <code>select * from movies where film like "%Crash%" and winner = 'True';</code>
 
 ##
 <h3> 9- Bom... dê um Oscar para um filme que merece muito, mas não ganhou. </h3>
 R: Um filme que deveria ter ganhado um Oscar é Castelo animado.
 
<code> select * from movies where film like '%Howls Moving Castle%' and winner = '1'
SELECT * FROM `movies` where film like "%Howls Moving Castle%" AND WINNER = '1'
update movies set winner= '1' where film like '%Howls Moving Castle%'
</code>

##
<h3> 10- O filme Central do Brasil aparece no Oscar? </h3>
R: Não aparece.<br> 
- <code>SELECT count(*) FROM `movies` where film like "%Central do Brasil%"</code>
 
 ##
 <h3> 11- Inclua no banco 3 filmes que nunca nem foram nomeados ao Oscar, mas que na sua opinião, merecem.</h3>
 <code>-INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES  ('2009', '2010', 82, 'MELHOR FILME', 'Anne Fletcher', 'The Proposal' , '1');
-INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES  ('2011', '2012', 84, 'MELHOR FILME', 'Dennis Dugan','Just Go with it' , '1'); 
-INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES  ('2008', '2009', 81, 'MELHOR FILME', ' Bryan Bertino','The Strangers' , '1'); </code>
 
 ##
 <h3> 12- Crie uma nova categoria de premiação. Qualquer prêmio que você queira dar. Agora vamos dar esses prêmios aos filmes que você cadastrou na questão acima.</h3>
 <code>ALTER TABLE movies ADD CONQUISTA varchar(225);  UPDATE `movies` SET `CONQUISTA`='NÃO TEM COMO ENJOAR' WHERE category LIKE '%MELHOR FILME%';
</code>

##
<h3> 13- Qual foi o primeiro ano a ter um prêmio do Oscar?</h3>
<code>select * from movies where winner = 'true'</code>

##
<h3> 14 - Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?</h3>

<h4> Melhor filme</h4>
R: O oscar de melhor filme foi para Chicago <br>
<code>SELECT * FROM movies where year_ceremony like '2003' and category like '%BEST PICTURE%' and winner = 1 </code>

<h4>Melhor Atriz</h4>
R: O oscar de melhor atriz foi para Nicole Kidman, com the hours <br>
<code>SELECT * FROM movies where year_ceremony like '%2003%' and category like '%ACTRESS%' and winner = 1;</code>

<h4>>Melhor diretor</h4>
R: O oscar de melhor diretor foi para Roman Polanski com O pianista <br>
<code>SELECT * FROM movies where year_ceremony like '%2003%' and category like '%DIRECTING%' and winner = 1;</code>
 
 
 ##
 <h3>15- Agora procure 7 atrizes que não sejam americanas, europeias ou brasileiras.  Vamos cadastrá-los no nosso banco, mas eles ainda não ganharam o Oscar. Só foram nomeados.</h3> <br>
 <code>
- 1 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2019', '2020', '92', 'ACTRESS', 'Park So-dam', 'Parasite', '0', ''); 
<br>
- 2 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2022', '2023', '95', 'ACTRESS', 'Sandra Oh',  'Umma', '0', '');
<br>
- 3 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2009', '2010', '82', 'ACTRESS', 'Isla Fisher',  'Confessions of a Shopaholic', '0', '');  
<br>
- 4 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2012', '2013', '85', 'ACTRESS', 'Rachel Mwanza', 'Rebelle', '0', '');  
<br>
- 5 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2017', '2018', '90', 'ACTRESS', 'Daniela Vega', 'Una Mujer Fantástica', '0', '');
<br>
- 6 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2008', '2009', '81', 'ACTRESS', 'Valeria Bertuccelli', 'Un Novio Para Mi Mujer', '0', '');
<br>
- 7 INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2021', '2022', '94', 'ACTRESS', 'Priyanka Chopra','The White Tiger' , '0', '');</code>
 
 
 ##
 <h3>16- Agora vamos falar da sua vida. Me diga o nome de uma pessoa que você admira e o que ela fez na sua vida. Agora me diz: Quê prêmio essa pessoa merece? </h3>
Este oscar vai para minha tia Izabel. Ela é uma mulher incrivel, forte, destemida, super mãe e super tia. Esses últimos anos ela batalhou muito para conseguir o melhor para ela e seu filho. Mesmo com todas as dificuldades, ela segue de cabeça erguida, determinada a conquistar seus sonhos.

<code> - INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner, PRÊMIO) VALUES ('2023', '2024', '96', 'ACTRESS', 'Izabel Cristina Rodrigues', 'I am', '1', ''); 
</code>
 
 #
 <p align="center"> <img src= "https://user-images.githubusercontent.com/125033731/236519898-326fac96-80e3-4a93-b48d-1e29715a888b.png"> </p>
