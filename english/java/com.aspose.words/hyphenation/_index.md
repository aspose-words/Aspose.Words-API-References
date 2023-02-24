---
title: Hyphenation
linktitle: Hyphenation
second_title: Aspose.Words for Java API Reference
description: Provides methods for working with hyphenation dictionaries in Java.
type: docs
weight: 335
url: /java/com.aspose.words/hyphenation/
---

**Inheritance:**
java.lang.Object
```
public class Hyphenation
```

Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated.

To learn more, visit the [ Working with Hyphenation ][Working with Hyphenation] documentation article.


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getCallback()](#getCallback) | Gets callback interface used to request dictionaries when page layout of the document is built. |
| [getClass()](#getClass) |  |
| [getWarningCallback()](#getWarningCallback) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| [hashCode()](#hashCode) |  |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String) | Returns  false  if for the specified language there is no dictionary registered or if registered is Null dictionary,  true  otherwise. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String) | Registers and loads a hyphenation dictionary for the specified language from file. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback) | Sets callback interface used to request dictionaries when page layout of the document is built. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| [toString()](#toString) |  |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String) | Unregisters a hyphenation dictionary for the specified language. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getCallback() {#getCallback}
```
public static IHyphenationCallback getCallback()
```


Gets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages.

**Returns:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) - Callback interface used to request dictionaries when page layout of the document is built.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getWarningCallback() {#getWarningCallback}
```
public static IWarningCallback getWarningCallback()
```


Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String}
```
public static boolean isDictionaryRegistered(String language)
```


Returns  false  if for the specified language there is no dictionary registered or if registered is Null dictionary,  true  otherwise.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String |  |

**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream}
```
public static void registerDictionary(String language, InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String}
```
public static void registerDictionary(String language, String fileName)
```


Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format.

This method can also be used to register Null dictionary to prevent [getCallback()](../../com.aspose.words/hyphenation/\#getCallback) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation/\#setCallback-com.aspose.words.IHyphenationCallback) from being called repeatedly for the same language.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| fileName | java.lang.String | A path to the dictionary file in Open Office format.

If this parameter is  null  or empty string then registered is Null dictionary and callback is not called anymore for this language.

To enable callback again use [unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation/\#unregisterDictionary-java.lang.String) method. |

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback}
```
public static void setCallback(IHyphenationCallback value)
```


Sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) | Callback interface used to request dictionaries when page layout of the document is built. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public static void setWarningCallback(IWarningCallback value)
```


Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String}
```
public static void unregisterDictionary(String language)
```


Unregisters a hyphenation dictionary for the specified language.

This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details.

If  null  or empty string then all dictionaries are unregistered. |

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

