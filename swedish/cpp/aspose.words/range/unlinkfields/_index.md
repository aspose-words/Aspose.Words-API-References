---
title: "Aspose::Words::Range::UnlinkFields‑metod"
linktitle: "UnlinkFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::UnlinkFields‑metod. Kopplar bort fält i detta område i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Kopplar bort fält i detta område.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Anmärkningar


Ersätter alla fält i detta område med deras senaste resultat.

För att koppla bort fält i hela dokumentet, använd [UnlinkFields](./).

## Exempel



Visar hur man kopplar bort alla fält i ett område.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Se även

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
