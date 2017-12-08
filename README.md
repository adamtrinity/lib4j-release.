# lib4j-release.
Bit-Lib4j is an useful library to handle bytes or bits in Java. With this library you can read/write data in a byte array with a custom size for Java primitive types.
Bit-lib4j Build Status Coverage Status

Bit-Lib4j is an useful library to handle bytes or bits in Java.
With this library you can read/write data in a byte array with a custom size for Java primitive types.

Maven Central

Simple API

It is very easy to get started with bit-lib4j:

Read data from byte array
	byte[] array = new byte[]{0x12,0x25}
	BitUtils bit = new BitUtils(array);
	int res = bit.getNextInteger(4);        // read the first 4 bits to an integer
Create byte array with bit
	BitUtils bit = new BitUtils(8);
	bit.setNextInteger(3,3);        // set an integer on 3 bits
	bit.setNextInteger(1,5);        // set one value on 5 bits

	// Result
	bit.getData();                  // return Ox61  (0110 0001b)
Read/write signed values
	BitUtils bit = new BitUtils(4);
	bit.setNextInteger(-2 , 4);	    // set an integer (-2) on 3 bits

	// Result
	bit.getNextIntegerSigned(4);    // return -2
You can also use getNextSignedLong() to handle long signed values.

Handle bytes more easily

The class ByteUtils provided static methods to convert byte array to String, String to byte array, int to byte array, byte array to binary representation.

More documentation into the wiki

Download

Maven

<dependency>
  <groupId>com.github.devnied</groupId>
  <artifactId>bit-lib4j</artifactId>
  <version>1.5.0</version>
</dependency>
JAR

You can download this library on Maven central or in Github release tab

Dependencies

If you are not using Maven or some other dependency management tool that can understand Maven repositories, the list below is what you need to run bit-lib4j.

Runtime Dependencies

slf4j-api 1.7.5
Bugs

Please report bugs and feature requests to the GitHub issue tracker.
Forks and Pull Requests are also welcome.
