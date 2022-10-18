---
title: Hyphenation
second_title: Aspose.Words for Java API Reference
description: Provides methods for working with hyphenation dictionaries.
type: docs
weight: 333
url: /java/com.aspose.words/hyphenation/
---

**Inheritance:**
java.lang.Object
```
public class Hyphenation
```

Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated.

To learn more, visit the **Working with Hyphenation** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream-) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String-) | Registers and loads a hyphenation dictionary for the specified language from file. |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String-) | Unregisters a hyphenation dictionary for the specified language. |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String-) | Returns False if for the specified language there is no dictionary registered or if registered is Null dictionary, True otherwise. |
| [getCallback()](#getCallback--) | Gets callback interface used to request dictionaries when page layout of the document is built. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback-) | Sets callback interface used to request dictionaries when page layout of the document is built. |
| [getWarningCallback()](#getWarningCallback--) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream-}
```
public static void registerDictionary(String language, InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String-}
```
public static void registerDictionary(String language, String fileName)
```


Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format.

This method can also be used to register Null dictionary to prevent [getCallback()](../../com.aspose.words/hyphenation\#getCallback--) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation\#setCallback-com.aspose.words.IHyphenationCallback-) from being called repeatedly for the same language.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| fileName | java.lang.String | A path to the dictionary file in Open Office format.

If this parameter is null or empty string then registered is Null dictionary and callback is not called anymore for this language.

To enable callback again use [unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation\#unregisterDictionary-java.lang.String-) method. |

### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String-}
```
public static void unregisterDictionary(String language)
```


Unregisters a hyphenation dictionary for the specified language.

This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details.

If null or empty string then all dictionaries are unregistered. |

### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String-}
```
public static boolean isDictionaryRegistered(String language)
```


Returns False if for the specified language there is no dictionary registered or if registered is Null dictionary, True otherwise.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String |  |

**Returns:**
boolean
### getCallback() {#getCallback--}
```
public static IHyphenationCallback getCallback()
```


Gets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages.

**Returns:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) - Callback interface used to request dictionaries when page layout of the document is built.
### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback-}
```
public static void setCallback(IHyphenationCallback value)
```


Sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) | Callback interface used to request dictionaries when page layout of the document is built. |

### getWarningCallback() {#getWarningCallback--}
```
public static IWarningCallback getWarningCallback()
```


Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public static void setWarningCallback(IWarningCallback value)
```


Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

