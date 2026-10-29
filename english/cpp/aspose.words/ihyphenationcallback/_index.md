---
title: Aspose::Words::IHyphenationCallback interface
linktitle: IHyphenationCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IHyphenationCallback interface. Implemented by classes which can register hyphenation dictionaries in C++.'
type: docs
weight: 78000
url: /cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Implemented by classes which can register hyphenation dictionaries.

```cpp
class IHyphenationCallback : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered.

 Implementation should find a dictionary and register it using [RegisterDictionary()](../hyphenation/registerdictionary/) methods.

 If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language using [RegisterDictionary()](../hyphenation/registerdictionary/) with **null** value. |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
