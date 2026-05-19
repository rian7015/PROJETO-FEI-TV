# PROJETO-FEI-TV

FEI-TV

O FEI-TV é um sistema desenvolvido na linguagem Python com o objetivo de simular uma plataforma de gerenciamento e compartilhamento de informações sobre filmes e séries. O projeto foi inspirado em plataformas de streaming bastante conhecidas, como Netflix e YouTube, porém com foco apenas no gerenciamento das informações dos vídeos, sem realizar reprodução de mídia. Toda a aplicação funciona diretamente pelo terminal do computador e utiliza arquivos de texto para armazenar permanentemente todas as informações do sistema. Dessa forma, mesmo após o encerramento do programa, os dados permanecem salvos normalmente, garantindo persistência das informações cadastradas pelos usuários.O principal objetivo do projeto foi aplicar conceitos fundamentais da programação utilizando Python, como manipulação de arquivos, criação de funções, estruturas condicionais, estruturas de repetição, validação de dados e organização lógica do código. Além disso, o sistema foi desenvolvido utilizando programação estruturada, deixando o código mais organizado, limpo e de fácil manutenção.

FUNCIONAMENTO DO SISTEMA

O sistema inicia verificando automaticamente se os arquivos necessários para funcionamento do projeto existem na pasta do programa. Caso algum arquivo não exista, ele é criado automaticamente utilizando a biblioteca os.
Os arquivos utilizados pelo sistema são:

usuarios.txt //	Armazena usuários e senhas
videos.txt	// Armazena filmes e séries
curtidas.txt	/ /Armazena curtidas dos usuários
favoritos.txt	// Armazena playlists

Além da criação automática dos arquivos, o sistema também verifica se o arquivo videos.txt está vazio. Caso esteja, o programa adiciona automaticamente uma lista de filmes e séries já cadastrados.
Cada vídeo contém:

ID;
Título;
Descrição;
Ano de lançamento.

ORGANIZAÇÃO DO CÓDIGO

O projeto foi desenvolvido utilizando funções específicas para cada funcionalidade do sistema. Essa organização facilita o entendimento do código e melhora a manutenção do programa.
As principais funções implementadas foram:

Cadastro de usuários;
Login;
Listagem de vídeos;
Busca de vídeos;
Curtir vídeos;
Descurtir vídeos;
Ranking dos mais curtidos;
Gerenciamento de playlists.

Cada funcionalidade foi separada em blocos organizados utilizando comentários no código para facilitar a navegação e leitura.

CADASTRO E LOGIN DE USUÁRIOS

O sistema permite que novos usuários realizem cadastro utilizando nome de usuário e senha. Antes de concluir o cadastro, o programa verifica se o usuário já existe dentro do arquivo usuarios.txt. Isso evita registros duplicados no sistema. Após o cadastro, o usuário pode realizar login utilizando as credenciais cadastradas. O sistema realiza a leitura do arquivo de usuários e compara os dados digitados com as informações armazenadas. Caso os dados estejam corretos, o acesso ao menu principal é liberado.

LISTAGEM E BUSCA DE VÍDEOS

Após o login, o usuário possui acesso à funcionalidade de listagem de vídeos. O sistema exibe todos os filmes e séries cadastrados mostrando:

ID;
Título;
Descrição;
Ano de lançamento;
Quantidade de curtidas.

O projeto também possui um sistema de busca que permite pesquisar vídeos utilizando parte do nome digitado pelo usuário. A busca percorre automaticamente todos os vídeos cadastrados e exibe apenas os resultados encontrados.

SISTEMA DE CURTIDAS

O FEI-TV possui um sistema completo de curtidas permitindo interação dos usuários com os vídeos cadastrados.Quando um usuário curte um vídeo, o sistema salva a informação no arquivo curtidas.txt. Cada curtida registra o nome do usuário junto ao ID do vídeo curtido.

O sistema também possui importantes validações:

Um usuário não pode curtir o mesmo vídeo duas vezes;
Um usuário só pode descurtir vídeos que já tenha curtido anteriormente.

Essas validações garantem maior controle e integridade das informações armazenadas.

RANKING DOS MAIS CURTIDOS

Outra funcionalidade importante implementada foi o ranking automático dos vídeos mais curtidos. O sistema percorre todos os vídeos cadastrados, calcula a quantidade de curtidas de cada um e organiza os resultados em ordem decrescente. Dessa forma, os vídeos mais populares aparecem nas primeiras posições do ranking. Essa funcionalidade deixa o sistema mais dinâmico e interativo.

SISTEMA DE PLAYLISTS

O projeto também possui um sistema de playlists permitindo que os usuários criem listas personalizadas de vídeos favoritos.
As funcionalidades disponíveis são:

Criar playlists;
Adicionar vídeos favoritos;
Remover vídeos favoritos;
Visualizar playlists;
Excluir playlists.

Antes de adicionar um vídeo à playlist, o sistema verifica se o ID informado realmente existe no cadastro de vídeos. Isso evita erros e garante maior segurança das informações armazenadas. Todas as playlists ficam armazenadas no arquivo favoritos.txt.

PERSISTÊNCIA DE DADOS

Uma das principais características do FEI-TV é a persistência de dados. Como todas as informações ficam armazenadas em arquivos .txt, os dados continuam salvos mesmo após o encerramento do sistema. Assim, usuários cadastrados, curtidas, favoritos e playlists permanecem disponíveis quando o programa é executado novamente. Essa funcionalidade torna o sistema mais próximo de aplicações reais que utilizam armazenamento permanente de informações.
