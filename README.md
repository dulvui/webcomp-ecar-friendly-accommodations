
# E-Car Friendly Accommodation Finder

[![REUSE status](https://api.reuse.software/badge/github.com/noi-techpark/webcomp-boilerplate)](https://api.reuse.software/info/github.com/noi-techpark/webcomp-boilerplate)
[![CI/CD](https://github.com/noi-techpark/webcomp-boilerplate/actions/workflows/main.yml/badge.svg)](https://github.com/noi-techpark/webcomp-boilerplate/actions/workflows/main.yml)


_What is the problem domain?_

E-vehicles are becoming increasingly popular, however, e-charging stations are not that widely available yet. Tourists that come to South Tyrol with their e-vehicles also face this problem, especially if their selected accommodation is not near a charging station.

_What does the web component provide?_

This web component tries to mitigate this issue by allowing the user to find accommodations in South Tyrol that are within a spefic distance to a charging station. 

_Which data of the Open Data Hub will be shown?_

The web component uses the Open Data Hub's Accommodation and E-Mobility datasets.

_Why is it soo cool?_

The web component is visually pleasing, easy to use, brings value to the user, allows for greener tourism, allows for dynamic accommodation type, distance from echarging station and language selection. The web component comes in 3 languages (English, Italian, German) (MAYBE). The data is fetched by using the SPARQL endpoint. 

## Table of contents

- [Usage](#usage)
- [Gettings started](#getting-started)
- [Tests and linting](#tests-and-linting)
- [Deployment](#deployment)
- [Docker environment](#docker-environment)
- [Information](#information)

## Usage

Include the webcompscript file `dist/accommodation.min.js` in your HTML and define the web component like this:

```html
<hotel-picker center="[54.012, 23.4567]" language="en"></hotel-picker>
```

### Attributes

#### center

The description of the parameter **center**.

Type: string
Options: "test", "123"

#### language

The description of the parameter **language**.

Type: string
Options: "en", "it", "de"

## Getting started

These instructions will get you a copy of the project up and running
on your local machine for development and testing purposes.

### Prerequisites

To build the project, the following prerequisites must be met:

- Node 12 / NPM 6

For a ready to use Docker environment with all prerequisites already installed and prepared, you can check out the [Docker environment](#docker-environment) section.

### Source code

Get a copy of the repository:

```bash
git clone https://github.com/gpiliponyte/ECarFriendlyAccommodation.git
```

Change directory:

```bash
cd ECarFriendlyAccommodation/
```

### Dependencies

Download all dependencies:

```bash
npm install
```

### Build

Build and start the project:

```bash
npm run start
```

The application will be served and can be accessed at [http://localhost:8080](http://localhost:8080).

## Tests and linting

The tests and the linting can be executed with the following commands:

```bash
npm run test
npm run lint
```

## Deployment

To create the distributable files, execute the following command:

```bash
npm run build
```

## Docker environment

For the project a Docker environment is already prepared and ready to use with all necessary prerequisites.

These Docker containers are the same as used by the continuous integration servers.

### Installation

Install [Docker](https://docs.docker.com/install/) (with Docker Compose) locally on your machine.

### Dependenices

First, install all dependencies:

```bash
docker-compose run --rm app /bin/bash -c "npm install"
```

### Start and stop the containers

Before start working you have to start the Docker containers:

```
docker-compose up --build --detach
```

After finished working you can stop the Docker containers:

```
docker-compose stop
```

### Running commands inside the container

When the containers are running, you can execute any command inside the environment. Just replace the dots `...` in the following example with the command you wish to execute:

```bash
docker-compose run --rm app /bin/bash -c "..."
```

Some examples are:

```bash
docker-compose run --rm app /bin/bash -c "npm run test"
```

## Information

### Support

For support, please contact [help@opendatahub.bz.it](mailto:help@opendatahub.bz.it).

### Contributing

If you'd like to contribute, please follow the following instructions:

- Fork the repository.

- Checkout a topic branch from the `development` branch.

- Make sure the tests are passing.

- Create a pull request against the `development` branch.

A more detailed description can be found here: [https://github.com/noi-techpark/documentation/blob/master/contributors.md](https://github.com/noi-techpark/documentation/blob/master/contributors.md).

### Documentation

More documentation can be found at [https://opendatahub.readthedocs.io/en/latest/index.html](https://opendatahub.readthedocs.io/en/latest/index.html).

### Boilerplate

The project uses this boilerplate: [https://github.com/noi-techpark/webcomp-boilerplate](https://github.com/noi-techpark/webcomp-boilerplate).

### License

The code in this project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE Version 3 license. See the [LICENSE.md](LICENSE.md) file for more information.
