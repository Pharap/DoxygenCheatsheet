# Doxygen Command Cheatsheet

## Basic Commands

### brief

Begins a brief description of an entity.

### details

Begins a detailed description of an entity.

### remark

Begins a remark.

### remarks

Same as [`remark`](#remark)

### attention

Identifies information that requires particular attention.

### see

Cross references an entity.
A reference can refer to a class, function, method, variable or file, or be a URL.

### sa

Same as [`see`](#see)

### anchor

Adds a named anchor into the documentation.
(E.g. for HTML, generates an `id` attribute for a tag.)

See [`ref`](#ref) for an example.

### ref

Adds a reference to a named section, subsection, page or anchor into the documentation.
(E.g. for HTML, generates an `a` tag with a `href` pointing to an anchor.)

**Example**

```cpp
/// @anchor AnchorName

// Some code...

/// @ref AnchorName 
```

### verbatim

TBC

### endverbatim

TBC

### \\~

Specifies documentation for a particular language.

**Example:***
```cpp
/// \~english This is English.
/// \~german Dies ist Detsch.
/// \~dutch Dit is Nederlands.
/// \~japanese これは日本語です。
/// \~ This applies to all languages.
```

## Code Information

### since

Identifies the first version or time at which an entity became avaiable.

### bug

Documents a bug.

### deprecated

Documents a deprecated feature or entity.
Ideally used to direct the reader to an alternative.

### warning

Creates a warning block to provide a warning to the reader.

### test

Describes a test.
(Tests are added to a designated test list and cross-referenced.)

### code

Begins a block of source code.
Must be followed by [`endcode`](#endcode).

To explicitly identify the code language use a file extension within curly braces.

**Example:**
```cpp
/// @code{.cpp}
/// void main() {}
/// @endcode
///
/// @code{.py}
/// def main():
///     pass;
/// @endcode
///
/// @code{.unparsed}
/// Plaintext in a code block.
/// @endcode
```

### endcode

Ends a block of source code.
Must be preceded by [`code`](#code).

### example

Identifies a file that contains example code.
For code examples to be contained within a doc-comment use [`code`](#code) instead.

**Example:**

```cpp
/// @example usage_example.cpp
```

## Metadata

### author

Documents one or more authors.

### authors

Same as [`author`](#author).

### copyright

Documents copyright information.
Useful for identifying a licence.

### date

Specifies a date.

### version

Specifies a version number.

## Function-Specific

### return

Documents the return value of a function.

### returns

Same as [`return`](#return).

### result

Same as [`return`](#return).

### param

Documents a function parameter.

**Syntax:**

`@param '[' direction ']' <parameter-name> {parameter-description}`

**Examples:**

```cpp
/// @param[out] desination The destination memory block.
/// @param[in] source The source memory block.
/// @param[in] size The number of bytes to copy.
void memcpy(void * destination, const void * source, std::size_t size);
```

```cpp
/// @param x,y,z The coordinates of the point in 3D space.
void setPosition(double x, double y, double z);
```

## Manual Documentation

### define

Documents a macro (i.e. `#define`).

### retval

## Misc

### dot

Begins a DOT graph description.
Must be followed by [`enddot`](#enddot).

Note: 'DOT' is a graph description language. See [Wikipedia](https://en.wikipedia.org/wiki/DOT_%28graph_description_language%29).

**Syntax:**

`@dot [caption] [<size-indication>=<size>]`

### enddot

Ends a DOT graph description.
Must be preceded by [`dot`](#dot).

### dotfile

Inserts a DOT graph using the description in the specified file.

### msc

Begins a message sequence chart description.
Must be followed by [`endmsc`](#endmsc).

Note: See http://www.mcternan.me.uk/mscgen/ for more information.

### endmsc

Ends a message sequence chart description.
Must be preceded by [`msc`](#msc).

### mscfile

Inserts a message sequence chart using the description in the specified file.

### diafile

Inserts a diagram created with Dia.

### image

Inserts an image into the documentation.
Can insert `html`, `latex`, `docbook` or `rtf`.