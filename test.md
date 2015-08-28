# Overview
This template document shows you how to slightly annotate your regular manuscript texts so that your text and all the other texts can later be converted into one nice book. The goal of this workflow is to stay as close as possible to our regular workflow (e.g., Word plus comments and track changes etc.), while keeping the management of the whole book as sane as possible. This template document should be self-contained, that is, you should not need to consult other resources to learn how to annotate your text. 

# Introduction
In the following I will explain how you can slightly annotate your regular manuscript texts so that your text and all the other texts can later be converted into one nice book. The basic idea is that we use a few tricks so that the structure of the text (e.g., headings) and the formatting (e.g., emphasis in italics) we use will be preserved when copy and pasting the main text as plain text (where it can be turned automatically into a book). It’s very easy. See the “#” in the header above? It makes clear that this is a level-1 heading. (In case you’re reading the PDF version of this chapter, you shouldn’t see such annotations anymore, only their results.)

We will use [Markdown], a simple markup language, which is easy to write and read. In the following I will illustrate the tricks we will most frequently need when writing scientific texts. The goal of this workflow is to stay as close as possible to our regular workflow (e.g., Word plus comments and track changes etc.), while keeping the management of the whole book as sane as possible. That is, everybody chapter team is totally free in how to write their texts, both in terms of the writing software (e.g., Microsoft Word, Pages, [GoogleDocs], plain text) and the way to manage collaboration (e.g., by email, [DropBox], [Copy], [GoogleDocs], [git]). In this way, we all can profit from the tools and tricks we already know and are familiar with. Although it is easy to use the annotations already while drafting the text, the annotations can also be added just before submitting the text.

This template document should be self-contained, that is, you should not need to consult other resources to learn how to annotate your text. If you are interested to learn more, you can consult the links provided throughout and the following website, which I draw upon liberally here: <http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html>. If you want to check out how markdown works (and how this or your text will look after formatting, except for the citations and references), check out, for example, <https://stackedit.io/editor>

# The Annotations

## Paragraphs
This is a regular paragraph. A [paragraph] is one or more lines of text followed by one or more blank lines. That is, the only difference to Word is that we need to add an empty line after a paragraph. You can indent the paragraphs if you want to, but this is not necessary.

[paragraph]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#paragraphs

## Links
[Links] can be created in two ways: If you want the URL to be seen, enclose it in pointy brackets like this: <https://stackedit.io/editor>

If you want to add a link to some text, enclose the text with square brackets (e.g., “paragraphs” or “Links”) and add the link information somewhere else (see example below). You can put the link near where you want to create the footnote or also at the end of the main text; it doesn’t matter. In this document I keep the links near where I create them, so that it’s easier for you to find the link. If you’re reading a formatted version of this chapter, then you won’t see this links anymore, but you can click on the link text and you will be taken to the link.

 [links]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#links


## Headers
A [header] consists of one to six # signs and a line of text. The number of # signs at the beginning of the line is the header level: One # for level 1, ## for level 2, ### for level 3 etc. We need to insert an empty line before the heading. We can, but don’t have to use an empty line after the heading. Note that you can format your headers (and in fact any text) however you want (e.g., bold, centered and 16 points). The only thing that matters is the annotations (here the #’s and the empty line).

[header]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#headers

## Emphasis/Italics
This section illustrates how to [emphasize text] with italics. To emphasize some text, surround it with asterisks like this: This text is *emphasized with asterisks*. We can italicize words here in Word and color the asterisks in grey (to make them stick out less) if we want to *like this*, but it’s only the asterisks that will matter.

[emphasize text]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#inline-formatting

## Dashes
One dash - will stay a normal dash.  Two dashes -- will become an n-dash. Three dashes --- will become an m-dash. Note that Word (and possibly other text processors), might automatically turn dashes into an m-dash, so just make sure that you always have the number of dashes you want.

## Footnotes
[Footnotes] work like this.[^my-footnote] You can continue with more text before you define what’s in the footnote itself in a separate line.

[^my-footnote]: This is the footnote text. Note that there needs to be an empty line before and after the footnote text. You can put the footnote text near where you create the footnote or also at the end of the main text; it doesn’t matter. Don’t use spaces or underscores for the footnote name; dashes are OK (e.g., “my-footnote”).

[footnotes]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#footnotes


## Citing References
[Citing references] works using the “key” of the reference (e.g., “einstein1935can”; see further below for more information, including where to get the key). Using this key we can cite references in different ways. Below, the first sentence shows how we cite and the second, repeated sentence shows how it will appear formatted later (APA style). Once formatted, the two sentences should be identical. I put the citation commands and the citation results below in bold here in Word so that they visually stick out.

[citing references]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#citations

Let’s cite a paper on quantum mechanics [@einstein1935can]. Let’s cite a paper on quantum mechanics (Einstein, Podolsky, & Rosen, 1935). A citation comes in square brackets and the key is prefixed with an “@”.

Let’s cite two papers on quantum mechanics [@bohr1935can; @einstein1935can]. Let’s cite two papers on quantum mechanics (Bohr, 1935; Einstein et al., 1935). We separate two or more references with a semi-colon (“;”). Note that the Einstein paper is now automatically shortened to “et al.” since we already cited it above.

Let’s cite a paper on quantum mechanics and add some additional words to the citations [see @einstein1935can, p. 777]. Let’s cite a paper on quantum mechanics and add some additional words to the citations (see Einstein et al., 1935, p. 777). We simply add the additional words before and/or after the reference.[^complex_citations]

[^complex_citations]: If we want to cite more than one paper and add a prefix to the second or later reference, we need to use a little LaTeX. For example: Quantum mechanics is great \parencites{einstein1935can}[but see][p. 696]{bohr1935can}. Quantum mechanics is great (Einstein et al., 1935; but see Bohr, 1935, p. 696). We add the information in square brackets: The first one (“[but see]”) will appear before the reference and the second one (“[p. 696]”) after the reference. If we only want to add some text before *or* after the reference, we just leave the other square brackets empty, but we need to have them both. For example: \parencites{einstein1935can}[][p. 696]{bohr1935can} For more information see section 3.7 in the [bibtex-manual].

[bibtex-manual]: http://mirrors.ctan.org/macros/latex/contrib/biblatex/doc/biblatex.pdf

Einstein and colleagues said something [-@einstein1935can]. Einstein and colleagues said something (1935). A minus sign (“-“) before the “@” will suppress mention of the author in the citation. This can be useful when the author is already mentioned in the text. Einstein and colleagues said something on a particular page [-@einstein1935can, p. 777]. Einstein and colleagues said something on a particular page (1935, p. 777). We can still add additional texts after the year.

## Creating the Reference Entries
At the very end of the document we gather the reference entries. We don’t have to keep them there (i.e., we could have them in a separate text file), but it’s probably convenient to have them in the same document as the main text. Eventually we will copy and paste them online. If there are entries that we don’t end up citing, that’s not a problem.

We need the references as “BibTeX”-entries. The probably easiest way to get them is to find the reference with GoogleScholar (e.g., [this reference][Einstein]), click on “Cite”, and then on “BibTeX”. In our example, we get the following entry:

[Einstein]: https://scholar.google.com/scholar?q=author%3Aa-einstein+author%3Apodolsky+author%3Arosen&btnG=&hl=en&as_sdt=0%2C5

```
@article{einstein1935can,
  title={Can quantum-mechanical description 
  of physical reality be considered complete?},
  author={Einstein, Albert and Podolsky, Boris and Rosen, Nathan},
  journal={Physical review},
  volume={47},
  number={10},
  pages={777},
  year={1935},
  publisher={APS}
}
```

Apparently GoogleScholar creates the key (“einstein1935can”) like this: [name_first_author][year][first_non_stop_word], where everything is lower case and “the” etc. are ignored. You don’t have to use GoogleScholar to create your BibTeX-entries (you can also expert BibTeX from other [bibliography managers], e.g., Papers)[^bibliography-managers], but please make sure that you use GoogleScholar‘s way of constructing the key. This way, I can later automatically detect duplicate references and we then only have to check a reference once (and not many times).

[bibliography managers]: https://en.wikipedia.org/wiki/Comparison_of_reference_management_software#Export_file_formats
[BibDesk]: http://bibdesk.sourceforge.net
[JabRef]: http://jabref.sourceforge.net

[^bibliography-managers]: [BibDesk] is a free Mac OS X bibliography manager. [JabRef] is a free java-based bibliography manager, which runs on Windows, Linux, and Mac OS X.

Please check whether the information is accurate and suitable for the APA citation style. In the Einstein-paper, we need to add the digital object identifier (doi) and capitalize the journal title. LaTeX turns the title into lower case (with the exception of the first letter). If there is a letter in the title that should be capitalized beyond the first letter (e.g., an abbreviation or the start of a second part-sentence after a “:”), enclose these letters with curly brackets. This tells LaTeX to preserve the capitalization. For example: 

```
title={Making robust classification decisions:
{C}onstructing and evaluating fast and frugal trees ({FFT}s)}

```
The correct Einstein-paper will look like this:

```
@article{einstein1935can,
  title={Can quantum-mechanical description 
  of physical reality be considered complete?},
  author={Einstein, Albert and Podolsky, Boris and Rosen, Nathan},
  journal={Physical Review},
  volume={47},
  number={10},
  pages={777},
  year={1935},
  publisher={APS},
  doi={10.1103/PhysRev.47.777}
}
```

If you want to cite an unpublished manuscript, use this template and cite it like any other paper [@maggs1997real].

```
@unpublished{maggs1997real,
  author={Maggs, Bruce M. and Schwabe, Eric J.},
  title={Real-time emulations of bounded-degree networks},
  year={1997},
  note={Unpublished manuscript}
}
```

Now we’ve covered how to create paragraphs, emphasize text, use dashes, create footnotes and cite references. These five tricks will likely cover 80% of what we need. One other further trick we might want to use are lists.

## Lists
This is how we create [lists].

[lists]: http://rmarkdown.rstudio.com/authoring_pandoc_markdown.html#lists

### Bullet Lists
A bullet list is a list of bulleted list items. A bulleted list item begins with a bullet (e.g., “-“). Here is a simple example (note the empty lines before and after the list):

- one
- two
- three

This will produce a “compact” list. If you want a “loose” list, in which each item is formatted as a paragraph, put empty lines between the items:

- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc venenatis dignissim dignissim. Donec porttitor, magna sit amet auctor sollicitudin, tellus risus mollis quam, hendrerit tincidunt est est vitae ante.

- Vivamus mollis id diam sit amet imperdiet. Integer consectetur tortor interdum, commodo leo ut, aliquam nulla. Vivamus leo enim, varius sit amet elementum vel, fermentum ac elit.

- Quisque lobortis, quam id feugiat ultricies, eros mauris faucibus tortor, ac eleifend leo magna porttitor erat. Duis vehicula nulla lectus, et lobortis odio dapibus eget. 

Bullet lists formatted by Word will only survive if the list item symbol is a dash (“-“; and not, for example, a big dot, which is Word’s default).

### Ordered Lists
Ordered lists work just like bulleted lists, except that the items begin with enumerators rather than bullets. For example:

1.  one
2.  two
3.  three

Ordered lists formatted by Word will survive, but only with numbers (1., 2., 3. etc.) and not with letters (a, b, c, etc.).

## Tables, Figures, and Equations
There are some further things we might want to use, for example, figures, tables and equations. For those we will need a little bit of LaTeX[^LaTeX], but not very much. Presumably not many people will need them for the extended abstracts, therefore they are not documented here. If you are interested in using them, please contact me and also check out using the followings links how to

- create [tables] with their captions (with the help of a convenient [online table editor]),
- insert [figures] with their captions, 
- how to [position tables and figures], and
- how to create [mathematical expressions] (with the help of a convenient [online equation editor]).

[tables]: https://www.sharelatex.com/learn/Tables
[online table editor]: https://www.sharelatex.com/learn/Tables
[figures]: https://www.sharelatex.com/learn/Inserting_Images
[position tables and figures]: https://www.sharelatex.com/learn/Positioning_images_and_tables
[mathematical expressions]: https://www.sharelatex.com/learn/Mathematical_expressions
[online equation editor]: https://chrome.google.com/webstore/detail/daum-equation-editor/dinfmiceliiomokeofbocegmacmagjhe


[^LaTeX]: If you feel comfortable working with LaTeX, then you can also write your text directly in LaTeX (instead of using markdown annotations) and later copy and paste the document content (i.e., without preamble, only the text between *begin* and *end* of the document). If you want to use LaTeX, consider trying out [sharelatex] or [overleaf], which allow multiple people to collaborate on the same texts (similar to [GoogleDocs]). As an added benefit, both platforms allow integration with [git].

[markdown]: https://help.github.com/articles/markdown-basics/
[DropBox]: https://www.dropbox.com/
[Copy]: https://www.copy.com/
[sharelatex]: https://www.sharelatex.com
[overleaf]: https://www.overleaf.com
[GoogleDocs]: https://www.google.com/docs/about/
[git]: https://www.git-tower.com/learn/git/ebook/command-line/introduction

# Copy and Pasting the Text for Submission
For submission, I will provide for every chapter links to three files. I will email these links with detailed instructions. Essentially it boils down to copy and pasting the following three types of information or text.

## Chapter Information (?header.tex)
Here you copy and paste (a) the title, (b) the short title (i.e., running header), and (c) the author names. If you use special characters (e.g., “&” or “%”), you need to escape them with a backslash “\”, like this: Jane Fonda \& Chuck Norris. This is because this file is actually LaTeX. You don’t have to worry about those special characters in the main text.

## Main Text (?.md)
Here you copy and paste the main text (i.e., everything after the title and author names and before the reference entries). 

## References (?.bib)
Here you copy and paste the reference entries (see the next page on how to create them).

# Instructions for Extended Abstracts
*(These instructions come from [here][instructions].)*

[instructions]: https://www.dropbox.com/s/l1oxrdmerqyuttm/Instructions%20for%20Extended%20Abstracts.pdf?dl=0

    enter code here

In the first book from the Center for Adaptive Rationality, we aim to tackle perhaps the toughest topic in our field: how do people tame uncertainty? Our proposal has four parts where we are asking for contributions from the members of ARC. Briefly each of the four parts examines this question from each of the different perspectives present in ARC: how heuristics are used to cut through the uncertainty; how people search uncertain options and environments to ultimately reduce their uncertainty and make a more informed decision; how the social world impacts how we deal with uncertainty and in some cases helps us navigate uncertainty; and how the adaptive mind changes partly in response to uncertainty but also how it changes in handling uncertainty.  

We seek a coherent message on our research: one that makes interconnections within the chapters of the book, but also makes connections outside the book to the broader fields of the cognitive and decision sciences and beyond. Moreover, we envision each chapter as being written to be accessible to a wide range of scientists that informs the readers of the progress our group has made in this area, and serves as a forum to push beyond conventional thinking. Borrowing the words of the [editorial policy] for *Trends in Cognitive Science* the chapters should “…offer more than summaries, they should contribute insight.” Hopefully, they should provide a means to offer insight beyond the conventional journal articles we have written on the subject. 

[editorial policy]: http://www.cell.com/trends/cognitive-sciences/authors

To these ends, we would like each group of people charged with a chapter to compose an extended abstract with a maximum of *1,000 words*. The due date for the abstracts will be *1 October, 2015*. Each abstract will be reviewed and discussed during the retreat. Further instructions for submission will be forthcoming. 

The abstracts should be written as if they were proposals being submitted to *Trends in Cognitive Science*. That is the abstract should outline how it will inform readers both inside and outside the field about what we have learned and the new ideas we are exploring on how people tame uncertainty. The abstract should be able to be evaluated independent of the book proposal (i.e., write it as if you are submitting the proposal to *Trends in Cognitive Science* or similar such journal).  It should address some of these questions: 

- What are the key questions you want to address? 
- How does your chapter connect to the overarching theme of adaptive cognition?
- What are the key empirical findings that you plan to report? 
- What are the key theories that you plan to use? 
- What are the key theoretical developments of the chapter?
- What lines of the research you will connect to outside the book?

Please also provide a list of the citations of your own papers and publications that you want to base your chapter on. 

Finally, independent of the abstract, one feature we seek to explore is to develop interactive features of the book. For instance, we may want to examine the inclusion of source code, working examples of experiments, simulations, data, and data visualization. Thus, as you are working please take note of unique ways we can make the chapters more interactive and promote an open science network. 

(This would be the last sentence that you would copy into the .md-file for the main text.)
 
