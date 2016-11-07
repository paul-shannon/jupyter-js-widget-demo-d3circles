# Some Simple Jupyter Widgets

Wishing to become proficient at creating interactive widgets for Jupyter notebooks and labs,
I studied the helpful documentation offered by the jupyter/ipywidgets project:

  -  https://github.com/ipython/ipywidgets   (the project's README is helpful)
  -  http://ipywidgets.readthedocs.io/en/latest/examples/Widget%20Custom.html (provides well-document incremental examples)

I next attempted more advanced examples (quoting here directly from the README):

<hr>
Examples of custom widget libraries built upon ipywidgets are

- [bqplot](https://github.com/bloomberg/bqplot) a 2d data visualization library
  enabling custom user interactions.
- [pythreejs](https://github.com/jovyan/pythreejs) a Jupyter - Three.js wrapper,
  bringing Three.js to the notebook.
- [ipyleaflet](https://github.com/ellisonbg/ipyleaflet) a leaflet widget for Jupyter.

<hr>

I found these, however, to be rather large and confusing. These
are big, rich widgets, worth emulating, very useful in themselves, but perhaps not the easiest examples for a
novice widget programmer to learn from:

  - ipyleaflet:  500 lines of python, 800 lines of javascript
  - pqplot: 4300 lines of python, 15000 lines of javascript
  - pythree: 800 lines of python, 2000 lines of javascript

So, with helpful advice from the jupyter-js-widget development team, I embarked upon
an intermediate (actually, pretty simple) widget "Simple-d3-circles" which I present here in several 
successive forms.  The first notebook has only 16 lines of python, and 92 lines of javascript.   
It demonstrates the features of widget programming I most wanted to understand as I started out.

The second notebook has a richer browser interface, and significantly more communication between
kernel and browser, with the goal of
  - synchronizing state fully between the two environments
  - offering operations (create, delete, count) equally in both enviroments, by function
    calls in python, and interactive gestures in the browser.

I will present both versions of the widget in three forms:

 - self-contained within a single jupyter notebook, using javascript "magic"
 - as an installable notebook extension following the [jupyter widget cookiecutter](https://github.com/jupyter/widget-cookiecutter),
   (pending)
 - with whatever modifications will be needed for it to function as a jupyter lab widget (also  pending)

I welcome suggestions.
