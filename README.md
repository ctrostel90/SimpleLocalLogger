# Simple Logger
A sample of utilizing a Global Singleton logger as a Publisher with logging implementations that Subsribe to it.

## Usage
Fill out the appropriate data in the `MAIN.Message` and `MAIN.Source` objects. Set `LogAMessage` and the message will be logged to the LocalLogger's Messages array. The array is treated as a ring buffer in this example.

The Global Singleton of a Publisher/Subscribe mechanism is not required to implement this. The Publisher allows for the user to implement their own logging mechanism (ADS, EventLogger, FileLogging etc etc). 

## Argument Example
Set `ArgumentExample` to True to see the arguments enter the log. This showcases how the same `LogMessage` method can be used for different argument types.

Arguments are implemented by creating an object that implements `I_SimpleLogArgument` then passing the argument object via the `LogMessage(Source,Message,Argument)` method. The Argument is an optional input and does not have to be used.

`I_SimpleLogArgument` just contains `I_Base` and a `ToString()` method. The `LogMessage()` implementation checks if the Argument input is != 0. If so, it appends the `Argument.ToString()` to the Log Entry.

## Expansion
- Users could expand by implementing custom loggers (ADS, File, EventLogger etc..)
- Users could expand by implementing custom parsing of the Source/Message structures
- Users could modify to not use Classes/Objects and instead structures for the Source/Message inputs (or change to any other types as desired)
