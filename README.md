# sampgdk-amlg

A 📦 PACC port of SAMPGDK Amalgamation

## Installation

Add `sampgdk-amlg` to dependencies in `cpackage.json`:

```json
"dependencies": [ "sampgdk-amlg@^0.1.0" ]
```

then run:

```
pacc install
```

**or**

```
pacc install sampgdk-amlg@^0.1.0 --global
```
to install globally.

## How to use

Note: for best experience, use `samp-cpp` library.
`samp-cpp` uses `sampgdk-amlg` as a dependency.


### With `samp-cpp`

Example code:

```cpp
#include <SAMPCpp/Everything.hpp>
#include <SAMPCppExt/ServerCore.hpp>

// for convenience
namespace samp = samp_cpp;
namespace color = samp::color;

///////////////////////
bool onPlayerConnect(samp::Player player)
{

	player.msg(color::white, "Hello, {}", player.name());
	return true;
}

///////////////////////
bool onPlayerSpawn(samp::Player player)
{
	samp::Vector3f spawnPos = {100.f, 200.f, 300.f};

	player.setPosition(spawnPos);
	player.setFacingAngle(120.f);
	player.msg(color::white, "You have been spawned at {}", spawnPos);
	return true;
}
````


### Pure `sampgdk-amlg`

Visit [official SAMPGDK repo site](https://github.com/Zeex/sampgdk) for tutorials.


## License

Everything besides SAMPGDK code is under MIT license.

SAMPGDK license is under [Apache 2.0 license](SAMPGDK_LICENSE)