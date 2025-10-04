# IASsure-WX-LITH

This is a fork of [dotFionn](https://github.com/dotFionn)'s [IASsure-WX](https://github.com/dotFionn/iassure-wx), modified for the needs of [Lithuania vACC](https://ltvacc.org) :lithuania: 

## Idea

This service is designed to gather weather data necessary for the [IASsure](https://github.com/MorpheusXAUT/IASsure) EuroScope plugin created by [MorpheusXAUT](https://github.com/MorpheusXAUT). It uses the [Open-Meteo.com](https://open-meteo.com) API as the data source.

## Installation/Deployment

IASsure-WX is intended to be deployed as a Docker container :whale2:

## Configuration

IASsure-WX can be configured using the `wx-config.json` file. It is documented in the schema definition file `wx-config.schema.json`. For now it contains test data from the original project, but in the future it will hold production data for the Vilnius FIR/UIR. If necessary, a different file can be mounted on top of it (`/opt/wx-config.json`). You may also make the necessary changes in a forked or cloned repository.

## Environment Variables

Some options can be defined using environment variables:  
```bash
# Defines the port that the application will listen on.
# Default: 3000
PORT=3000
# Defines the base path used for the resulting API.
# Default: /api
BASE_PATH=/api
# Defines IPs that are allowed as proxy IPs.
# See http://expressjs.com/en/guide/behind-proxies.html
# Empty by default.
TRUST_PROXY=
# Set to true to disable the /api endpoint. Will also disable the frontend.
# Empty (false) by default.
DISABLE_DEFAULT_API_ENDPOINT=
```

## Acknowledgements

Thanks go out to G. Csernak for creating and maintaining [EuroScope](https://www.euroscope.hu/wp/) itself, [MorpheusXAUT](https://github.com/MorpheusXAUT) for the [IASsure plugin](https://github.com/MorpheusXAUT/IASsure), and of course [dotFionn](https://github.com/dotFionn) for creating the original [IASsure-WX](https://github.com/dotFionn/iassure-wx) project. This repository would not exist if not for the time and dedication of these amazing people.

## License

Copyright (C) 2023-2025 dotFionn, MorpheusXAUT  
Copyright (C) 2025 Lithuania vACC  
This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, version 3.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.