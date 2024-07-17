# WordPress com Docker e Banco de Dados Externo

### Visão Geral
Este projeto visa configurar uma instância do WordPress utilizando Docker, com a particularidade de conectar-se a um banco de dados MySQL externo. A implementação tem como objetivo proporcionar um ambiente isolado e facilmente replicável para o desenvolvimento e teste de sites em WordPress.

### Tecnologias Utilizadas
 - Docker: Para criar e gerenciar containers que isolam o ambiente do WordPress.
 - Docker Compose: Para definir e executar múltiplos containers com um arquivo de configuração YAML.
 - WordPress: Plataforma de gerenciamento de conteúdo (CMS) amplamente utilizada.
 - MySQL: Sistema de gerenciamento de banco de dados relacional, já existente e acessado remotamente.

### Estrutura do Projeto
 - docker-compose.yml: Arquivo de configuração que define o serviço do WordPress e suas dependências.
 - Variáveis de Ambiente: Configurações do banco de dados externo são passadas como variáveis de ambiente no docker-compose.yml.

### Fluxo de Trabalho

1 - Preparação do Ambiente:
 - Certifique-se de que o Docker e o Docker Compose estão instalados no sistema.
 - Tenha um banco de dados MySQL externo ou local, configurado e acessível.

O arquivo docker-compose.yml é configurado para iniciar um container do WordPress que se conecta ao banco de dados externo, utilizando as informações de host, usuário e senha apropriadas.

2 - Execução do Projeto:
 - Execute o comando ```docker-compose up -d``` no terminal para iniciar o container do WordPress.
 - Acesse o WordPress através do navegador em [http://localhost:8000](http://localhost:8000) para configurar o site.


### Considerações de Segurança
 - Assegurar que o banco de dados externo permite conexões remotas apenas de IPs autorizados.
- Utilizar senhas fortes e práticas recomendadas para configuração de usuários no banco de dados.

### Benefícios
 - Isolamento: O uso de Docker proporciona um ambiente isolado, evitando conflitos com outras aplicações.
 - Facilidade de Configuração: O Docker Compose permite configurar rapidamente o ambiente com um simples comando.
 - Escalabilidade: A configuração pode ser facilmente replicada em outros ambientes de desenvolvimento ou produção.

### Conclusão
Este projeto demonstra uma abordagem eficaz para implementar um site WordPress utilizando Docker, facilitando o gerenciamento e a escalabilidade enquanto utiliza um banco de dados externo para persistência de dados.
