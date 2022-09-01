# Driver script
# Socorro Dominguez
# August 30, 2022

# This Makefile generates a report State of the DB.Rmd

# USAGE:

# From the command line.
# make all
#			Runs the Rmd file. Delivers a final report.

# Run the four scripts
all : StateoftheDB.html



# Creates document
StateoftheDB.html : StateoftheDB.Rmd 
	Rscript -e "rmarkdown::render('StateoftheDB.Rmd')"
