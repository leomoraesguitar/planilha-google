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
2. Clique em "Create Credentials" e selecione "Service Account".
3. Preencha os detalhes da conta de serviço e clique em "Create".
4. Na seção "Service account permissions", selecione "Project" > "Editor" (ou o papel que você achar adequado).
5. Clique em "Done" após a criação da conta de serviço.
6. Na lista de contas de serviço, clique na conta recém-criada e depois em "Add Key" > "Create New Key".
7. Selecione o formato JSON e clique em "Create". Isso fará o download do arquivo JSON para o seu computador.

## Passo 3: Compartilhar a Planilha com a Conta de Serviço

1. Abra a planilha do Google Sheets que você deseja acessar.
2. Clique em "Compartilhar" no canto superior direito.
3. No campo de adicionar pessoas, insira o e-mail da conta de serviço (encontrado no arquivo JSON como `client_email`).
4. Defina as permissões conforme necessário (Leitor, Editor) e clique em "Enviar".
