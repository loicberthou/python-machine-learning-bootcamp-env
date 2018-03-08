FROM continuumio/anaconda3:5.1.0

RUN /opt/conda/bin/conda install jupyter -y --quiet
RUN mkdir -p /opt/notebooks/Python-Data-Science-and-Machine-Learning-Bootcamp
RUN mkdir /tmp/data
COPY ./Python-Data-Science-and-Machine-Learning-Bootcamp /opt/notebooks/Python-Data-Science-and-Machine-Learning-Bootcamp

CMD ["/opt/conda/bin/jupyter", "notebook", "--notebook-dir=/opt/notebooks", "--ip='*'", "--port=8888", "-y", "--no-browser", "--allow-root", "--NotebookApp.token=''"]
