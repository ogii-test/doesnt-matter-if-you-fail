# doesnt-matter-if-you-fail
A sample CircleCI project to trigger a sequential job regardless if the first job passes or fails

The continuation orb does not allow you to directly pass in a value for `when`, and due to this I have copied the command code from the orb source.

## How to use

There are three files in this project:

1. `config.yml` - used to create the setup workflow
2. `config_continue.yml` - contains the downstream jobss
3. `continue.sh` - script to fire the continuation api call

For your first job, please define it within the setup workflow in `config.yml`. 
All downstream jobs can be defined within `config_continue.yml`.
