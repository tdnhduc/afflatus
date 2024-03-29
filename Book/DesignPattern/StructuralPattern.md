# STRUCTURAL DESIGN PATTERN 

> These design patterns are about _**organizing different classes and objects to form larger structures and provide new functionality**_.

> Structural design patterns are _**Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Private Class Data, and Proxy**_.


|Pattern|Intent|
|:---|:---|
|Adapter|_**convert interfaces**_. Adapter let's two components _**working together**_, which wouldn't be working because of incompatible interfaces|
|Decorator|_**adds new functionalities at runtime**_. It allows you to enrich the object, even after it's creation.|
|Facade|neither converts interfaces nor adds new functionality, instead, it just _**provides simpler interfaces**_.|
|Proxy|_**act as real object**_ and can provide alternate behavior or forward request to original object.|

## Decorator Pattern 
> View on: [**refactoring.guru**](https://refactoring.guru/design-patterns/decorator)

2. **Solution**

<img src="https://refactoring.guru/images/patterns/diagrams/decorator/example-2x.png?id=4891323a27d5601a174e" />

3. **Example** :
```java
// The component interface defines operations that can be
// altered by decorators.
interface DataSource is
    method writeData(data)
    method readData():data

// Concrete components provide default implementations for the
// operations. There might be several variations of these
// classes in a program.
class FileDataSource implements DataSource is
    constructor FileDataSource(filename) { ... }

    method writeData(data) is
        // Write data to file.

    method readData():data is
        // Read data from file.

// The base decorator class follows the same interface as the
// other components. The primary purpose of this class is to
// define the wrapping interface for all concrete decorators.
// The default implementation of the wrapping code might include
// a field for storing a wrapped component and the means to
// initialize it.
class DataSourceDecorator implements DataSource is
    protected field wrappee: DataSource

    constructor DataSourceDecorator(source: DataSource) is
        wrappee = source

    // The base decorator simply delegates all work to the
    // wrapped component. Extra behaviors can be added in
    // concrete decorators.
    method writeData(data) is
        wrappee.writeData(data)

    // Concrete decorators may call the parent implementation of
    // the operation instead of calling the wrapped object
    // directly. This approach simplifies extension of decorator
    // classes.
    method readData():data is
        return wrappee.readData()

// Concrete decorators must call methods on the wrapped object,
// but may add something of their own to the result. Decorators
// can execute the added behavior either before or after the
// call to a wrapped object.
class EncryptionDecorator extends DataSourceDecorator is
    method writeData(data) is
        // 1. Encrypt passed data.
        // 2. Pass encrypted data to the wrappee's writeData
        // method.

    method readData():data is
        // 1. Get data from the wrappee's readData method.
        // 2. Try to decrypt it if it's encrypted.
        // 3. Return the result.

// You can wrap objects in several layers of decorators.
class CompressionDecorator extends DataSourceDecorator is
    method writeData(data) is
        // 1. Compress passed data.
        // 2. Pass compressed data to the wrappee's writeData
        // method.

    method readData():data is
        // 1. Get data from the wrappee's readData method.
        // 2. Try to decompress it if it's compressed.
        // 3. Return the result.

// Option 1. A simple example of a decorator assembly.
class Application is
    method dumbUsageExample() is
        source = new FileDataSource("somefile.dat")
        source.writeData(salaryRecords)
        // The target file has been written with plain data.

        source = new CompressionDecorator(source)
        source.writeData(salaryRecords)
        // The target file has been written with compressed
        // data.

        source = new EncryptionDecorator(source)
        // The source variable now contains this:
        // Encryption > Compression > FileDataSource
        source.writeData(salaryRecords)
        // The file has been written with compressed and
        // encrypted data.

// Option 2. Client code that uses an external data source.
// SalaryManager objects neither know nor care about data
// storage specifics. They work with a pre-configured data
// source received from the app configurator.
class SalaryManager is
    field source: DataSource

    constructor SalaryManager(source: DataSource) { ... }

    method load() is
        return source.readData()

    method save() is
        source.writeData(salaryRecords)
    // ...Other useful methods...

// The app can assemble different stacks of decorators at
// runtime, depending on the configuration or environment.
class ApplicationConfigurator is
    method configurationExample() is
        source = new FileDataSource("salary.dat")
        if (enabledEncryption)
            source = new EncryptionDecorator(source)
        if (enabledCompression)
            source = new CompressionDecorator(source)

        logger = new SalaryManager(source)
        salary = logger.load()
    // ...
  ```
## ADAPTER PATTERN
> View on: [**refactoring.guru**](https://refactoring.guru/design-patterns/adapter)

> _**MAIN RESPONSIBILITY**_ :  that allows objects with _**incompatible interfaces to collaborate**_.

1.  The adapter gets an interface, compatible with one of the existing objects.
2.  Using this interface, the existing object can safely call the adapter’s methods.
3.  Upon receiving a call, the adapter passes the request to the second object, but in a format and order that the second object expects.
  

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODgyODUxMjgsMjA0NjI3NzI4NSwtMT
ExNzk3MjM2MCwxNjk0OTA2OTE3LDQ2OTU0MDYzOSwtMTU1MzU1
NjYxOSwxODM2NTEyNDYwLC03MDYzNDk1MzhdfQ==
-->