# REMEMBER to restart R after you modify and save this file!
source("renv/activate.R")

library(ggplot2)
library(blogdown)

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

# Define custom ggplot theme
my_theme <- function(){
    
    # Replace elements we want to change
    theme_minimal() %+replace%
        
        theme(
            panel.grid.major = element_line(color = "gray90", size = .2),
            axis.title.y = element_text(angle = 0, vjust = .5)
            ,strip.text = element_text(size = 12)
        )
}

# Set to custom theme
theme_set(my_theme())
