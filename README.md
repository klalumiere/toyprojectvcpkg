# toyprojectvcpkg

## Relevant links

- [Pull request versioning](https://github.com/microsoft/vcpkg/pull/11758)
- [Pull request registries RFC](https://github.com/microsoft/vcpkg/pull/13590)
- [Pull request registries implementation](https://github.com/microsoft/vcpkg/pull/15054)
- [vcpkg roadmap](https://github.com/microsoft/vcpkg/wiki/Roadmap)

## Build

### Requirement

Set the environment variable `VCPKG_ROOT` to the folder that contains vcpkg source.

### Building

```shell
mkdir debug
cd debug
cmake -G Ninja ..
cmake --build .
./toyprojectvcpkg_main
```
