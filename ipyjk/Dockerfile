FROM p6steve/rakudo:scipy

LABEL maintainer="p6steve <p6steve@furnival.net>"
LABEL tag="p6steve/rakudo:ipyjk"

RUN    zef install https://github.com/niner/Inline-Python.git --exclude="python3"
RUN    zef install --/test Text::CSV
RUN    zef -v install git://github.com/bduggan/p6-jupyter-kernel.git
RUN    jupyter-kernel.raku --generate-config

#USER ${NB_UID}

ENTRYPOINT ["/bin/bash"]

#EXPOSE 8888
#CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
