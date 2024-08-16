<h1>
    <img align="center" width="40px" src="./docker-mark-blue.svg" alt="Docker logo">
    <span>Criando um Dockerfile para o Nginx</span>
</h1>

Repositório desenvolvido para fins educativos.

## Objetivo

Criar e executar um Dockerfile com a imagem do Nginx para realizar as seguintes tarefas:

- Copiar um arquivo index.html (https://viacep.com.br/exemplo/jquery/)
    
- Expor a porta 80

- Build do Dockerfile

- Executar o container com `docker run`

## Exemplo de Dockerfile

```
FROM nginx
COPY static-html-directory /usr/share/nginx/html/
EXPOSE 80
```

## Estrutura do projeto

Certifique-se de que o projeto tenha a seguinte estrutura:

```
.
├── Dockerfile
└── static-html-directory
    └── cep.html
```

## Instruções do Dockerfile

### Build da imagem

No diretório onde está o Dockerfile, execute:

```
sudo docker build -t rafaelmotadasilva/nginx .
```

### Execute o contêiner

```
sudo docker run -d -p 80:80 rafaelmotadasilva/nginx
```
