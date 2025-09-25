# LUGHUTILS Utility Library

NOTE: This project is currently in development. Most classes still need to be
fully documented, and some features may be missing.

## Description

LUGHUTILS is a utility library designed to provide a collection of useful functions
and classes for various programming tasks. It aims to simplify common operations and
enhance productivity by offering reusable components.

This is a Companion repository to the main [LughSharp 2D Game Framework](https://www.github.com/biffbaff64/LughSharp)
project,
and that is its primary purpose. It can, however, be used as a standalone library and,
if you find it useful, please feel free to do so.

I will be adding more features and improvements over time, so stay tuned for updates!

### Table of Contents

- [Installation](#installation)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

### Installation

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


### Classes

#### Main Namespace

- Alignment
    - Provides utility methods and constants for handling alignment using bit flags.
      This is useful for positioning and aligning UI elements or game objects.
  

- BaseClassFactory
    - Provides a base class for factory implementations that require initialization logic.


- BinaryHeap
    - A binary heap that stores nodes which each have a float value and are sorted either
      lowest first or highest first.
  

- Bits
    - A bitset, without size limitation, allows comparison via bitwise operators to other bitfields.
  

- Buffer
    - Represents a generic, resizable buffer for unmanaged types, supporting byte-level and
      element-level operations, endianness, and direct/bulk access.
  

- ByteOrder
    - A typesafe enumeration for byte orders.
  

- CaseInsensitiveEnumArrayConverterFactory
    - Various util classes for working with enum arrays.
  

- ComparableTimSort
    - A near duplicate of [TimSort<T>](#TimSort), modified for use with arrays of objects that implement
      IComparable, instead of using explicit comparators.
  

- DataOutput
    - Extends BinaryWriter with additional convenience methods.
  

- DataUtils
    - Various utility functions for working with data.
  

- GCSuppressor
    - GC Suppression utilities.
  

- HashHelpers
    - Provides helper methods and constants for efficient hash table index calculations, including
      support for Fibonacci hashing and bitmask/shift computations for power-of-two table sizes.
  

- PerformanceCounter
  - Class to keep track of the time and load (percentage of total time) a specific task takes.
  

- PerformanceCounters
    - Class to keep track of a group of PerformanceCounter instances.
  

- PropertiesUtils
    - A helper class that allows you to load and store key/value pairs of an Dictionary<TK,TV>
      with the same line-oriented syntax supported by IPreferences.
  

- QuadTreeFloat
    - A quad tree that stores a float for each point.
  

- QuickSelect
    - Implementation of Tony Hoare's quickselect algorithm.
  

- SystemArrayUtils
    - Utility methods for working with System.Array.
  

- TimeUtils
    - Helper functions for working with System.DateTime and System.TimeSpan.
  

- TimSort
    - A stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons
      when running on partially sorted arrays, while offering performance comparable to a
      traditional mergesort when run on random arrays.


#### Collections Namespace

- ByteArray
   - a resizable array structure for storing bytes (byte). It supports both ordered and
     unordered modes:
  
       - Ordered Mode: Maintains the order of elements when adding or removing.
       - Unordered Mode: Optimizes removal by moving the last element into the removed position,
         avoiding memory copies.

   - Key Features
       - Resizable Storage: Automatically grows the internal array as needed.
       - Constructors: Multiple constructors allow creation from capacity, another
         ByteArray, or a raw byte[].
       - Add/Insert/Remove: Methods to add, insert, and remove bytes or ranges.
       - Access/Modify: Get, set, increment, and multiply values at specific indices.
       - Search: Methods to check for containment, find index/last index of a value.
       - Bulk Operations: Add all, remove all, insert ranges, and clear.
       - Utility: Sort, reverse, shuffle, truncate, shrink, ensure capacity, and
         convert to array.
       - Stack-like Methods: Pop, Peek, and First for stack/queue semantics.
       - Equality and Hashing: Custom Equals and GetHashCode implementations (note:
         hash code is a placeholder).
       - String Representation: ToString methods for formatted output. 

   - Properties
       - Items: The backing array of bytes.
       - Size: The current number of elements.
       - Ordered: Whether the array maintains order.

   - Usage
     This class is useful for scenarios requiring efficient, dynamic byte storage with
     optional order preservation, such as buffer management, serialization, or custom
     data structures.

- DelayedRemovalList 
    - An list that queues removal during iteration until the iteration has completed. Queues
      any removals done after Begin() is called to occur once End() is called. This can allow
      code out of your control to remove items without affecting iteration.
      
- DictionaryExtensions
    - A collection of extension methods for working with IDictionary<TKey, TValue> instances.

- IdentityMap
    - An unordered map that uses identity comparison for the object keys. Null keys are not
    - allowed. No allocation is done except when growing the table size.

- ListExtensions
    - A collection of extension methods for working with IList<T> instances.

- ObjectMap
    - An unordered map where the keys and values are objects.
    
- OrderedMap
    - An ObjectMap{TK,TV} that also stores Keys in an List{T} using the insertion order.
    - Null Keys are not allowed. No allocation is done except when growing the table size.

- PredicateIterable
    - A collection of extension methods for filtering and iterating over IEnumerable<T> instances.

- PredicateIterator
    - A collection of extension methods for filtering and iterating over IEnumerator<T> instances.

- SnapshotArrayList—( Still in development )
    - An array that allows modification during iteration. Guarantees that array entries provided
      by begin() between indexes 0 and size at the time begin was called will not be modified
      until end() is called. If modification of the SnapshotArray occurs between begin/end, the
      backing array is copied prior to the modification, ensuring that the backing array that was
      returned by begin() is unaffected. To avoid allocation, an attempt is made to reuse any
      extra array created as a result of this copy on subsequent copies.
      Note that SnapshotArray is not for thread safety, only for modification during iteration.
  

#### Exceptions Namespace

- AssetNotLoadedException
    - Exception used for signalling asset load failures.
- GdxRuntimeException
    - Typed runtime exception for use when no suitable exception type exists.
- Guard
    - Utility Exception class for use in validating arguments.
- ReadOnlyBufferException
    - Unchecked exception thrown when a content-mutation method such as put or compact
      is invoked upon a read-only buffer.


#### Logging Namespace

- FPSLogger
    - A simple helper class to log the frames per seconds achieved.
- Logger
    - A class to write debug messages to console and a text file. Primarily intended for
      flow tracing, messages will display calling file/class/methods and any provided
      debug message.
- Preferences ( With accompanying IPreferences interface )
    - A Persistant Properties Manager.
- Stats
    - An extension of the Preferences class to provide a simple way to log statistics.


#### Maths Namespace

- FloatCounter
    - Tracks statistics (count, sum, min, max, average, latest, and windowed mean) for
      a sequence of floating-point values, with optional windowed mean support.
- MathUtils
    - A Collection of mathematical functions and data.
- NumberUtils
    - A Collection of mathematical functions for integer and floating-point values.
- WindowedMean
    - A simple class keeping track of the mean of a stream of values within a certain window.


#### Pooling Namespace

- Pool ( with accompanying IPoolable interface )
    - A Utility class for managing a pool of objects.
- PooledLinkedList
    - A simple linked list that pools its nodes.
- Pools
    - Stores a map of Pool<T> instances by type for convenient static access.
  
    
### Contributing

Contributions are welcome! If you find a bug or have a feature request, please open an issue on GitHub.
Feel free to fork the repository and submit pull requests for any improvements or new features.
Please ensure that your code adheres to the existing coding style and includes appropriate tests.
Before submitting a pull request, make sure to run all tests to ensure nothing is broken.

### License

This project is licensed under the MIT License. See the LICENSE file for details.

### Contact

For any questions or inquiries, please contact the maintainer at richikin@gmail.com
or visit the GitHub repository at www.github.com/biffbaff64/LughUtils.

Thank you for using LUGHUTILS!

