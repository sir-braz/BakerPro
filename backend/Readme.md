### 🚀 Rodando o Backend com Docker Compose

Para facilitar a inicialização do backend junto com o banco de dados, utilizamos o **Docker Compose**. Siga os passos abaixo para rodar o projeto:

---

### **📌 Pré-requisitos**
Antes de continuar, certifique-se de ter instalado:
- **Docker** 🐳 → [Instalar Docker](https://docs.docker.com/get-docker/)
- **Docker Compose** 📦 → [Instalar Docker Compose](https://docs.docker.com/compose/install/)

---

### **🔧 Passos para Execução**

1. **Clone o repositório** (se ainda não fez isso):
   ```bash
   git clone https://github.com/sir-braz/PaoFacil.git
   cd PaoFacil/backend
   ```

2. **Suba os containers com Docker Compose**:
   Caso você queira subir a aplicação (backend + banco de dados), execute o comando abaixo:
   ```bash
   sudo docker-compose up --build
   ```
   📌 O parâmetro `--build` garante que as imagens do Docker sejam reconstruídas, caso haja alguma alteração no código ou na configuração.

3. **Aguarde a inicialização dos containers**. Após alguns instantes, o backend estará rodando em:
   ```
   http://localhost:8080
   ```

4. **Para parar os containers**, pressione `CTRL + C` ou execute:
   ```bash
   sudo docker-compose down
   ```



### **🐳 Estrutura do Docker Compose**

O **Docker Compose** é responsável por subir dois containers:
- **Backend** (`paofacil-backend`) → API desenvolvida em **Java + Spring Boot**.
- **Banco de Dados** (`paofacil-db`) → **PostgreSQL** como banco de dados relacional.

Caso precise verificar se os containers estão rodando, use:
```bash
sudo docker ps
```

Se precisar remover todos os containers (em caso de falha ou para reiniciar o ambiente):
```bash
sudo docker rm -f $(sudo docker ps -aq)
```


