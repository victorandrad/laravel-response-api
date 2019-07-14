# Response API

## About

The `laravel-response-api` package allows you to standardize the responses of your api that will be consumed.

## Installation

Require the `victorandrad/laravel-response-api` package in your `composer.json` and update your dependencies:
```sh
$ composer require victorandrad/laravel-response-api
```

## Global usage

To use Response you must include it in your Controller, include the
in the return of your method you want it to return:

```php
public function User {
	//return success
	$json = //my object
	return Response::json(ResponseUtil::makeResponse('DONE', $json), Response::HTTP_OK);
	
	//return error
	$json = //my object
	return Response::json(ResponseUtil::makeError('NOT_FOUND', $json), Response::HTTP_NOT_FOUND);
}
```
