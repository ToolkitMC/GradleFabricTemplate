# GradleFabricTemplate
# Fabric Gradle Template

A simple Fabric mod template that automatically generates metadata from Gradle properties.

## Features

* Automatic `fabric.mod.json` variable replacement
* Centralized configuration through `gradle.properties`
* Easy version management
* Fabric Loom support
* Clean project structure
* GitHub-friendly setup

## Project Structure

```text
.
├── build.gradle
├── gradle.properties
└── src
    └── main
        └── resources
            └── fabric.mod.json
```

## Configuration

Edit `gradle.properties`:

```properties
mod_id=my_mod
mod_version=1.0.0
mod_name=My Mod
author=YourName
```

All values are automatically injected into `fabric.mod.json` during the build process.

## Building

```bash
./gradlew build
```

Build outputs can be found in:

```text
build/libs/
```

## Example

`fabric.mod.json`

```json
{
  "id": "${mod_id}",
  "version": "${mod_version}",
  "name": "${mod_name}"
}
```

After building:

```json
{
  "id": "my_mod",
  "version": "1.0.0",
  "name": "My Mod"
}
```

## Requirements

* Java 21+
* Gradle
* Fabric Loom

## License

MIT License
