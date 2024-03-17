# Data Design

The design of a database - whether it is the data within it or the schema of it - can be done through several concepts in MySQL.

## Data Types

There are three main data types, all of which have their own sub-types:

* Numeric – data used for calculations
* Text – data used for non-calculated values (postcodes, email addresses, etc.)

These data types are assigned to the fields within database tables.

From here, we can construct a baseline constraint for the type of data we store in each table.

## Numeric Data

Numeric data is data which is used for calculations, such as prices, quantities, etc.

Below is a list of the most common numeric data types that can be used in MySQL:

|     Type     |  Min Storage Value   |   Max Storage Value   |        Example         |
|:------------:|:--------------------:|:---------------------:|:----------------------:|
|   **BIT**    |          1           |          64           |           63           |
|  **BOOLEAN**   |         -128         |          127          | 0 or 1 (False or True) |
|   **TINYINT**    |         -128         |          127          |           47           |
|   **SMALLINT**   |        -32768        |         32767         |          5923          |
|  **MEDIUMINT**   |       -8388608       |        8388607        |         -83320         |
|     **INT**      |     -2147483748      |      2147483747       |           12           |
|    **BIGINT**    | -9223372036854775808 |  922337203685477507   |       7642384732       |
|   **DECIMAL**    | [LOWER THAN BIG INT] | [HIGHER THAN BIG INT] |        35D.30D         |
| **FLOAT/DOUBLE** | [HARDWARE DEPENDENT] | [HARDWARE DEPENDENT]  |          BIT           |

## Text Data

Text data is data which isn't used for calculations, but rather just information we wish to contain, such as names, addresses, phone numbers, etc.

Below is a list of some of the different text-based data types that can be used in MySQL:

|  Type   |      Format       |  Style   |
|:-------:|:-----------------:|:--------:|
|  **CHAR**   | 0-255 characters  |  Fixed   |
| **VARCHAR** | 0-65535 character | Variable |

**CHAR** has fixed length - if a field is of type CHAR(20), the length of that field will always be 20.

**VARCHAR** doesn't have a fixed length, which saves on memory and is easier to search for.

There are other text-based data types that are stored in binary format, instead of characters.

These are more efficient due to less overhead, so they don’t need to store data in the character set.
