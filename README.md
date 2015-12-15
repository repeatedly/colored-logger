# Colored Logger

Color your log message.

This depends on [std.experimental.logger](http://dlang.org/phobos/std_experimental_logger.html).

# Example

```d
import coloredlogger;
import std.experimental.logger : LogLevel;
import std.stdio : stdout;

void main()
{
    auto logger = new ColoredLogger(stdout, LogLevel.all);

    logger.trace("trace");
    logger.info("info");
    logger.warning("warning");
    logger.error("error");
    logger.critical("critical");
    logger.fatal("fatal");
}
```

![example](https://i.gyazo.com/6dcaf43bcb963a894d003368b50aa5d7.png)

## Change color

You can change color setting by passing `string[LogLevel]` object to 2nd argument.

```d
new ColoredLogger(stdout, [LogLevel.info : ColoredLogger.Color.White], LogLevel.all);
```

# Copyright

Copyright (c) 2015- Masahiro Nakagawa

# License

Distributed under the [Boost Software License, Version 1.0](http://www.boost.org/users/license.html).
