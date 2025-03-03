# Zephyr Infra

## Descricao

O **Zephyr Infra** é o repositório responsável por armazenar a infraestrutura compartilhada entre os serviços da plataforma **Zephyr Platform**. Aqui estão definidos os arquivos de configuração, scripts e composições Docker necessárias para a orquestração dos serviços.

---

## 🚀 Componentes Principais

### 🛠️ Docker Compose

O `docker-compose.yml` contido neste repositório define a infraestrutura necessária para a execução dos serviços da plataforma. Ele inclui:

- **PostgreSQL**: Banco de dados para persistência de dados.
- **Zookeeper**: Serviço de coordenação para o Kafka.
- **Kafka**: Mensageria para troca de eventos entre os serviços.
- **Kafka Connect**: Integração do Kafka com o PostgreSQL para armazenamento de dados.
- **Volumes**: Persistência dos dados do PostgreSQL e Kafka.
- **Rede Docker**: Configuração para garantir a comunicação entre os contêineres.

### 📝 Configurações Compartilhadas

- **sink-config.json**: Arquivo de configuração do **Kafka Connect** para conectar o Kafka ao PostgreSQL.
- **.env**: Variáveis de ambiente utilizadas pelos serviços.
- **Scripts de inicialização**: Automatizam a criação de banco, tabelas e permissões no PostgreSQL.

---

## 🛠️ Como Utilizar

### 1. Clonar o Repositório

```bash
git clone https://github.com/marcuslira2/zephyr-infra.git
cd zephyr-infra
```

### 2. Subir a Infraestrutura

Para iniciar os serviços, utilize:
```bash
docker-compose up -d
```
Isso iniciará todos os componentes necessários para a execução dos microserviços.

### 3. Verificar Logs

Para acompanhar logs dos serviços:
```bash
docker-compose logs -f
```

### 4. Derrubar a Infraestrutura

Para parar e remover os contêineres:
```bash
docker-compose down -v
```
Isso remove também os volumes criados, garantindo um ambiente limpo para novos testes.

---

## 📝 Licença

Este projeto está sob a licença **MIT**. Fique à vontade para usar, modificar e contribuir!

---

## 📧 Contato
Caso tenha alguma dúvida ou sugestão, entre em contato via [GitHub Issues](https://github.com/marcuslira2/zephyr-infra/issues).

