# Functions, Operators, and Arguments
## R Programming

### Week 1 Lectures
#### Console Input and Evaluation

| Operator / Symbol | Description |
|:---: |:--- |
| `<-` | assignment operator |
| `#` | comment character |
| `:` | creates integer sequence |

| Function | Description |
|:--- |:--- |
| `print()` | explicit printing method |

#### R Data Types - Objects and Attributes

| Operator / Symbol | Description |
|:--- |:--- |
| `L` | as suffix to a number, specifies an integer |
| `Inf` | infinity |
| `NaN` | undefined number |

| Function | Description |
|:--- |:--- |
| `vector()` | creates empty vector; attributes = type, length |
| `attributes()` | accesses the attributes; used to set or modify if user-defined |

##### Common object attributes
* `class` - has by default
* `length` - has by default
* `names` - optional?
* `dimnames` - dimension names in matrices

#### R Data Types - Vectors and Lists

| Function | Description |
|:——- |:——- |
| `c()` | creates vector by concatenating elements |
| `as.*()` | coerces explicitly to a particular class where possible, or NAs if not |
| `list()` | creates list; elements may be of any class | 

#### R Data Types - Matrices

| Function | Description |
|:——- |:——- |
| `matrix()` | creates empty matrix; by definition, a vector with `dim` attribute |
| `cbind()` | column-binds vectors to create matrix |
| `rbind()` | row-binds vectors to create matrix |

##### Matrix attributes
* `dim` - dimensions; is itself a vector of 2 elements \(nrow, ncol\)
* `nrow` - number of rows
* `ncol` - number of columns

#### R Data Types - Factors

| Function | Description |
|:——- |:——- |
| `factor()` | creates factor from character vector input; has `levels` attribute |
| `table()` | gives a frequency count of each level in a factor |
| `unclass()` | reveals the underlying integer vector for a factor |

#### R Data Types - Missing Values

| Function | Description |
|:——- |:——- |
| `is.na()` | tests for all missing values, including NaNs |
| `is.nan()` | tests for NaNs | 

#### R Data Types - Data Frames

| Function | Description |
|:——- |:——- |
| `read.table()` | creates a data frame already populated  |
| `read.csv()` | creates a data frame already populated |
| `data.matrix()` | converts data frame to matrix - but coerces to one type |
| `data.frame()` | creates data frame by defining it as a type of list |

##### Data Frame attributes
* `row.names` - as advertised

#### R Data Types - Names

| Function | Description |
|:——- |:——- |
| `names()` | accesses or defines names of vector elements in an object  |
|  | can be done within the `list()` function for lists |
|  | or with the `dimnames()` equivalent for matrices |

#### Reading Tabular Data

| Function | Description |
|:——- |:——- |
| `readLines()` | reads in text files  |
| `source()`  | reads in R code to reconstruct multiple objects |
| `dget()` | reads in R code to reconstruct single object |
| `load()` | reads in saved workspaces |
| `unserialize()` | reads in single binary objects |
| `write.table()` | writes data to a table |
| `writeLines()` | writes a character vector line by line to a text file  |
| `dput()` | writes object as R code that can later reconstruct the object |
| `dump()`  | equivalent to `dput()` but takes multiple objects |
| `save()` | writes to saved workspaces |
| `serialize()` | creates single binary objects |

##### Arguments for read.table()
* `file` - string; name of file or connection
* `header` - logical; does it have one?
* `sep` - string; separator character
* `colClasses` - character vector
* `nrows` - number of rows
* `comment.char` - sets (if other than default #)
* `skip` - specifies rows from top to skip 
* `stringsAsFactors` - logical; columns with strings assumed to be factors? default true

#### Reading Large Tables

| Function | Description |
|:——- |:——- |
| `sapply()` | applies a function to elements in a list  |

#### Connections: Interfaces to the Outside World

| Function | Description |
|:——- |:——- |
| `file()` | connects to a standard uncompressed file  |
| `gzfile()` | connects to a file compressed with gzip  |
| `bzfile()` | connects to a file compressed with bzip2  |
| `url()` | connects to a website  |

##### Arguments for file()
- `description` - string; name of the file
- `open` - can be set with one of these flags:
  - `r` read
  - `w` write
  - `a` append
  - `rb` read binary
  - `wb` write binary
  - `ab` append binary

#### Subsetting R Objects: Basics

| Operator or Symbol | Description |
|:——- |:——- |
| `[]` | extracts multiple elements; returns same class as original object |
| `[[]]` | extracts single element of list or data frame, but the element can be nested; returns any class; can use computed index |
| `$` | extracts single element of list or data frame; by its name rather than by index |

#### Subsetting R Objects: Missing Values

| Function | Description |
|:——- |:——- |
| `complete.cases()` | used to remove missing values from multiple elements or data frames  |

#### Vectorized Operations

| Operator or Symbol | Description |
|:——- |:——- |
| `% * %` | true matrix multiplication; i.e. not element-wise  |

| Function | Description |
|:——- |:——- |
| `rep(VALUE, NUMBER OF TIMES)` | repeats same value, e.g. when filling a matrix  |











