# samsara-python

Python SDK for the Samsara REST API.

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage

### pip install

To install directly from Github:

```sh
pip install git+https://github.com/samsarahq/samsara-python.git
```
(Note that you may need to run `pip` with root permission).

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

## Getting Started

* Install the samsara Python package: [installation procedure](#installation--usage).

* Get your Samsara API access token.

The access token authenticates requests. It is tied to your organization and can be found on the
API Tokens tab on your Organization Settings page in Samsara Cloud (click on the user drop-down in
the upper-right of the Dashboard).

All API calls require the access token.

* Get the Group IDs for the groups you want to access.

The API Tokens tab lists all your organization's Groups and their associated IDs ("groupId").

Certain API calls require this value.

* Check out the examples in the `examples/` directory to see how to use the Python client.

## API Endpoints

All URIs are relative to *https://api.samsara.com/v1*

Method | HTTP request | Description
------------ | ------------- | -------------
[**get_fleet**](docs/DefaultApi.md#get_fleet) | **POST** /fleet/list | Get the vehicles for the group.
[**get_fleet_locations**](docs/DefaultApi.md#get_fleet_locations) | **POST** /fleet/locations | Get the GPS locations for all vehicles in the group.
[**get_fleet_trips**](docs/DefaultApi.md#get_fleet_trips) | **POST** /fleet/trips | Get the trips for the specified vehicle.
[**add_fleet_address**](docs/DefaultApi.md#add_fleet_address) | **POST** /fleet/add_address | Add an address book entry for the group.
[**update_vehicles**](docs/DefaultApi.md#update_vehicles) | **POST** /fleet/set_data | Update the metadata for the specified vehicles.
[**get_sensors**](docs/DefaultApi.md#get_sensors) | **POST** /sensors/list | Get the sensors for a group.
[**get_sensors_temperature**](docs/DefaultApi.md#get_sensors_temperature) | **POST** /sensors/temperature | Get the current temperature readings for the specified sensors.
[**get_sensors_humidity**](docs/DefaultApi.md#get_sensors_humidity) | **POST** /sensors/humidity | Get the current humidity readings for the specified sensors.
[**get_sensors_history**](docs/DefaultApi.md#get_sensors_history) | **POST** /sensors/history | Get the historical data for the sensors.

## Request Parameters

- [GroupParam](docs/GroupParam.md)
- [TripsParam](docs/TripsParam.md)
- [AddressParam](docs/AddressParam.md)
- [VehicleUpdateParam](docs/VehicleUpdateParam.md)
- [SensorParam](docs/SensorParam.md)
- [HistoryParam](docs/HistoryParam.md)

## Responses

- [Vehicle](docs/Vehicle.md)
- [VehicleLocation](docs/VehicleLocation.md)
- [TripResponse](docs/TripResponse.md)
- [Sensor](docs/Sensor.md)
- [TemperatureResponse](docs/TemperatureResponse.md)
- [HumidityResponse](docs/HumidityResponse.md)
- [SensorHistoryResponse](docs/SensorHistoryResponse.md)
- [ErrorResponse](docs/ErrorResponse.md) 


## Footnotes

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build date: 2016-08-17T12:10:56.786-07:00
- Build package: class io.swagger.codegen.languages.PythonClientCodegen
