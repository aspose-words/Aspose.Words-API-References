---
title: "Aspose::Words::Fields::FormFieldCollection::idx_get metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormFieldCollection::idx_get metod. Returnerar ett formulärfält efter bokmärkesnamn i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/formfieldcollection/idx_get/
---
## FormFieldCollection::idx_get(const System::String\&) method


Returnerar ett formulärfält efter bokmärkesnamn.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(const System::String &bookmarkName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Skiftlägesokänsligt bokmärkesnamn. |

## Se även

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FormFieldCollection::idx_get(int32_t) method


Returnerar ett formulärfält på det angivna indexet.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Ett index i samlingen. |
## Anmärkningar


Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst sista och så vidare.

Om index är större än eller lika med antalet objekt i listan, returneras en null-referens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returneras en null-referens.

## Se även

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
