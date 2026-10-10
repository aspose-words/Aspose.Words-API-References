---
title: "Aspose::Words::Replacing::ReplacingArgs class"
linktitle: "ReplacingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::ReplacingArgs class. Tillhandahåller data för en anpassad ersättningsoperation. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Tillhandahåller data för en anpassad ersättningsoperation. För att lära dig mer, besök artikeln [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) documentation article.

```cpp
class ReplacingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifierar, efter index, en fångad grupp i [Match](./get_match/) som ska ersättas med [Replacement](./get_replacement/)-strängen. |
| [get_GroupName](./get_groupname/)() const | Identifierar, efter namn, en fångad grupp i [Match](./get_match/) som ska ersättas med [Replacement](./get_replacement/)-strängen. |
| [get_Match](./get_match/)() const | Den **Match** som resultat av en enskild reguljär uttrycks‑matchning under en **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Hämtar noden som innehåller slutet av matchen. |
| [get_MatchNode](./get_matchnode/)() const | Hämtar noden som innehåller början av matchen. |
| [get_MatchOffset](./get_matchoffset/)() const | Hämtar den nollbaserade startpositionen för matchen från början av noden som innehåller matchens början. |
| [get_Replacement](./get_replacement/)() const | Hämtar ersättningssträngen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Sättare för [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Sättare för [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Ställer in ersättningssträngen. |
| static [Type](./type/)() |  |

## Se även

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
