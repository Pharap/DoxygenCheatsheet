# Examples

## Class Documentation

```cpp
/// @brief A class.
/// @details This class is used to demonstrate a number of section commands.
/// @author John Doe
/// @author Jane Doe
/// @version 4.1a
/// @date 1990-2011
/// @pre Initialise the system.
/// @bug Not all memory is freed when deleting an object of this class.
/// @warning Improper use can crash your application.
/// @copyright MIT Licence.
class SomeClass
{
};
```

## Function Documentation

```cpp
/// @brief Calculates the sine of a value.
/// @param value The value to compute the sine of, in radians.
/// @return The sine of the provided value.
double sin(double value);
```

## Page Documentation

```cpp
/// @page page1 A documentation page
/// @tableofcontents
/// Leading text.
/// @section sec An example section
/// This page contains the subsections @ref subsection1 and @ref subsection2.
/// For more info see page @ref page2.
/// @subsection subsection1 The first subsection
/// Text.
/// @subsection subsection2 The second subsection
/// More text.

/// @page page2 Another page
/// Even more info.
```