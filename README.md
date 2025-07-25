# Simple Logger
A sample of utilizing a Global Singleton logger as a Publisher with logging implementations that Subsribe to it.

## Usage
Fill out the appropriate data in the `MAIN.Message` and `MAIN.Source` objects. Set `LogAMessage` and the message will be logged to the LocalLogger's Messages array. The array is treated as a ring buffer in this example.

THe Global Singleton of a Publisher/Subscribe mechanism is not required to implement this. The Publisher allows for the user to implement their own logging mechanism (ADS, EventLogger, FileLogging etc etc). 

## Expansion
- Users can expand by augmenting the properties inside the Source and Message interfaces/structures
- Users could expand by implementing custom parsing of the Source/Message structures
- Users could expand by adding arguments to the LogMessage() method
- Users could modify to not use Classes/Objects and instead structures for the Source/Message inputs (or change to any other types as desired)
