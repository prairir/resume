build:
	FROM ubuntu:22.04

	# install dependencies
	RUN apt-get update -yqq && \
		DEBIAN_FRONTEND="noninteractive" apt-get install -yqq \
			texlive-latex-extra \
			texlive-fonts-extra \
			texlive-bibtex-extra \
			biber \
			texlive-latex-base \
			texlive-luatex

	WORKDIR /resume
	RUN cd /resume

	ARG file

	COPY --dir components ./

	COPY $file.tex .

	RUN lualatex -interaction=nonstopmode -halt-on-error $file.tex

	SAVE ARTIFACT $file.pdf AS LOCAL $file.pdf
