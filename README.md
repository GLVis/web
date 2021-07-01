# GLVis / web

This repo contains the GLVis website [MkDocs](http://www.mkdocs.org/) sources.

To clone, including submodules

```
git clone --recurse-submodules git@github.com:GLVis/web.git
```

If you've already cloned you can pull submodules with:

```
git submodule update --init --recursive
```

To make changes to the website pages:

- use MkDocs v1.0.4 with Markdown v2.6.8, PyYAML v3.13 and futures v3.3.0, e.g.
  * `pip install --upgrade --user mkdocs==1.0.4`
  * `pip install --upgrade --user Markdown==2.6.8`
  * `pip install --upgrade --user PyYAML==3.13`
  * `pip install --upgrade --user futures==3.3.0`
- clone this repo,
- edit or add some ```.md``` files (you may also need to update the ```mkdocs.yml``` config),
- preview locally with ```mkdocs serve``` (Windows users may need to specify a port, such as ```mkdocs serve --dev-addr 127.0.0.1:4000```),
- publish with ```mkdocs gh-deploy```.
