# Padrão de Nomes de Arquivos

## Vantagens

Os benefícios de seguir o versionamento semântico são inúmeros, destancando-se:

* é possível dizer do que se trata o arquivo só pelo nome;
* fica mais fácil e rápido achar arquivos;
* diminui ambiguidade e a margem para erros e mal-entendidos. _"A versão que está valendo é a 1.2.1"_ é muito mais claro que _"A versão que está valendo é a alterado_azul22"_;
* facilita muito buscas no sistema operacional ou gerenciadores de arquivos
* facilitar o entendimento qual mudança foi feita, quando, por quem e por quê

## Sumário

Nomes de arquivos e suas extensões **DEVEM** ser escritos:

- em caracteres minúsculos (caixa baixa). e.g. nomedearquivo.txt;
- sem espaço, com o hífen substituindo espaços em branco. e.g nome-de-arquivo.txt;
- com a primeira parte (o nome) descritiva, com especificidade crescente: do mais geral, para o mais específico. e.g. cliente-projeto-entregavel.txt
- com número de versão composto de 3 grupos de números, seguindo regras de versionamento semântico com o primeiro grupo especificando CONCEITO, o segundo MUDANÇAS dentro da um mesmo conceito e o terceiro grupos indicando CORREÇÕES dentro de um mesmo grupo de mudanças. e.g. cliente-projeto-entregavel.1.0.1.txt

Preferencialmente, nomes de arquivo **DEVERIAM** ser escritos:
- sem acentuaço ou caracteres especiais. e.g. cliente-projeto-documentacao.1.0.0;
- sem abreviações, exceto as que sejam definidas e entendidas por todo o time;

## Padrão 

Dado um nome de arquivo no padrão NOME-DO-ARQUIVO.VERSÃO.EXTENSÃO, defini-se as seguintes partes de nomes de arquivos:

1. NOME-DO-ARQUIVO (e.g. cliente-projeto-entregavel )
2. VERSÃO (e.g. 1.1.2)
3. EXTENSÃO (e.g. .txt)

### Nome

