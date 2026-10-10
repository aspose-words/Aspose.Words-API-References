---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SdtAppearance enum. Specificerar utseendet för en strukturerad dokumenttagg i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Anger utseendet på en strukturerad dokumenttagg.

```cpp
enum class SdtAppearance
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| BoundingBox | 0 | Representerar en strukturerad dokumenttagg som visas som en skuggad rektangel eller en avgränsningsruta. |
| Taggar | 1 | Representerar en strukturerad dokumenttagg som visas som start- och slutmarkörer. |
| Hidden | 2 | Representerar en strukturerad dokumenttagg som inte visas. |
| Default | n/a | Standardvärdet är [BoundingBox](./). |


## Exempel



Visar hur man visar en tagg runt innehållet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
