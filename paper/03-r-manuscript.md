# Data Skills - Week 4 - Lab

> Graham Bishop

## Background

This directory contains a partial manuscript published in Current Biology by Benjamin M. Van Doren et al.

[Link to paper](https://www.sciencedirect.com/science/article/abs/pii/S0960982224017019)

The manuscript was written entirely with R and Quarto. Some additional files (e.g., supplementary materials and custom formatting code) are not included here for simplicity.

## Step 1

Open main_text.qmd in RStudio. Install any packages as prompted and click "Render." The manuscript should generate and appear as an html file in your web browser. Inspect the html file that opens in your browser.

*Q1. Add your name to the author list by editing the YAML header in main_text.qmd. Render the file to confirm that it worked. Copy and paste the entire YAML header below (between the ---):*

> YOUR ANSWER

## Step 2 - Citations

*Q2. Track down the file that contains the manuscript's bibliography. What format is this file?*

> YOUR ANSWER

Let's add a new citation to the end of the second sentence of the Summary. In main_text.qmd, select the Visual Editor and scroll down to the end of the second sentence of the summary. Choose Insert -> Citation from the menu at the top of the editor window. Search for "Newton 2008 Migration Ecology of Birds" and insert the citation. Click back to the Source Editor. Render the document to make sure the citation appears.

*Q3. In the source editor, what is the text of the inserted citation (beginning with @)?*

> YOUR ANSWER

## Step 3 - Inline code

On line 694, find the placeholder text that says "<INSERT HERE>". Your job is to add code to render the correct number of monitoring hours to fill the gap in the manuscript.

The variable `file_df$duration_s` is a vector containing the count in seconds of every file in the dataset. Write code that will sum this vector and divide by 3600 to find the total number of recording hours, and insert that code instead of the placeholder text. Render the document.

*Q4. What is the total number of hours recorded as now rendered on the document?*

> YOUR ANSWER

## Step 4 - Figure presentation

Figure 3 is currently rendered too small on the document. Find the chunk that generates that figure and change the parameters at the top of the chunk to get the figure rendered properly. You may want to consult the helpful documentation [here](https://r4ds.hadley.nz/quarto.html#figure-sizing).

*Q5. What did you change in the figure chunk to get the figure to render properly?*

> YOUR ANSWER

## Step 5 - Cross references

On line 1034, find the placeholder text "<INSERT REF TO TABLE>". We need to insert a reference to Table 1 here. Insert the appropriate text (hint: it will begin with \@). Render the document to confirm. See helpful documentation [here](https://quarto.org/docs/manuscripts/authoring/rstudio.html#cross-ref).

*Q6. What text did you insert to add the reference?*

> YOUR ANSWER

## Step 6 - Exporting in other formats

On line 48 of the document in the YAML header, there is currently the word `html:`, indicating that the document will be formatted as html. However, Quarto supports docx, pdf, and other formats. Try replacing `html` with `docx` and `pdf` and rendering the file.

*Q7. Were you able to export the document as docx or html? If so, how does the appearance compare to that of the html file?*

Note: if you cannot render the pdf because you do not have LaTeX installed on your computer, do not worry about installing LaTeX. It is not required for this class.

> YOUR ANSWER

## Submitting

You're done! There is no need to submit this file to Canvas since it is a bonus exercise.

## Resources

[Quarto - Authoring Manuscripts](https://quarto.org/docs/manuscripts/authoring/rstudio.html)
