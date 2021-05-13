Configuration
=============

Sphinx Dependencies
-------------------

If you use custom dependencies in your Sphinx build, make sure to include them in a ``requirements.txt`` file in your documentation directory.


GitHub Action
-------------

This GitHub Action will check-out the repository and use ``sphinx-action`` to build the documentation in the ``docs/`` directory.
Then an artifact of the HTML output is created and the documentation is committed on the ``gh-pages`` branch.

.. note::
    The ``gh-pages`` branch is initialised again on every build and force pushed to the repository.
    This is done because I don't want to keep the history of the built pages.

.. literalinclude:: ../.github/workflows/sphinx2pages.yml
  :language: yaml


GitHub Pages
------------

Configure GitHub Pages to serve your documentation from the root of the ``gh-pages`` branch.
You should now be able to browse your documentation on GitHub Pages!