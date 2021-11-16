# Unit tests example

This is a single Git repository that holds two microservices (Python and GO) that demonstrates different ways of running unit tests with Codefresh.

## Packaging the Go app

To compile and package using Docker 

```bash
cd golang-app-A
docker build . -t my-go-app
```

## Packaging the Python app

To compile and package using Docker 

```bash
cd python-app-B
docker build . -t my-python-app
```


## Running the unit tests locally

To run unit tests each application

```bash
cd golang-app-A
go test -v
```

and

```bash
cd python-app-B
python setup.py test
```


You need to have a development environment for Go/Python in each case.

## To use this project in Codefresh

There is also a [codefresh.yml](codefresh.yml) for easy usage with the [Codefresh](codefresh.io) CI/CD platform.

More details can be found in [Codefresh documentation](https://codefresh.io/docs/docs/yaml-examples/examples/run-unit-tests/).

