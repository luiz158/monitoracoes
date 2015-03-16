# Sistema de Monitoramento de Ações #

## Como configurar o Banco de Dados para a Aplicação ##

### Instruções passo a passo: ###

  1. Clique “Iniciar -> Programas -> PostGreSQL 8.2 -> pgAdmin III “. Depois, selecione a opção “localhost”, clique com o botão direito e então “Connect”. http://monitoracoes.googlecode.com/svn/trunk/docs/images/ConfigurarPostgres/Passo_1_Conectar_Postgres.JPG
  1. Selecione a opção “Localhost -> Database(1)”,e clique com o botão direito em "New Database...", digite "cotacoes" e depois clique "OK". http://monitoracoes.googlecode.com/svn/trunk/docs/images/ConfigurarPostgres/Passo_3_Criar_Banco.JPG
  1. Após criar o banco de dados "cotacoes", selecione a opção na árvore da esquerda “Localhost -> Database(2) -> cotacoes ”.
  1. Então clique na opção “Tools -> Query Tool” no menu. Desta forma, uma nova janela abrirá para executar os comandos de criação e configuração do Banco de Dados.
  1. **Copie** o conteúdo do [script de criação do banco](WikiScriptCriacao.md) e **cole** o conteúdo do arquivo na ferramenta “Query Tool” e execute o script em “Query -> Execute”. http://monitoracoes.googlecode.com/svn/trunk/docs/images/ConfigurarPostgres/Passo_2_Executar_Scripts.JPG
  1. 4.	Se tudo ocorrer corretamente a seguinte mensagem é mostrada (conforme a figura acima):
```
NOTICE:  ALTER TABLE / ADD PRIMARY KEY will create implicit index "cotacao_pk" for table "cotacao"
NOTICE:  ALTER TABLE / ADD PRIMARY KEY will create implicit index "planilha_pk" for table "planilha"

Query returned successfully with no result in 297 ms
```

[Voltar](PaginaInicial.md)