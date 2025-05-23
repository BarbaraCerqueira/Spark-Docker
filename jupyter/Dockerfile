FROM bitnami/spark:3.5.5

USER root

# Instalar dependências necessárias para o Jupyter Notebook e PySpark
RUN apt-get update && apt-get install -y python3-pip && \
    pip3 install --upgrade pip && \
    pip3 install jupyter pyspark==3.5.5

EXPOSE 8888

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]
