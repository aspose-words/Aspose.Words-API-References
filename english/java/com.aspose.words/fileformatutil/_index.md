---
title: FileFormatUtil
second_title: Aspose.Words for Java API Reference
description: Provides utility methods for working with file formats such as detecting file format or converting file extensions to/from file format enums.
type: docs
weight: 266
url: /java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums.

To learn more, visit the **Detect File Format and Check Format Compatibility** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String-) | Converts IANA content type into a load format enumerated value. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String-) | Converts IANA content type into a save format enumerated value. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream-) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String-) | Detects and returns the information about a format of a document. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String-) | Converts a file name extension into a [SaveFormat](../../com.aspose.words/saveformat) value. |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int-) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int-) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int-) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String-}
```
public static int contentTypeToLoadFormat(String contentType)
```


Converts IANA content type into a load format enumerated value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String-}
```
public static int contentTypeToSaveFormat(String contentType)
```


Converts IANA content type into a save format enumerated value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream-}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String-}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Detects and returns the information about a format of a document.  Detects and returns the information about a format of a document stored in a disk file.

Even if this method detects the document format, it does not guarantee that the specified document is valid. This method only detects the document format by reading data that is sufficient for detection. To fully verify that a document is valid you need to load the document into a [Document](../../com.aspose.words/document) object.

This method throws [FileCorruptedException](../../com.aspose.words/filecorruptedexception) when the format is recognized, but the detection cannot complete because of corruption.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file name. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo) object that contains the detected information.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String-}
```
public static int extensionToSaveFormat(String extension)
```


Converts a file name extension into a [SaveFormat](../../com.aspose.words/saveformat) value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| extension | java.lang.String | The file extension. Can be with or without a leading dot. Case-insensitive.

If the extension cannot be recognized, returns [SaveFormat.UNKNOWN](../../com.aspose.words/saveformat\#UNKNOWN). |

**Returns:**
int
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int-}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int-}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int-}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int-}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int-}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

