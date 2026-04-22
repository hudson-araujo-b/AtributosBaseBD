# AtributosBaseBD

```sql
create database bdAgenciaViagens;
use bdAgenciaViagens;

create table cliente(
IdCli int primary key auto_increment,
EmailCli varchar (255) not null unique,
TelefoneCli varchar (20) not null,
NomeCli varchar (100) not null,
DataNasCli date not null,
CpfCli char (11) not null unique,
EnderecoCli varchar (100),
CepCli varchar (9)
);
```

```sql
create database dbteste2a;
use dbteste2a;

create table Cliente (
  codCli int primary key auto_increment,
  Nome varchar(50),
  Telefone varchar(20)
);
-- iserindo dados na tabela
insert into Cliente(nome,telefone)values('Huguinho','(11)11111-1111');
insert into Cliente(nome,telefone)values('Luizinho','(22)22222-2222');
insert into Cliente(nome,telefone)values('Zezinho','(33)33333-3333');
insert into Cliente(nome,telefone)values('Donalds','(44)44444-4444');
insert into Cliente(nome,telefone)values('Patinhas','(55)55555-5555');
insert into Cliente(nome,telefone)values('Maga Patalogica','(66)66666-6666');
insert into Cliente(nome,telefone,Preco)values('City','(88)99999-9999', 21);
insert into Cliente(nome,telefone,Preco)values('Rian','(99)77777-9999', 35);
insert into Cliente(nome,telefone,Preco)values('Zequinha','(97)88888-5555',37);



select * from Cliente;

select CodCli, Nome from Cliente where Telefone= '(22)22222-2222' limit 1;

select CodCli,Nome,Telefone from Cliente where telefone= '(22)22222-2222' and
Nome ='Luizinho';

select CodCli,Nome from Cliente order by Nome desc;

update Cliente set Nome = 'Professor Pardal' where CodCli= 1;

alter table Cliente
add Preco decimal(10,2);

select Nome,Preco from Cliente where Nome='City' and Preco <30;

select Nome,Preco from Cliente where Preco between 30 and 40;      
 
 -- Filtrar dados usando diferente
select Nome,Preco from Cliente where Preco <> 100.00; 

-- Pesquisa Personalizada
select Nome from Cliente where Nome like '%P%';
```

```sql
create database dbHerois;

use dbHerois;

drop table Produto;
create table Herois (
Id int primary key auto_increment,
Nome varchar(50),
Poder varchar(50),
Cor varchar(30)
);
create table Produto (
Id int primary key auto_increment,
Nome varchar(50),
Descricao varchar(150),
Preco decimal(5,2)
);

insert into Herois(Nome, Poder, Cor) values ('Ignis','Controle total do fogo','Vermelho');
insert into Herois(Nome, Poder, Cor) values ('Aquarion','Manipulação da água e cura','Azul');
insert into Herois(Nome, Poder, Cor) values ('Terron','Super força e controle da terra','Marrom');
insert into Herois(Nome, Poder, Cor) values ('Voltix','Velocidade e eletricidade','Amarelo');
insert into Herois(Nome, Poder, Cor) values ('Noctra','Invisibilidade e sombras','Preto');

insert into Produto(Nome, Descricao, Preco) values ('SmartLuz','Lâmpada inteligente controlada por app',79.90);
insert into Produto(Nome, Descricao, Preco) values ('FoneWave','Fone sem fio com cancelamento de ruído',199.90);
insert into Produto(Nome, Descricao, Preco) values ('FitBand Pro','Pulseira fitness com monitor cardíaco',149.90);
insert into Produto(Nome, Descricao, Preco) values ('Café Turbo','Café energético premium em cápsulas',29.90);
insert into Produto(Nome, Descricao, Preco) values ('CoolBottle','Garrafa térmica que mantém temperatura por 12h',59.90);

select poder from Herois where Poder like '%c%';

select * from Herois order by Nome asc;
select * from Herois order by Nome desc;

update Herois set Poder = 'Teletransporte' where Id = 4;

alter table Produto
add Preco_Venda decimal(10,2);

select Nome,Preco from Produto where Preco < 100.00;

select * from Herois;
select * from Produto;
```
