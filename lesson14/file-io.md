# File Input/Output (I/O)

## Reading Material

- [Intro to File Input & Output (UPenn)](https://www.seas.upenn.edu/~cis1xx/resources/java/fileIO/introToFileIO.html)
- [Byte Streams (Java Tutorials handbook)](https://docs.oracle.com/javase/tutorial/essential/io/bytestreams.html)
- [Character Streams (Java Tutorials handbook)](https://docs.oracle.com/javase/tutorial/essential/io/charstreams.html)
- [Buffered Streams (Java Tutorials handbook)](https://docs.oracle.com/javase/tutorial/essential/io/buffers.html)

## Processing Individual Characters: File Reader and File Writer

Java Byte streams are used to perform input and output of 8-bit bytes, whereas Java Character streams are used to perform input and output for 16-bit unicode. Though there are many classes related to character streams but the most frequently used classes are FileReader and FileWriter. Though internally FileReader uses FileInputStream and FileWriter uses FileOutputStream but here the major difference is that FileReader reads two bytes at a time and FileWriter writes two bytes at a time.

```java
import java.io.*;
public class CopyFile {

   public static void main(String args[]) throws IOException {
      FileReader in = null;
      FileWriter out = null;

      try {
         in = new FileReader("input.txt");
         out = new FileWriter("output.txt");
         
         int c; // Each char is read in as an int code
         while ((c = in.read()) != -1) {
            out.write(c);
         }
      } finally {
         // Close input and output streams
         if (in != null) {
            in.close();
         }
         if (out != null) {
            out.close();
         }
      }
   }
}
```

## Buffered Readers and Writers

Java documentation:
- [BufferedReader](https://docs.oracle.com/javase/8/docs/api/java/io/BufferedReader.html)
- [BufferedWriter](https://docs.oracle.com/javase/8/docs/api/java/io/BufferedWriter.html)

Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines.
The buffer size may be specified, or the default size may be used. The default is large enough for most purposes.

In general, each read request made of a Reader causes a corresponding read request to be made of the underlying character or byte stream. It is therefore advisable to wrap a BufferedReader around any Reader whose read() operations may be costly, such as FileReaders and InputStreamReaders. For example:



```java
import java.io.*;
public class CopyFile {

   public static void main(String args[]) throws IOException {
      BufferedReader in = null;
      BufferedWriter out = null;

      try {
         in = new BufferedReader(new FileReader("input.txt"));
         out = new BufferedWriter(new FileWriter("output.txt"));
         
         String line;
         while ((line = in.readLine()) != null) {
            out.write(line);
            out.newLine(); // Writes a carriage return
         }
      } finally {
         // Close input and output streams
         if (in != null) {
            in.close();
         }
         if (out != null) {
            out.close();
         }
      }
   }
}
```
