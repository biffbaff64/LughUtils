LUGHUTILS Utility Library
=========================
                                                         
NOTE: This project is currently in development. Most classes still need to be
      fully documented, and some features may be missing.

LUGHUTILS is a utility library designed to provide a collection of useful functions
and classes for various programming tasks. It aims to simplify common operations and
enhance productivity by offering reusable components.

This is a Companion repository to the main LughSharp 2D Game Framework project, which can
be found at:

[www.github.com/biffbaff64/LughSharp](https://www.github.com/biffbaff64/LughSharp)

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

 - Alignment
 - BaseClassFactory
 - BinaryHeap
 - Bits
 - Buffer<T>
 - BufferUtils
 - ByteOrder
 - BytePointerToString
 - CaseInsensitiveEnumArrayConverterFactory
 - ComparableTimSort
 - Constants
 - DataInput
 - DataOutput
 - DataUtils
 - GCSuppressor
 - GdxNativesLoader
 - HashHelpers
 - IClearablePool
 - IClipboard
 - ICloseable
 - IDrawable
 - IManaged
 - IReadable
 - IResetable
 - IRunnable
 - LughTestAdapter
 - PerformanceCounter
 - PerformanceCounters
 - PhysicsUtils
 - PropertiesUtils
 - QuadTreeFloat
 - QuickSelect
 - Scaling
 - ScreenUtils
 - Selector
 - SingletonBase<T>
 - SortUtils
 - StringUtils
 - SystemArrayUtils
 - Timer
 - TimeUtils
 - TimSort

 - Collections
   - ArrayList
   - ArrayListEnumerator
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
   - SnapshotArrayList

 - Exceptions
   - AssetNotLoadedException
   - BufferOverflowException
   - BufferUnderflowException
   - GdxRuntimeException
   - Guard
   - NumberFormatException
   - ReadOnlyBufferException
   - SerializationException

 - Logging
   - FPSLogger
   - IPreferences
   - Logger
   - Preferences
   - Stats

 - Maths
   - FloatCounter
   - MathUtils
   - NumberUtils
   - WindowedMean

 - Pooling
   - FlushablePool
   - IPoolable
   - Pool
   - PooledLinkedList
   - Pools
   - ReflectionPool

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
