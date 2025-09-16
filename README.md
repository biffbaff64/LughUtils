LUGHUTILS Utility Library
=========================
                                                         
NOTE: This project is currently in development. Most classes still need to be
      fully documented, and some features may be missing.

LUGHUTILS is a utility library designed to provide a collection of useful functions
and classes for various programming tasks. It aims to simplify common operations and
enhance productivity by offering reusable components.

This is a Companion repository to the main [LughSharp 2D Game Framework](https://www.github.com/biffbaff64/LughSharp) project,
and that is its primary purpose. It can, however, be used as a standalone library and,
if you find it useful, please feel free to do so.

I will be adding more features and improvements over time, so stay tuned for updates!

Table of Contents
-----------------
- [Installation](#installation)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

Installation
------------
LUGHUTILS is available as a Nuget package. You can install it via the NuGet Package Manager Console.

To install via NuGet, use the following command:
```
Install-Package LughUtils
```
Or via the .NET CLI:
```
dotnet add package LughUtils
```
Alternatively, you can clone the repository or download the source code directly.
The library is compatible with .NET Standard, making it suitable for a wide range of applications.
You can include the source files in your project or compile them into a DLL for easier distribution.


Features
--------

 - <b>Alignment</b>
    - Provides utility methods and constants for handling alignment using bit flags.
      This is useful for positioning and aligning UI elements or game objects.
 - <b>BaseClassFactory</b>
    - Provides a base class for factory implementations that require initialization logic.
 - <b>BinaryHeap</b>
    - A binary heap that stores nodes which each have a float value and are sorted either
      lowest first or highest first.
 - <b>Bits</b>
    - A bitset, without size limitation, allows comparison via bitwise operators to other bitfields.
 - <b>Buffer</b>
    - Represents a generic, resizable buffer for unmanaged types, supporting byte-level and
      element-level operations, endianness, and direct/bulk access.
 - <b>ByteOrder</b>
   - A typesafe enumeration for byte orders.
 - <b>CaseInsensitiveEnumArrayConverterFactory</b>
   - Various util classes for working with enum arrays.
 - <b>ComparableTimSort</b>
   - A near duplicate of [TimSort<T>](#TimSort), modified for use with arrays of objects that implement
     IComparable, instead of using explicit comparators.
 - <b>DataOutput</b>
   - Extends BinaryWriter with additional convenience methods.
 - <b>DataUtils</b>
   - Various utility functions for working with data.
 - <b>GCSuppressor</b>
   - GC Suppression utilities.
 - <b>HashHelpers</b>
   - Provides helper methods and constants for efficient hash table index calculations, including
     support for Fibonacci hashing and bitmask/shift computations for power-of-two table sizes.
 - <b>PerformanceCounter</b>
   - Class to keep track of the time and load (percentage of total time) a specific task takes.
 - <b>PerformanceCounters</b>
   - Class to keep track of a group of PerformanceCounter instances.
 - <b>PropertiesUtils</b>
   - A helper class that allows you to load and store key/value pairs of an Dictionary<TK,TV>
     with the same line-oriented syntax supported by IPreferences.
 - <b>QuadTreeFloat</b>
   - A quad tree that stores a float for each point.
 - <b>QuickSelect</b>
   - Implementation of Tony Hoare's quickselect algorithm.
 - <b>SystemArrayUtils</b>
   - Utility methods for working with System.Array.
 - <b>TimeUtils</b>
   - Helper functions for working with System.DateTime and System.TimeSpan.
 - <b>TimSort</b>
   - A stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons
     when running on partially sorted arrays, while offering performance comparable to a
     traditional mergesort when run on random arrays.


 - <b>Collections</b>
   - ByteArray
   - DelayedRemovalList
   - DictionaryExtensions
   - IdentityMap
   - IPredicate
   - ListExtensions
   - ObjectMap
   - OrderedMap
   - PredicateIterable
   - PredicateIterator
   - SnapshotArrayList - TODO


 - <b>Exceptions</b>
   - <b>AssetNotLoadedException</b>
     - Exception used for signalling asset load failures.
   - <b>GdxRuntimeException</b>
     - Typed runtime exception for use when no suitable exception type exists.
   - <b>Guard</b>
     - Utility Exception class for use in validating arguments.
   - <b>ReadOnlyBufferException</b>
     - Unchecked exception thrown when a content-mutation method such as put or compact
       is invoked upon a read-only buffer.


 - <b>Logging</b>
   - <b>FPSLogger</b>
     - A simple helper class to log the frames per seconds achieved.
   - <b>Logger</b>
     - A class to write debug messages to console and a text file. Primarily intended for
       flow tracing, messages will display calling file/class/methods and any provided
       debug message.
   - <b>Preferences ( With accompanying IPreferences interface )</b>
     - A Persistant Properties Manager.
   - <b>Stats</b>
     - An extension of the Preferences class to provide a simple way to log statistics.


 - <b>Maths</b>
   - <b>FloatCounter</b>
     - Tracks statistics (count, sum, min, max, average, latest, and windowed mean) for
       a sequence of floating-point values, with optional windowed mean support.
   - <b>MathUtils</b>
     - A Collection of mathematical functions and data.
   - <b>NumberUtils</b>
     - A Collection of mathematical functions for integer and floating-point values.
   - <b>WindowedMean</b>
     - A simple class keeping track of the mean of a stream of values within a certain window.


 - <b>Pooling</b>
   - <b>Pool ( with accompanying IPoolable interface )</b>
     - A Utility class for managing a pool of objects.
   - <b>PooledLinkedList</b>
     - A simple linked list that pools its nodes.
   - <b>Pools</b>
     - Stores a map of Pool<T> instances by type for convenient static access.

Contributing
------------

Contributions are welcome! If you find a bug or have a feature request, please open an issue on GitHub.
Feel free to fork the repository and submit pull requests for any improvements or new features.
Please ensure that your code adheres to the existing coding style and includes appropriate tests.
Before submitting a pull request, make sure to run all tests to ensure nothing is broken.

License
-------
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
-------
For any questions or inquiries, please contact the maintainer at richikin@gmail.com
or visit the GitHub repository at www.github.com/biffbaff64/LughUtils.
Thank you for using LUGHUTILS!

