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
