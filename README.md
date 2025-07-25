# Simple Logger
A sample of utilizing a Global Singleton logger as a Publisher with logging implementations that Subsribe to it.

## Usage
Fill out the appropriate data in the `MAIN.Message` and `MAIN.Source` objects. Set `LogAMessage` and the message will be logged to the LocalLogger's Messages array. The array is treated as a ring buffer in this example.

THe Global Singleton of a Publisher/Subscribe mechanism is not required to implement this. The Publisher allows for the user to implement their own logging mechanism (ADS, EventLogger, FileLogging etc etc). 
