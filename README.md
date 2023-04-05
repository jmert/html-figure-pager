# HTML Figure Pager

*An active example of this Javascript library can be found
[here](https://jmert.github.io/html-figure-pager/index.html).*

This package provides a small, self-contained Javascript library which allows one to
easily create "figure pagers" in their HTML documents.
In my graduate research group, we often had to generate many plots (numbering anywhere from
a handful to many thousands) that showed data in various combinations or processing options.

Beyond a few figures, it is impractical to show all combinations linearly on a page, so we
used the so-called figure pagers to allow interactive selection of a single image to show
at a time from a collection.
For instance, the following screenshot is one simple example where there are two
types of options ("Mode" and "Color map") which can both take on a variety of values.
By clicking on an option, the figure to the right is updated according to a user-defined
mapping from option values to image file name.

![screenshot](screenshot.png)

## Cloning

The demo linked above is contained within the `gh-pages` branch of this repository, and
it contains a large number of images.
With a normal `git clone`, all of these images are downloaded as part of the git history,
increasing the download and storage size significantly beyond the small size of the pager
script itself.

To avoid downloading the unnecessary demo, you may instead use a shallow clone to obtain
a copy of only the latest commit, and then "unshallow" the branch to obtain the full
history of the `master` branch while completely ignoring the `gh-pages` branch.

```bash
git clone --depth 1 https://github.com/jmert/html-figure-pager
cd html-figure-pager
git pull --unshallow
```
