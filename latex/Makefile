.PHONY: resume cv coverletter clean

CC=xelatex
RESUME_SRCS=$(shell find resume -name '*.tex')
CV_SRCS=$(shell find cv -name '*.tex')

resume: 
	$(CC) -output-directory=/outputs ./resume.tex $(RESUME_SRCS) 

cv: 
	$(CC) -output-directory=/outputs ./cv.tex $(CV_SRCS) 

coverletter: 
	$(CC) -output-directory=/outputs ./coverletter.tex

