---
title: Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions constructor
linktitle: FindReplaceOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions constructor. Initializes a new instance of the FindReplaceOptions class with default settings in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Initializes a new instance of the [FindReplaceOptions](../) class with default settings.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## Examples



Shows how to recognize and use substitutions within replacement patterns. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Using legacy mode does not support many advanced features, so we need to set it to 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Initializes a new instance of the [FindReplaceOptions](../) class with the specified direction.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Parameter | Type | Description |
| --- | --- | --- |
| direction | Aspose::Words::Replacing::FindReplaceDirection | The direction of the find and replace operation. |

## See Also

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initializes a new instance of the [FindReplaceOptions](../) class with the specified direction and replacing callback.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parameter | Type | Description |
| --- | --- | --- |
| direction | Aspose::Words::Replacing::FindReplaceDirection | The direction of the find and replace operation. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | The callback to use for replacing found text. |

## See Also

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initializes a new instance of the [FindReplaceOptions](../) class with the specified replacing callback.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parameter | Type | Description |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | The callback to use for replacing found text. |

## See Also

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
