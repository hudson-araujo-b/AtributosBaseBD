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
