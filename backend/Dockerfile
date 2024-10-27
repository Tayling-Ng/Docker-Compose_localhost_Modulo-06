# Imagem base
FROM python:3.10-slim

# Define a porta do backend (padrão 5000)
EXPOSE 5000

# Define o diretório de trabalho
WORKDIR /app

# Copia o código para o container 
COPY . .

# Instala dependências do Python 
RUN pip install -r requirements.txt

# Concede permissão de execução ao script wait-for-it.sh
RUN chmod +x ./wait-for-it.sh

# Define o comando padrão a ser executado quando o container é iniciado
CMD ["./wait-for-it.sh", "db:3306", "--timeout=120", "--", "python", "app.py"]