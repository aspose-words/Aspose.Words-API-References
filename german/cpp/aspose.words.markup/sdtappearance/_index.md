---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SdtAppearance enum. Gibt das Aussehen eines strukturierten Dokumenttags in C++ an."
type: docs
weight: 18000
url: /de/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Gibt das Erscheinungsbild eines strukturierten Dokument‑Tags an.

```cpp
enum class SdtAppearance
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| BoundingBox | 0 | Stellt einen strukturierten Dokumenttag dar, der als schattiertes Rechteck oder Begrenzungsrahmen angezeigt wird. |
| Tags | 1 | Stellt einen strukturierten Dokumenttag dar, der als Anfangs‑ und End‑Markierungen angezeigt wird. |
| Hidden | 2 | Stellt einen strukturierten Dokumenttag dar, der nicht angezeigt wird. |
| Default | n/a | Standardmäßig [BoundingBox](./). |


## Beispiele



Zeigt, wie man ein Tag um den Inhalt herum anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
