# Contributing to the slides

## Structure

The slides are implemented using [xaringan](https://cran.r-project.org/package=xaringan).

The source file that encodes the slides is `index.Rmd`.

Images are stored in the `img/` sub-directory, and their relative link is used in the `index.Rmd` to insert them in the slides.


## How can I contribute?

- Add slides in the `index.Rmd` file (see the 'Format' section above for more details).
- If applicable, add images in the `img/` sub-directory.

## How do I insert a new slide?

Individual slides are separated by a line made of three dashes, i.e. `---`, surrounded by two empty lines, one above and one below, i.e.

```
Slide 1

---

Slide 2
```

## How do I insert images in slides?

Once you have stored a new image in the `img/` sub-directory, you can link it from the `index.Rmd` file using its relative path, e.g.

```
<img src='img/Bioconductor-rh.png' height='400px'>"
```

Note that HTML attributes, e.g. `height='400px'`, are optional, but helpful to control the size and layout of the image in the slide.

It is also possible to use `knitr::include_graphics()`, e.g.

````
```{r, fig.align='center', out.height='400px', echo=FALSE}
knitr::include_graphics("img/OSCA/bioc-figures_v2-02.png")
```
````
