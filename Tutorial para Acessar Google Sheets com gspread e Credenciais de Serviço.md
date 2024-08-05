Tutorial para Acessar Google Sheets com gspread e Credenciais de Serviço
## Este tutorial guia você pelo processo de configurar e acessar uma planilha do Google Sheets usando a biblioteca gspread em Python com credenciais de serviço.

Pré-requisitos
Conta Google
Acesso ao Google Cloud Console
Planilha do Google Sheets que você deseja acessar
Python instalado no seu sistema
Biblioteca gspread instalada
Passo 1: Configurar o Projeto no Google Cloud Console
Acesse o Google Cloud Console.
Crie um novo projeto ou selecione um projeto existente.
Habilite a API Google Sheets:
Navegue até "APIs & Services" > "Library".
Pesquise por "Google Sheets API" e habilite-a.
Pesquise por "Google Drive API" e habilite-a também (necessário para permissões de leitura/escrita).
Passo 2: Criar Credenciais de Serviço
No Google Cloud Console, vá para "APIs & Services" > "Credentials".
Clique em "Create Credentials" e selecione "Service Account".
Preencha os detalhes da conta de serviço e clique em "Create".
Na seção "Service account permissions", selecione "Project" > "Editor" (ou o papel que você achar adequado).
Clique em "Done" após a criação da conta de serviço.
Na lista de contas de serviço, clique na conta recém-criada e depois em "Add Key" > "Create New Key".
Selecione o formato JSON e clique em "Create". Isso fará o download do arquivo JSON para o seu computador.
Passo 3: Compartilhar a Planilha com a Conta de Serviço
Abra a planilha do Google Sheets que você deseja acessar.
Clique em "Compartilhar" no canto superior direito.
No campo de adicionar pessoas, insira o e-mail da conta de serviço (encontrado no arquivo JSON como client_email).
Defina as permissões conforme necessário (Leitor, Editor) e clique em "Enviar"
