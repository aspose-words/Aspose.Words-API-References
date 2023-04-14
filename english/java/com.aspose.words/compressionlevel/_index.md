---
title: CompressionLevel
linktitle: CompressionLevel
second_title: Aspose.Words for Java API Reference
description: Compression level for OOXML files in Java.
type: docs
weight: 90
url: /java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Compression level for OOXML files.

(DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive.

Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)

 **Examples:** 

Shows how to specify the compression level to use while saving an OOXML document.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
 // Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
 // the default compression that Aspose.Words uses while saving OOXML documents.
 // Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
 // Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
 // the default compression that Microsoft Word uses.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 saveOptions.setCompressionLevel(compressionLevel);

 StopWatch st = new StopWatch();
 st.start();
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
 st.stop();

 File fileInfo = new File(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx");

 System.out.println(MessageFormat.format("Saving operation done using the \"{0}\" compression level:", compressionLevel));
 System.out.println(MessageFormat.format("\tDuration:\t{0}", st.getTime()));
 System.out.println(MessageFormat.format("\tFile Size:\t{0} bytes", fileInfo.length()));
 
```
## Fields

| Field | Description |
| --- | --- |
| [FAST](#FAST) | Fast compression level. |
| [MAXIMUM](#MAXIMUM) | Maximum compression level. |
| [NORMAL](#NORMAL) | Normal compression level. |
| [SUPER_FAST](#SUPER-FAST) | Super Fast compression level. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int compressionLevel)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Fast compression level.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Maximum compression level.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal compression level. Default compression level used by Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Super Fast compression level. Microsoft Word uses this compression level.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int compressionLevel) {#toString-int}
```
public static String toString(int compressionLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

