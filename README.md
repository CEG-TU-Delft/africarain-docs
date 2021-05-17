# Africa Rainfall Data documentation 

User-facing documentation for Africa Rainfall project data. This documentation is hosted at [africarain.readthedocs.io](https://africarain.readthedocs.io/en/latest/).

## Installation:
These steps are required to edit files locally and publish to the Read The Docs site. Changes made directly in GitHub via the browser will also be reflected on the readthedocs site after a few minutes.

1. Clone the repository

``` shell
git clone https://github.com/CEG-TU-Delft/africarain-docs.git
```

2. Go to the root of the repository and create a virtual environment

``` shell
$ cd africarain-docs
$ python3 -m venv ./venv
```

3. Activate the virtual environment

* Linux:

``` shell
$ source ./venv/bin/activate
```

* Windows:

```shell
> .\venv\Scripts\activate
```

4. Use pip to install the required packages

``` shell
$ pip install -r requirements.txt
```

3. Go to `./docs` and compile

``` shell
$ make html
```

For more on creating you own Sphinx projects visit the [official documentation.](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html)
