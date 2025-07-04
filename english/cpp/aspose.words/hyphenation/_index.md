---
title: Aspose::Words::Hyphenation class
linktitle: Hyphenation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Hyphenation class. Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated. To learn more, visit the  documentation article in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words/hyphenation/
---
## Hyphenation class


Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated. To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) documentation article.

```cpp
class Hyphenation
```

## Methods

| Method | Description |
| --- | --- |
| static [get_Callback](./get_callback/)() | Gets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| static [get_WarningCallback](./get_warningcallback/)() | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Returns **false** if for the specified language there is no dictionary registered or if registered is Null dictionary, **true** otherwise. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. This method can also be used to register Null dictionary to prevent [Callback](./get_callback/) from being called repeatedly for the same language. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Unregisters a hyphenation dictionary for the specified language. This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language. |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
