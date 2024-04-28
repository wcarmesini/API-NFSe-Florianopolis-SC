## API NFS-e Florianopolis-SC | Iniciando o projeto 🚀 

Aplicação desenvolvida em PHP para consumir API de notas fiscais da Prefeitura de Florianópolis - SC.

Neste estágio inicial de desenvolvimento (v0.1.0), nossa aplicação já está operacional com algumas funcionalidades básicas. No entanto, estamos apenas começando e há uma série de aprimoramentos e implementações planejadas.

O objetivo deste projeto é tornar o processo de gerenciamento de notas fiscais mais eficiente e acessível, oferecendo uma solução fácil de usar para os negócios e cidadãos de Florianópolis.

## Funcionalidades operacionais na versão 0.1.0

- Emissão de nota fiscal
- Consulta de notas fiscais (todas as notas ou utilizando alguns parâmetros)
- Validação de XML de nota fiscal
- Download de XML da nota fiscal

## Algumas Funcionalidades em vista para a próxima versão

- Emissão de nota fiscal simplificada e substituta
- Cancelamento de nota fiscal
- Filtros e parâmetros adicionais na consulta de notas fiscais

## Como utilizar a nossa aplicação?

1. Vá em **app>config.php** e preencha as informações necessárias.

```bash

// Credenciais de autenticação da aplicação
// Para geração das credenciais de integração deve-se acessar este link: https://nfps-e.pmf.sc.gov.br/frontend/#!/credenciais-integracao
// As credenciais serão recebidas em sua caixa de e-mail. 
$client_id = '...';
$client_secret = '...';

// Informações do usuário auntenticado
$user_cmc = "..."; // Número da Inscrição Municipal
$user_aedf = "..."; // Número da AEDF (Autorização para Emissão de Nota Fiscal)
$password = '...'; // Senha de acesso ao sistema de emissão de notas fiscais

// Informações do certificado digital
$pfxFile = 'data/certificados/certificado.pfx'; // Caminho do certificado digital
$pfxPassword = '...'; // Senha do certificado digital

```

2. Faça a requisição do arquivo de funções e aproveite as funcionalidades!

```bash

// Faz a inclusão das funções da aplicação
require 'app/functions.php';

// Chama a função para obter as notas fiscais
$notas = getNotasFiscais();

// Exibe o resultado na tela
echo "<pre>";
print_r($notas);
echo "</pre>";


```
