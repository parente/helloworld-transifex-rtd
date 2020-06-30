# helloworld-transifex-rtd

This project demonstrates demonstrate a continuous integration and deployment workflow involving
Sphinx, Transifex, GitHub Actions, and ReadTheDocs. I created it to supplement the documentation in
https://github.com/jupyter/jupyter/pull/475 describing how to enable translations of Sphinx
documentation for Project Jupyter.

![Translation CI/CD](https://raw.githubusercontent.com/parente/jupyter/translation-doc/docs/source/contrib_docs/static/translation-ci-cd.png)

Points of interest

- The Sphinx configuration `docs/source/conf.py` which configures the path where `.po` language
  files reside
- The GitHub Action workflow `.github/workflows/gettext.yml` which regenerates and commits the
  English `.po` files automatically any time the English Markdown or restructuredText documentation
  changes on the `master` branch
- https://github.com/parente/helloworld-transifex-rtd/commit/9c2b4212ad - an example commit made by
  the GitHub Action workflow after I added a new text to `second.md`
- https://github.com/parente/helloworld-transifex-rtd/pull/1 - an example pull request submitted by
  Transifex after I translated all of the English text in the `first.po` file to Spanish using the
  Transifex web app
- https://helloworld-transifex-rtd.readthedocs.io/en/latest/ - the English docs hosted on
  ReadTheDocs
- https://helloworld-transifex-rtd.readthedocs.io/es/latest/ - the translated Spanish docs hosted on
  ReadTheDocs
