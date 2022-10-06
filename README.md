<h1 align="center">heroku-buildpack-wkhtmltopdf</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---


## 📝 Table of Contents

- [About](#about)
- [Changelog](#changelog)
- [Deployment](#deployment)
- [Usage](#usage)
- [Acknowledgements](#acknowledgement)
- [License](#license)

##  About <a name = "about"></a>

This buildpack downloads and extracts the most recent [wkhtmltopdf](https://wkhtmltopdf.org/) binaries:

- v0.12.6.1-2 for `heroku-22` stack
- v0.12.6-1 for `heroku-20` stack
- v0.12.5 for `heroku-18` stack.

## Changelog <a name = "changelog"></a>
- v1.0 (initial release)
  - Support for `Cedar-14`, `heroku-16`,  and `heroku-18`
  - Support for Aptfile

- v2
    - Added support for `Heroku-20`
    - Removed support for `Cedar-14` and `heroku-16` as they reached end of life.

- this fork
    - Added support for `Heroku-22`
    - Removed Aptfile
    - Updated Readme

## Deployment <a name = "deployment"></a>
Just add the buildpack to your heroku app under 'Settings' or by executing:

```bash
heroku buildpacks:add https://github.com/DGalbichek/heroku-buildpack-wkhtmltopdf.git
```

Might help to purge cache when changing stack!

```bash
heroku plugins:install heroku-repo
heroku repo:purge_cache -a appname
```

## Usage <a name="usage"></a>

The binaries `wkhtmltopdf` and `wkhtmltoimage` will be available on `/app/bin`,
you can just execute `/app/bin/wkhtmltopdf ` and `/app/bin/wkhtmltoimage`  from your app.


## Acknowledgements <a name = "acknowledgement"></a>

Original:
- All thanks to [heroku-buildpack-apt](https://github.com/ddollar/heroku-buildpack-apt) project.
- Forgive me if I've used your code and forgot to mention you.

Fork:
- Big thank you to RohanDebroy, of course :)

## License <a name="license"></a>
MIT
