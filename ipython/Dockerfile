FROM miniconda3

LABEL maintainer=@pwolter

RUN conda update conda && \
    conda install --quiet --yes ipython && \
    conda clean -tipy

CMD ["ipython"]
