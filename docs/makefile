RmdFiles := $(wildcard *.Rmd)
HtmlFiles := $(patsubst %.Rmd,%.html,$(RmdFiles))

default: $(HtmlFiles)
	echo $(HtmlFiles)
	@echo All updated
index.html: index.Rmd makefile arduino.css $(HtmlFiles)
	R -e "rmarkdown::render('$<')"
indice.html: indice.Rmd makefile arduino.css $(HtmlFiles)
	R -e "rmarkdown::render('$<')"
%.html: %.Rmd makefile arduino.css
	R -e "rmarkdown::render('$<')"
