FROM continuumio/miniconda3

RUN apt-get update
RUN apt-get install -y build-essential
RUN git clone --depth 1 https://github.com/fanzheng10/CliXO-1.0 clixo
WORKDIR "/clixo"
RUN rm -f clixo clustersToDAG
RUN make clean all
RUN mkdir /tmp/cdclixo
COPY dist/*.whl /tmp/cdclixo

RUN /opt/conda/bin/pip install /tmp/cdclixo/cdclixo*whl

RUN rm -rf /tmp/cdclixo

ENTRYPOINT ["/opt/conda/bin/cdclixocmd.py"]
CMD ["--help"]
