<div align="center">

<h2>MockIt: A tool to quickly create mocked APIs.</h2>
<p>Stop wasting time mocking APIs. MockIt gives you an interface to configure and create REAL mocked endpoints for your applications. Whilst you wait for APIS to be built use MockIt to talk to a real service.</>

  <hr />

[![Travis](https://img.shields.io/travis/boyney123/mockit/master.svg)](https://travis-ci.org/boyney123/mockit)
[![CodeCov](https://codecov.io/gh/boyney123/mockit/branch/master/graph/badge.svg?token=AoXW3EFgMP)](https://codecov.io/gh/boyney123/mockit)
[![Netlify Status](https://api.netlify.com/api/v1/badges/6d5acca1-0959-4d92-a739-08f725fdc464/deploy-status)](https://app.netlify.com/sites/mockit/deploys)
[![MIT License][license-badge]][license]
[![PRs Welcome][prs-badge]][prs]
[![All Contributors](https://img.shields.io/badge/all_contributors-13-orange.svg?style=flat-square)](#contributors-)

[![Watch on GitHub][github-watch-badge]][github-watch]
[![Star on GitHub][github-star-badge]][github-star]
[![Tweet][twitter-badge]][twitter]

[Donate ☕](https://www.paypal.me/boyney123/5)

<hr />

<img alt="header" src="./images/demo.gif" />

  <h3>Features: Live Reload, Chaos Engineering, Authentication, CORS and more...</h3>

[Read the Docs](https://mockit.netlify.com/) | [Edit the Docs](https://github.com/boyney123/mockit-docs)

</div>

<hr/>

# The problem

When building applications you often need to interact with services. When the services are not ready to be consumed you have a few options:

1. Mock out the response with a JSON file
2. Create a mock service yourself
3. Use MockIt.

# This solution

This tool was designed to help developers quickly create endpoints for their applications. No need to create a server, just use docker and run this project locally. You can create, edit and manage routes to your API. Every change to the API will be reflected on the server and updated straight away.

This tool comes with a few features out the box:

- CORS
- Basic Authentication
- Chaos Monkey (Unleash a monkey to take down your endpoints)

More information about how it works, its features can be found on the docs.

[Read the docs and get started](https://mockit.netlify.com/)

# Getting Started

_Make sure you have docker running_

```sh
git clone https://github.com/boyney123/mockit.git
```

```sh
cd mockit && docker-compose up --build -d
```

Once everything is up and running go to [http://localhost:5000](http://localhost:5000) to see MockIt.

For instructions on how to use MockIt please see the [documentation](https://mockit.netlify.com/docs/getting-started/routes).

## Permissions

_If you get error: `Couldn't connect to Docker daemon at http+docker://localhost - is it running?` you might need run_ with _sudo_

```
sudo docker-compose up --build -d
```

## Local install and running tests

If you want to install and run the tests for all apps then you can run this script:

```
sh install-and-test.sh
```

_If you have any problems with permissions you might need to chmod the file_

```
chmod +x install-and-test.sh && ./install-and-test.sh
```

# Viewing the dashboard, server and API

Once Docker is running you have three applications running on the machine.

1. The client: [http://localhost:5000](http://localhost:5000)
2. The client-server: [http://localhost:4000](http://localhost:4000)
3. The MockIt API (this is the server that runs your API): [http://localhost:3000](http://localhost:3000)

If you want to view the dashboard to get started go to [http://localhost:5000](http://localhost:5000).

If you want to interact with your new API go to [http://localhost:3000](http://localhost:3000).

For example, if you have a `/user` route setup, go to [http://localhost:3000/user](http://localhost:3000/user) to view the data.

# Tools

- [nodemon - Listening for changes](https://github.com/remy/nodemon)
- [Express](https://expressjs.com/)
- [React](https://reactjs.org/)
- [Docker](https://www.docker.com/)

## Documentation

- [Docusaurus](https://docusaurus.io/)

## Testing

- [jest](https://jestjs.io/)
- [react-testing-library](https://github.com/kentcdodds/react-testing-library)
- [supertest](https://github.com/visionmedia/supertest)

# Contributing

If you have any questions, features or issues please raise any issue or pull requests you like.

# Templating

## Faker

For faker use this template on response:

```
{{faker.[category].[type]}}
```

replace the category and type with list below

*for example*

the response is like this
```
{
  "zip_code": "{{faker.address.zipCode}}"
}
```

the zip_code will be different on every hits

### Faker Category and Type

* address
    * zipCode
    * zipCodeByState
    * city
    * cityPrefix
    * citySuffix
    * cityName
    * streetName
    * streetAddress
    * streetSuffix
    * streetPrefix
    * secondaryAddress
    * county
    * country
    * countryCode
    * state
    * stateAbbr
    * latitude
    * longitude
    * direction
    * cardinalDirection
    * ordinalDirection
    * nearbyGPSCoordinate
    * timeZone
* animal
    * dog
    * cat
    * snake
    * bear
    * lion
    * cetacean
    * horse
    * bird
    * cow
    * fish
    * crocodilia
    * insect
    * rabbit
    * type
* commerce
    * color
    * department
    * productName
    * price
    * productAdjective
    * productMaterial
    * product
    * productDescription
* company
    * suffixes
    * companyName
    * companySuffix
    * catchPhrase
    * bs
    * catchPhraseAdjective
    * catchPhraseDescriptor
    * catchPhraseNoun
    * bsAdjective
    * bsBuzz
    * bsNoun
* database
    * column
    * type
    * collation
    * engine
* datatype
    * number
    * float
    * datetime
    * string
    * uuid
    * boolean
    * hexaDecimal
    * json
    * array
* date
    * past
    * future
    * between
    * betweens
    * recent
    * soon
    * month
    * weekday
* fake
* finance
    * account
    * accountName
    * routingNumber
    * mask
    * amount
    * transactionType
    * currencyCode
    * currencyName
    * currencySymbol
    * bitcoinAddress
    * litecoinAddress
    * creditCardNumber
    * creditCardCVV
    * ethereumAddress
    * iban
    * bic
    * transactionDescription
* git
    * branch
    * commitEntry
    * commitMessage
    * commitSha
    * shortSha
* hacker
    * abbreviation
    * adjective
    * noun
    * verb
    * ingverb
    * phrase
* helpers
    * randomize
    * slugify
    * replaceSymbolWithNumber
    * replaceSymbols
    * replaceCreditCardSymbols
    * repeatString
    * regexpStyleStringParse
    * shuffle
    * mustache
    * createCard
    * contextualCard
    * userCard
    * createTransaction
* image
    * image
    * avatar
    * imageUrl
    * abstract
    * animals
    * business
    * cats
    * city
    * food
    * nightlife
    * fashion
    * people
    * nature
    * sports
    * technics
    * transport
    * dataUri
    * lorempixel
    * unsplash
    * lorempicsum
* internet
    * avatar
    * email
    * exampleEmail
    * userName
    * protocol
    * httpMethod
    * url
    * domainName
    * domainSuffix
    * domainWord
    * ip
    * ipv6
    * port
    * userAgent
    * color
    * mac
    * password
* lorem
    * word
    * words
    * sentence
    * slug
    * sentences
    * paragraph
    * paragraphs
    * text
    * lines
* mersenne
    * rand
    * seed
    * seed_array
* music
    * genre
* name
    * firstName
    * lastName
    * middleName
    * findName
    * jobTitle
    * gender
    * prefix
    * suffix
    * title
    * jobDescriptor
    * jobArea
    * jobType
* phone
    * phoneNumber
    * phoneNumberFormat
    * phoneFormats
* random
    * number
    * float
    * arrayElement
    * arrayElements
    * objectElement
    * uuid
    * boolean
    * word
    * words
    * image
    * locale
    * alpha
    * alphaNumeric
    * hexaDecimal
* system
    * fileName
    * commonFileName
    * mimeType
    * commonFileType
    * commonFileExt
    * fileType
    * fileExt
    * directoryPath
    * filePath
    * semver
* time
    * recent
* unique
* vehicle
    * vehicle
    * manufacturer
    * model
    * type
    * fuel
    * vin
    * color
    * vrm
    * bicycle


## Request Forwarding
For request forwarding on response use this template on response:
```
{{req.[request body]}}
```

It will find from query param first, if not found then try to find on payload body

*for example*

the response is like this
```
{
  "order_id": "{{req.data.order.id}}"
}
```

and the request payload will look like this
```
{
  "data": {
    {
      "order":{
        "id": "this string will show on response"
      }
    }
  }
}
```

# Parameterized URL
Mockit supports for parameterized URL Param, this can be achieved by declaring segment that wants to be set as path as `:pathName` (reference: [Express - Route Parameters](https://expressjs.com/en/guide/routing.html))

To add parameter to your response, simply add `{{param.parameterName}}` to your response

```
GET /users/:id/detail
{
    "id": "{{param.id}}",
    "name": "John"
}
```

Once user requested that endpoint along with ID at the URL, parameter will resolved to the actual parameter value
```
GET /users/5/detail
{
    "id": "5",
    "name": "John"
}
```

# Conditions
Conditions allows user to return multiple responses based on condition that are given on the expressions. To start, simply click "Add Condition" below response (note: If there's any conditions set, previous response will be treated as Fallback when there's no condition fulfilled)

## Available Expression Parameters
* `==` (Equal)
* `!=` (Not Equal)
* `<` (Less than)
* `>` (Greater than)
* `<=` (Less than Equal)
* `>=` (Greater than Equal)

## Available Expression Key
* `param.*` - Value will be taken from URL parameter (see Parameterized URL)
* `req.*` - Value will be taken from request body (See [flat npm package](https://www.npmjs.com/package/flat) for the notation)
* `header.*` - Value will be taken from header

# Attribution

This repository is forked from [Github](https://github.com/boyney123/mockit) and edited for fulfill delos requirement.