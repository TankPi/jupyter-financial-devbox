ARG VARIANT
FROM jupyter/${VARIANT}

USER root

RUN apt-get update && apt-get install -y --no-install-recommends \
    bash-completion \
    && rm -rf /var/lib/apt/lists/*

USER jovyan

RUN conda install pandas-datareader \
                    yfinance \
                    alpha_vantage \
                    quandl \
                    requests_cache
                    

RUN sed -i "s/# c.NotebookApp.token = .*/c.NotebookApp.token = ''/" /home/jovyan/.jupyter/jupyter_notebook_config.py

