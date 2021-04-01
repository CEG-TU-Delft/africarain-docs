# Africa Rain 

User's Documentation.

## Installation:

1. Clone the repository

``` shell
git clone https://github.com/CEG-TU-Delft/africarain-docs.git
```

2. Go to the root of the repository and create a virtual environment

``` shell
$ cd .../sphinx-itc-template
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