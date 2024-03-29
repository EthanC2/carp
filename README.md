# C.A.R.P.: A Commandline Argument Parser
A light-weight commandline argument parser, originally built to support my [password cracker](https://github.com/EthanC2/password-cracker). This parser was designed to make
processing commandline arguments easier by allowing the programmer to directly query whether or not an argument was provided; in addition to querying arguments, the parser
supports querying the parameters of and argument. Being light-weight, the parser makes no unncessary allocations (using C++17's [string_view](https://docs.microsoft.com/en-us/cpp/standard-library/string-view?view=msvc-170)) and only supports the necessary
features for a parser: 

# Features
- Argument building using the builder pattern
- Long and short names for arguments
- Support for value-accepting arguments
- Program info and built-in support for `--help`
- Built-in type-casting with `try_parse_integer()`, `try_parse_floating_point()`,  `try_parse_bool()`, and `try_parse_user_defined()`

# Planned Features
- Subcommands (also called subparsers)
- Remove exceptions where possible (via nullptr and std::optional)
- Update 'ArgAction' to SingleValue, ManyValue, Flag, and Count.

- Make sure the parser complies with [POSIX Utility Conventions](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html)
