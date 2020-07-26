# Base container provided by Jupyter Development Team and is distributed under their terms of the Modified BSD License.
ARG BASE_CONTAINER=jupyter/scipy-notebook
FROM $BASE_CONTAINER

LABEL maintainer="Descript data <tyson@descriptdata.com>"

USER $NB_UID

# Install Python 3 NLP packages
RUN pip install spacy
RUN conda install --quiet --yes \
	'nltk=3.4.*' \
	'gensim=3.8.*' \
	&& \
    conda clean --all -f -y



RUN python -c "import nltk; nltk.download('popular')"
RUN python -m spacy download en_core_web_lg
