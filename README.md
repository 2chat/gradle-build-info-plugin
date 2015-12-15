# gradle-build-info-plugin

[![Build Status](https://travis-ci.org/ksoichiro/gradle-build-info-plugin.svg?branch=master)](https://travis-ci.org/ksoichiro/gradle-build-info-plugin)
[![Coverage Status](https://coveralls.io/repos/ksoichiro/gradle-build-info-plugin/badge.svg?branch=master&service=github)](https://coveralls.io/github/ksoichiro/gradle-build-info-plugin?branch=master)

Gradle plugin to include build information to your JAR.

## Usage

Apply plugin:

```gradle
plugins {
    id 'com.github.ksoichiro.build.info' version '0.1.0'
}
```

Note that you can use this plugin only when you use java plugin because you build JAR:

```gradle
apply plugin: 'java'
```

Then just build your project:

```sh
./gradlew build
```

Now your Manifest in JAR includes special attributes:

```
unzip -p build/libs/yourJar.jar META-INF/Manifest.MF
```

## License

    Copyright 2015 Soichiro Kashima

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
