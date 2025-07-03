---
title: Aspose::Words::IHyphenationCallback::RequestDictionary method
linktitle: RequestDictionary
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IHyphenationCallback::RequestDictionary method. Notifies application that hyphenation dictionary for the specified language wasn''t found and may need to be registered. Implementation should find a dictionary and register it using RegisterDictionary() methods. If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language using RegisterDictionary() with null value in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered. Implementation should find a dictionary and register it using [RegisterDictionary()](../) methods. If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language using [RegisterDictionary()](../) with **null** value.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| language | System::String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |

## See Also

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
