---
title: IHyphenationCallback
linktitle: IHyphenationCallback
second_title: Aspose.Words for Java API Reference
description: Implemented by classes which can register hyphenation dictionaries in Java.
type: docs
weight: 654
url: /java/com.aspose.words/ihyphenationcallback/
---
```
public interface IHyphenationCallback
```

Implemented by classes which can register hyphenation dictionaries.
## Methods

| Method | Description |
| --- | --- |
| [requestDictionary(String language)](#requestDictionary-java.lang.String) | Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered. |
### requestDictionary(String language) {#requestDictionary-java.lang.String}
```
public abstract void requestDictionary(String language)
```


Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered.

Implementation should find a dictionary and register it using **M:Aspose.Words.Hyphenation.RegisterDictionary(System.String,System.IO.Stream)** methods.

If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language using [Hyphenation.registerDictionary(java.lang.String, java.lang.String)](../../com.aspose.words/hyphenation/\#registerDictionary-java.lang.String--java.lang.String) with  null  value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | java.lang.String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. Exceptions thrown by this method will abort execution of page layout process. |

