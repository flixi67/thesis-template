# Thesis Template

Credits to this go mostly to [Flori F](https://github.com/FloriF/thesis-template). His version was adapted to fit the requirements of a B.A. or M.A. thesis at the Department for Political Science and Administration @ Uni Konstanz.

In general, this template can be used for any thesis or  large report, based on `.Rmd`-files and with some technical knowledge highly adaptable.

## Basic Usage

### Main usage
1. Define the sections of your thesis in the main file, `thesis.Rmd`.
2. Add the content of each page in the content folder. For every main section, there exists a separate `.Rmd`-file.
3. You can directly include scripts to run in `R`. The data of the experiment was in the data folder. Using the settings print_analysis and print_analysis_results you can decide if you want your analyses printed in your document. I found this useful for testing.
4. At any place in the document, you can access the variables from such a script like shown in the discussion section. This is onnly possible because the scripts are written in RMardown. But it is very easy to change any R script into a valid `.Rmd` file.
5. To create the final output, knit `thesis.Rmd`.

### Citing
1. To cite a source, you add the `BibTex` entry to the `references.bib` file
2. The citing syntax is straightforward. Use @key or [@key, p. 1] for in-text citations, the reference list will be created automatically accordingly.

## Notes

This is not yet a full documentation of this template, this is rather just the rough and dirty skeleton of my thesis. However, if you ever worked with LaTeX, you can adapt everything. You could also set keep_latex: true, so you can manually adjust everything that does not look right.

Since knitting/using RMarkDown requires you to have a LaTeX-Distribution installed, I recommend MikTex. It allows you to install every package you may need (and that you do not yet have installed) to be downloaded and installed automatically, and it can even ask you to decide on each package on its own.

You might want to add/remove some `\newpage` commands at the beginning to correctly position the pages on the left/right side of a page.

You can edit anything. You can add/remove sections, title pages, etc. 

Styling of the title page happens in style/title.sty (I wanted a very beautiful title page, so I had to do this in Tex and not in Markdown. You can of course decide to use a markdown title page.)

Should be able to be knitted via the 'Knit' button in RStudio or using 
`rmarkdown::render('thesis.Rmd', output_format = 'pdf_document', encoding = 'UTF-8')`. **Please try this before you start using this template!** At some point I will add a script or something similar to do this for you. I set up Sublime Text 3 (the text editor I use) to recompile the whole stuff by pressing 'CTRL + B' while editing the thesis.Rmd file.