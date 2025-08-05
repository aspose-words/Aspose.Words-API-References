---
title: Aspose::Words::Replacing::ReplacingArgs class
linktitle: ReplacingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::ReplacingArgs class. Provides data for a custom replace operation. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Provides data for a custom replace operation. To learn more, visit the [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) documentation article.

```cpp
class ReplacingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifies, by index, a captured group in the [Match](./get_match/) that is to be replaced with the [Replacement](./get_replacement/) string. |
| [get_GroupName](./get_groupname/)() const | Identifies, by name, a captured group in the [Match](./get_match/) that is to be replaced with the [Replacement](./get_replacement/) string. |
| [get_Match](./get_match/)() const | The **Match** resulting from a single regular expression match during a **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Gets the node that contains the end of the match. |
| [get_MatchNode](./get_matchnode/)() const | Gets the node that contains the beginning of the match. |
| [get_MatchOffset](./get_matchoffset/)() const | Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match. |
| [get_Replacement](./get_replacement/)() const | Gets the replacement string. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Setter for [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Setter for [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Sets the replacement string. |
| static [Type](./type/)() |  |

## See Also

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
