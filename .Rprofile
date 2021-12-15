# REMEMBER to restart R after you modify and save this file!
source("renv/activate.R")

library(dplyr)
library(ggplot2)
library(forcats)
library(purrr)
library(brms)
library(feather)
library(blogdown)
library(sysfonts)
library(showtext)

# Now set options to customize the behavior of blogdown for this project. Below
# are a few sample options; for more options, see
# https://bookdown.org/yihui/blogdown/global-options.html
options(
  # to automatically serve the site on RStudio startup, set this option to TRUE
  blogdown.serve_site.startup = FALSE,
  # to disable knitting Rmd files on save, set this option to FALSE
  blogdown.knit.on_save = TRUE,
  # build .Rmd to .html (via Pandoc); to build to Markdown, set this option to 'markdown'
  blogdown.method = 'html'
)

# Set Hugo version
options(blogdown.hugo.version = "0.87.0")

# Stan options
# rstan_options(auto_write = FALSE)
# options(mc.cores = parallel::detectCores())

# Get Monda font from Google and make available in ggplots
font_add_google(name = "Monda", family = "Monda")
showtext_auto()

# Define custom ggplot theme
my_theme <- function(){
    
    # Replace elements we want to change
    theme_classic() %+replace%
        
        theme(
            panel.grid.major = element_line(color = "gray90", size = .2),
            panel.spacing = unit(2, "lines"),
            axis.title.y = element_text(angle = 0, vjust = .5,
                                        
                                        # Increase axis title's right margin
                                        margin = margin(r = 5))
            
            # Increase font sizes & set font
            ,strip.text = element_text(size = 14),
            axis.title = element_text(size = 13),
            axis.text = element_text(size = 11),
            legend.title = element_text(size = 13),
            legend.text = element_text(size = 11),
            text = element_text(family = "Monda")
        )
}

# Set to custom theme
theme_set(my_theme())

# Solve a conflict with filter()
filter <- dplyr::filter
