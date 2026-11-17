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
class IHyphenationCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered. Implementation should find a dictionary and register it using [RegisterDictionary()](../) methods. If dictionary is unavailable for the specified language implementation can opt out of further calls for the same language using [RegisterDictionary()](../) with **null** value. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
