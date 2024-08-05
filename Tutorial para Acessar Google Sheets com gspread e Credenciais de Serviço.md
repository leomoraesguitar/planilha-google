# Tutorial para Acessar Google Sheets com gspread e Credenciais de Serviço

Este tutorial guia você pelo processo de configurar e acessar uma planilha do Google Sheets usando a biblioteca `gspread` em Python com credenciais de serviço.

## Pré-requisitos

- Conta Google
- Acesso ao Google Cloud Console
- Planilha do Google Sheets que você deseja acessar
- Python instalado no seu sistema
- Biblioteca `gspread` instalada

## Passo 1: Configurar o Projeto no Google Cloud Console

1. Acesse o [Google Cloud Console](https://console.cloud.google.com/).
2. Crie um novo projeto ou selecione um projeto existente.
3. Habilite a API Google Sheets:
   - Navegue até "APIs & Services" > "Library".
   - Pesquise por "Google Sheets API" e habilite-a.
   - Pesquise por "Google Drive API" e habilite-a também (necessário para permissões de leitura/escrita).

## Passo 2: Criar Credenciais de Serviço

1. No Google Cloud Console, vá para "APIs & Services" > "Credentials".
2. Clique em "criar credenciais" e selecione "Contas de serviço".
3. Preencha o Nome da conta de serviço  clique em "concluir".
4. Na seção "Contas de serviço", click em "Gerenciar contas de serviço".
5. Click no tr~es pontinhos do lado direito da conta criada e selecione "gerenciar chaves".
6. Click em "Adicionar Chave" e depois em "Criar nova chave".
7. Escolha "JSON" e click em "criar", isso fará o download do arquivo JSON para o seu computador
.

## Passo 3: Compartilhar a Planilha com a Conta de Serviço

1. Abra a planilha do Google Sheets que você deseja acessar.
2. Clique em "Compartilhar" no canto superior direito.
3. No campo de adicionar pessoas, insira o e-mail da conta de serviço (encontrado no arquivo JSON como `client_email`), ou na parte de crediciais vista anteriomente.
4. Defina as permissões conforme necessário (Leitor, Editor) e clique em "Enviar".
