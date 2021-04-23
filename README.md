# Envio de emails com alteração de imagens

## Descrição:

A função email_with_image faz a leitura do Google Sheets com as respostas do formulário do Card da Gratidão e faz o envio do email utilizando as APIs do [Sendgrid](https://sendgrid.com/) e [Imgbb](https://imgbb.com/).

## Requisitos

### Bibliotecas:

- gspread (Para leitura do Google Sheets)
- sendgrid (Para envio dos emails)
- premailer (Modifica o HTML para se adequar ao sendgrid)
- PIL (Manipulação de imagens)
- cv2 (Manipulação de imagens)
- pandas (Manipulação de tados tabelados)

### Env:

É necessário adicionar um arquivo com as chaves de acessos do Sendgrid e do Imgbb, essas chaves podem ser conseguidas através dos links dos dois serviços adicionadas na parte de descrição.

O arquivo `env.py` precisa receber essas chaves antes do script ser executado.

## Funcionalidade:

O script faz a leitura do Google Sheets, o tratamento de nomes para verificar possíveis problemas em formatação, cria a imagem mediante a escolha do card, faz o upload dessa imagem no imgbb e recebe o link localizando essa imagem na web, prepara o email com o HTML pré definido, inserindo a imagem e os nomes do remetente e destinatário nos devidos campos.
