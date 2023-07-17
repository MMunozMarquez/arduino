RmdFiles := $(wildcard *.Rmd)
HtmlFiles := $(patsubst %.Rmd,%.html,$(RmdFiles))

default: $(HtmlFiles)
	echo $(HtmlFiles)
	@echo All updated
%.html: %.Rmd makefile arduino.css
	R -e "rmarkdown::render('$<')"
