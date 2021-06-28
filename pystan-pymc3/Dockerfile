# python3をベースにする
FROM python:3

RUN apt-get update
# RUN pip install --upgrade pip
RUN pip3 install --upgrade pip setuptools
RUN pip3 install jupyterlab matplotlib pystan pymc3 seaborn
RUN jupyter serverextension enable --py jupyterlab

# 作業ディレクトリを指定
WORKDIR /workdir

# コンテナ側のポート番号
EXPOSE 8888

ENTRYPOINT ["jupyter-lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]

# Jupyterlabのルートとなるディレクトリを指定
CMD ["--notebook-dir=/workdir"]
