# NEX'MAP PWA — publicação pelo GitHub

Este pacote contém a versão atual do NEX'MAP, com instalação PWA e funcionamento off-line para consulta dos dados já sincronizados.

## 1. Criar o repositório

1. Entre em https://github.com/new
2. Informe um nome, por exemplo `nexmap-pwa`.
3. Crie o repositório sem adicionar README, licença ou `.gitignore`.
4. Na página do repositório, escolha **uploading an existing file**.
5. Envie todo o conteúdo desta pasta — não envie apenas o arquivo ZIP.
6. Confirme em **Commit changes**.

## 2. Hospedagem necessária

O GitHub guarda o código, mas o NEX'MAP possui banco de dados e rotas de servidor. Por isso, o GitHub Pages sozinho não executa o aplicativo completo. Conecte o repositório a uma hospedagem compatível com Cloudflare Workers e D1.

Configuração de compilação:

- Node.js: `22.13` ou superior
- instalação: `npm ci`
- compilação: `npm run build`
- variável protegida: `MANAGEMENT_PASSWORD`

Nunca escreva a senha do modo gestor dentro dos arquivos do GitHub. Cadastre-a somente nas variáveis protegidas da hospedagem.

## 3. Instalar no celular

1. Abra o endereço HTTPS publicado no Chrome.
2. Entre no modo técnico.
3. Toque em **Instalar app** ou, no menu do navegador, em **Adicionar à tela inicial**.
4. Antes de trabalhar em um local sem sinal, abra o app conectado e visualize a região do mapa que será usada.

## Recursos PWA incluídos

- manifesto de instalação;
- ícones de 192 px e 512 px;
- service worker;
- abertura em tela independente;
- cache da interface, das CTOs sincronizadas e dos mapas já visualizados;
- identificação automática dos ramais e cores diferentes por ramal.

