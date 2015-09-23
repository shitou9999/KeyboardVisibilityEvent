KeyboardVisibilityEvent
===

[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-KeyboardVisibilityEvent-green.svg?style=flat)](https://android-arsenal.com/details/1/2519)

Android Library to handle soft keyboard visibility change event.
show/hide keyboard method is also included.

## Features
- handle keyboard visibility change
- check if keyboard is currently visible
- show/hide keyboard(check UIUtil.java)

_Please note that as described in this [issue](https://github.com/yshrsmz/KeyboardVisibilityEvent/issues/1), currently the library cannot detect visibility change when the activity's `windowSoftInputMode` do not change Activity's height(such as `adjustNothing`)._

## Installation

AAR is distributed on the Maven Central repository.

```groovy
repositories {
    mavenCentral()
}

dependencies {
    compile 'net.yslibrary.keyboardvisibilityevent:keyboardvisibilityevent:1.0.0'
}
```

## Usage

check out sample project!

### Add event listener for keyboard change event

```java
KeyboardVisibilityEvent.setEventListener(
        getActivity(),
        new KeyboardVisibilityEventListener() {
            @Override
            public void onVisibilityChanged(boolean isOpen) {
                // some code depending on keyboard visiblity status
            }
        });
```

## License

http://www.apache.org/licenses/LICENSE-2.0.txt

