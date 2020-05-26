# Custom JupyterHub Templates for CarbonPlan JupyterHubs

This repo contains html jinja2 templates for customising the appearance of JupyterHub. Each HTML file here will override the files in `https://github.com/jupyterhub/jupyterhub/tree/master/share/jupyter/hub/templates`.

## Usage

To use this repo ensure it is checked out and available somewhere that JupyterHub can find it. In this example we will assume we have cloned it somewhere and created the following symlinks:

`/path/to/repo/templates` -> `/usr/local/share/jupyter/hub/custom_templates`
`/path/to/repo/assets` -> `/usr/local/share/jupyter/hub/static/custom`

Add the following to your JupyterHub config

```python
c.JupyterHub.logo_file = '/usr/local/share/jupyter/hub/static/custom/images/logo.png'
c.JupyterHub.template_paths = ['/usr/local/share/jupyter/hub/custom_templates/',
                                '/usr/local/share/jupyter/hub/templates/']
```

## license

All the code in this repository is [MIT](https://choosealicense.com/licenses/mit/) licensed, but we request that you please provide attribution if reusing any of our digital content (graphics, logo, reports, etc.). Some of the data featured here is sourced from content made available under a [CC-BY-4.0](https://choosealicense.com/licenses/cc-by-4.0/) license. We include attribution for this content, and we please request that you also maintain that attribution if using this data.

## about us

CarbonPlan is a non-profit organization working on the science and data of carbon removal. We aim to improve the transparency and scientific integrity of carbon removal and climate solutions through open data and tools. Find out more at [carbonplan.org](https://carbonplan.org/) or get in touch by [opening an issue](https://github.com/carbonplan/hub/issues/new) or [sending us an email](mailto:hello@carbonplan.org).
