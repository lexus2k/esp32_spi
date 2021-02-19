# esp32_spi

## Usage example

```.cpp
#include "spibus.h"
WireSPI SPI;

...
    SPI.begin();
...
    SPI.beginTransaction( 1000000, -1, 0); //  Start transaction at 1MHz in SPI mode 0, CS is not specified (-1)
    SPI.transfer(data, len); // Transfer buffer data of length len bytes
    SPI.endTransaction();    // End transaction
...
    SPI.end();
...

```
