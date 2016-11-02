# hexify.c
Convert binary data (unsigned char*) into a hexidecimal string

## Installation

  Install with [clib](https://github.com/clibs/clib):

```
$ clib install pepaslabs/hexify.c
```

## API

```c
int hexify(unsigned char *in, size_t in_size, char *out, size_t out_size);
```

## License

[MIT](https://opensource.org/licenses/MIT)
