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

## Example

Dump the following into a terminal to create a demo program:

```
cd /tmp
cat > main.c << 'EOF'
#include <stdlib.h>
#include <stdio.h>
#include "hexify/hexify.h"

int main(int argc, char **argv) {
    unsigned char binary[4];
    binary[0] = 0xde;
    binary[1] = 0xad;
    binary[2] = 0xbe;
    binary[3] = 0xef;
    char hex[8+1];
    hexify(binary, sizeof(binary), hex, sizeof(hex));    
    printf("%s\n", hex);
    return EXIT_SUCCESS;
}
EOF
clib install pepaslabs/hexify.c
gcc -Wall -Werror -c deps/hexify/*.c
gcc -Wall -Werror -Ideps *.o main.c
```

Try it out:

```
$ ./a.out
deadbeef
```

## License

[MIT](https://opensource.org/licenses/MIT)
