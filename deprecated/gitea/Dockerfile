# https://docs.gitea.io/en-us/external-renderers/

FROM gitea/gitea

RUN apk --no-cache add \
    freetype \
    freetype-dev \
    gcc \
    g++ \
    libpng \
    python-dev \
    py-pip \
    python3-dev \
    py3-pip

RUN pip3 install --upgrade pip
RUN pip3 install -U setuptools
RUN pip3 install docutils

