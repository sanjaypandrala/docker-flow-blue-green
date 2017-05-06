# Do not use this project. It is in the brainstorming phase

## Requirements

### Functional requirements / the process

* Detect the color of the current release color (e.g. blue)
* Deploy a new release a the other color (e.g. green)
* Publish the new release under a "special" address (e.g. through DFP) so that it can be tested.
* Replace the new release in the proxy config.
* (Optionally) revert to the previous color.

## Technical requirements

* Deployment using blue-green process should be as transparent as possible. Ideally, it would be a new flag in `docker service create` or `docker stack deploy`. If changing Docker binary is not an option, alternative would be to create a new binary that would act as a wrapper around `docker` commands.
* Additional binaries/containers should not be needed (e.g. Consul for service registry)
