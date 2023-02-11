ARG VARIANT
FROM jupyter/${VARIANT}

RUN conda install pandas-datareader \
                    yfinance \
                    alpha_vantage \
                    quandl
                    

RUN sed -i "s/# c.NotebookApp.token = .*/c.NotebookApp.token = ''/" /home/jovyan/.jupyter/jupyter_notebook_config.py

