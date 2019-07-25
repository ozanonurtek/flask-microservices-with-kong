# Kong Api Gateway with Flask Microservices

This is a simple demonstration of how to use Kong as a api gateway of Python/Flask Microservices. This tutorial uses DBless setup(declarative_config) of Kong because of its simplicity. By default kong uses postgresql to store its configurations

## Cinema 3 (Microservices Part)

[Cinema 3]("https://github.com/umermansoor/microservices") is an example project which demonstrates the use of microservices for a fictional movie theater. 
The Cinema 3 backend is powered by 4 microservices, all of which happen to be written in Python using 
Flask.

 * Movie Service: Provides information like movie ratings, title, etc.
 * Show Times Service: Provides show times information.
 * Booking Service: Provides booking information. 
 * Users Service: Provides movie suggestions for users by communicating with other services.

### Usage

- Python 2.7 must be installed (Which is already installed in macOS by default)
- `cd mircroservices && make install`

- To launch the services: `make launch`

- To stop the services: : `make launch`

- Details can be found under microservices path's README.md


## Kong


### Installation macOS

- Homebrew must be installed in your system:

- Install homebrew: `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)` 

- `brew tap kong/kong ` 

- `brew install kong`

- If your XCode is outdated, during installation `xcode-select --install` might be asked.

- Run! : `kong start -c kong.conf`

- Sample request to UserMicroservice: `curl -L -i -X GET http://0.0.0.0:8000/users --header 'Host: users.com'`

- If you wish to add new microservices to kong configuration, service configurations are stored under kong.yml. You can also apply plugins like basic-auth using this configuration file.

### Credits

- Thanks for preparing Cinema 3 microservice example to [umermansoor](https://github.com/umermansoor)

- Thaks for [comment](https://github.com/Kong/kong/issues/4373#issuecomment-470987094) under [this issue](https://github.com/Kong/kong/issues/4373)
