# Padrão de Nomes de Arquivos

## Vantagens

Os benefícios de seguir o versionamento semântico são inúmeros, destancando-se:

* é possível dizer do que se trata o arquivo só pelo nome;
* fica mais fácil e rápido achar arquivos;
* diminui ambiguidade e a margem para erros e mal-entendidos. *"A versão que está valendo é a 1.2.1"* é muito mais claro que *"A versão que está valendo é a alterado*azul22"*;
* facilita muito buscas no sistema operacional ou gerenciadores de arquivos
* facilitar o entendimento qual mudança foi feita, quando, por quem e por quê

## Sumário

Nomes de arquivos e suas extensões **DEVEM** ser escritos:

- em caracteres minúsculos (caixa baixa). e.g. nomedearquivo.txt;
- sem espaço, com o hífen substituindo espaços em branco. e.g nome-de-arquivo.txt;
- com a primeira parte (o nome) descritiva, com especificidade crescente: do mais geral, para o mais específico. e.g. cliente-projeto-entregavel.txt
- com número de versão composto de 3 grupos de números, seguindo regras de versionamento semântico com o primeiro grupo especificando **CONCEITO**, o segundo MUDANÇAS dentro da um mesmo conceito e o terceiro grupos indicando CORREÇÕES dentro de um mesmo grupo de mudanças. e.g. cliente-projeto-entregavel.1.0.1.txt

Preferencialmente, nomes de arquivo **DEVERIAM** ser escritos:
- sem acentuação ou caracteres especiais. e.g. cliente-projeto-documentacao.1.0.0;
- sem abreviações, exceto as que sejam definidas e entendidas por todo o time;

## Padrão 

Dado um nome de arquivo no padrão NOME-DO-ARQUIVO.VERSÃO.EXTENSÃO, defini-se as seguintes partes de nomes de arquivos:

1. NOME-DO-ARQUIVO (e.g. cliente-projeto-entregavel )
2. VERSÃO (e.g. 1.1.2)
3. EXTENSÃO (e.g. .txt)

### Nome do Arquivo

#### Utilize caracteres minúsculos

Nomes de arquivos **DEVEM** ser escritos utilizando caracteres minúsculos (caixa baixa).

Alguns sistemas operacionais e programas são sensíveis à diferenças de "caixa". Isto é,  o arquivo com Nome1.txt é diferente de um arquivo com nome1.txt . Utilizar apenas uma forma evita ambiguidades e erros, e como caracteres em caixa baixa tem melhor ergonomia visual [1] e facilita a leitura, esta forma deve ser usada. 

Exemplo e.g. nome-de-arquivo.txt;

#### Não utilize espaços em branco

Nomes de arquivos **DEVEM** ser escritos sem espaços em branco.

Alguns sistemas, especialmente alguns servidores de sites mais antigos, têm dificuldade em lidar com espaços em brancos. Alguns não leêm o restante do nome, outros trocam por _ (*underscore*), entre outros possíveis problemas.

Um exemplo comum são capturas de tela produzidas em sistemas Apple MacOs, cujo padrão é similiar a "Captura de Tela 2017-04-20 às 09.07.50.jpg" . Embora o MacOs entenda perfeitamente os espaços em branco, muitos servidores de sites não entendem e não encontram o arquivo.

Por esta razão, os nomes de arquivos devem ser escritos sem espaços em branco, que devem ser substuídos por "-"(hífen)

Nota: o mesmo problema pode acontecer com caracteres especiais e acentuados como ã, ç, etc. Entretanto, o suporte a caracteres especiais é mais comum do que espaços em branco e o problema acontece com menos frequência. Ainda que o padrão não proíba o uso de caracteres especiais, aconselhamos que seja evitado, como visto adiante neste documento

#### Termos descritivos e em ordem de especificidade

Nomes de arquivos **DEVEM** ser descritivos e seguir ordem de especificidade.

A fim de facilitar o entendimento do conteúdo do arquivo sem que seja necessário arquivo, e também facilitar buscas por arquivo, os arquivos devem ter nomes descritivos e seguir uma ordem crescente de especificidade crescente.  

Os termos e as regras específicas varia conforme empresa, projeto ou caso, mas sempre seguindo especificidade: a primeira parte tem escopo geral, a segunda é mais específica, e assim por diante.

Por exemplo, em caso de documentos e arquivos de projetos, pode-se utilizar o padrão cliente[-projeto]-entregavel, sendo a parte entre chaves [] opcional. e.g. 2aces-site-layout.1.2.1.ai

Partindo do exemplo anterior, caso o projeto possua uma abreviação ou código e todos no time tenham conhecimento do código, é aceitável também usar códigocliente[-projeto]-entregavel-versao. e.g. 2a-site-layout-.1.2.1.ai

Com arquivos e documentos que não são de clientes e projetos específicos, prefira uma sequência lógica do mais geral para o mais específico, incluindo o uso de datas. Um log ou diário poderia utilizar o nome diario-20170420.txt

#### Evite acentuação e caracteres especiais

Preferencialmente, nomes de arquivo **DEVERIAM** ser escritos sem acentuação ou caracteres especiais. e.g. cliente-projeto-documentacao.1.0.0.txt.

Assim como no caso de espaços em brancos, diversos sistemas, principalmente servidores de sites mais antigos, não conseguem lidar com estes caracteres. Novamente, um exemplo comum são capturas de tela produzidas em sistemas Apple MacOs, cujo padrão é similiar a "Captura de Tela 2017-04-20 às 09.07.50.jpg", que contém um "à" que pode não ser entendido e gerar erros.

#### Evite abreviações

Nomes de arquivo **DEVERIAM** ser escritos sem abreviações, exceto as que sejam definidas e entendidas por todo o time, para evitar ambiguidade. 

TODO: exemplos de ambiguidade com abreviações em buscas por arquivos


### Versão do Arquivo

O versionamento de arquivos e documentos é inspirado pelo Versionamento Semântico de software ( http://semver.org/lang/pt-BR/ ) e outras práticas.

A versão deve ser indicada por 3 números precedidos e separados por ponto (e.g. 1.2.1), entre o nome do arquivo e sua extensão. Cada grupo de número tem um significado diferente, do mais geral para o mais específico:

- o primeiro número significa CONCEITO;
- o segundo número significa MUDANÇA;
- o terceiro número significa CORREÇÃO;

Qualquer número utilizado em versão DEVE ser inteiro, NÃO DEVE ser negativo, e NÃO DEVE conter zeros à esquerda e cada elemento DEVE aumentar numericamente. Por exemplo: 1.9.0 -> 1.10.0 -> 1.11.0.

Incremente o primeiro número apenas quando mudar o CONCEITO ou abordagem para o documento (ou imagem, ou planilha, ou lay-out, etc). Se a versão é rascunho, trabalho em progresso, e não uma versão oficial ou acabada, utilize 0 (zero).

Incremente o número do meio quando é MUDANÇA ou aperfeiçoamento dentro de um documento: uma nova seção, novos gráficos, novas fotografias, etc.

Incremente o último da direita quando fizer CORREÇAO (revisão de texto, corrigir número ou informação errada, etc),

#### Exemplo de versionamento

Considere uma pasta com diversos arquivos PDFs com o lay-outs de um site:


Se ainda não foi apresentado para o cliente e está na 6a versão de rascunho (sem considerar correções) teria versão 0.6.0 (e.g. 2aces-site-layout.0.6.0.pdf).

Se for feita uma correção (e.g. corrigir de fodografia para fotografia) neste mesmo lay-out, teria versão 0.6.1 (e.g. 2aces-site-layout.0.6.1,pdf)

No momento em que o arquivo é considerado pronto para envio para o cliente, ele se torna 1.0.0. Se antes de enviar for feita uma correção no logo do site , se torna 1.0.1. 

Se depois de enviado ao cliente, este pede algumas pequenas alterações, esta primeira versão pós alterações se torna 1.1.0. Caso passe por uma segunda alteração, 1.2.0. Caso esta versão sofra revisões ou correções, se torna 1.2.1, 1.2.2, etc.

Caso sejam criados lay-outs totalmente diferentes ou decida-se apresentar alternativas para a cliente escolher, estas versões seriam CONCEITOS diferentes e teriam números diferentes. (e.g. 2aces-site-layout.2.0.0, 2aces-site-layout.3.1.2,pdf, etc)
