#######################################################################
#Copyright (C) Olivier Dion <olivier.dion@polymtl.ca>		      #
#								      #
#This program is free software: you can redistribute it and/or modify #
#it under the terms of the GNU General Public License as published by #
#the Free Software Foundation, either version 3 of the License, or    #
#(at your option) any later version.				      #
#								      #
#This program is distributed in the hope that it will be useful,      #
#but WITHOUT ANY WARRANTY; without even the implied warranty of	      #
#MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the	      #
#GNU General Public License for more details.			      #
#								      #
#You should have received a copy of the GNU General Public License    #
#along with this program.  If not, see <http://www.gnu.org/licenses/>.#
#######################################################################


# Target
TARGET = howto

# Directories
IMG_DIR = img
MINTED_DIR = _minted-$(TARGET)

# Sources
SRC = $(shell echo *.tex)

# pdflatex
PDF = pdflatex
PDF_OPTS = \
-shell-escape -synctex=1 -interaction=nonstopmode

# Utils
RM = rm -rf

CLEAN = $(filter-out $(IMG_DIR) $(MINTED_DIR) makefile $(SRC), $(shell echo *))
CLEANER = $(MINTED_DIR)

all: $(TARGET).pdf

$(TARGET).pdf:
	@echo "PDF $(SRC) -> $@"
	@$(PDF) $(PDF_OPTS) $(SRC)

clean:
	@echo "CLEAN $(CLEAN)"
	@$(RM) $(CLEAN)

cleaner: clean
	@echo "CLEAN $(CLEANER)"
	@$(RM) $(CLEANER)

