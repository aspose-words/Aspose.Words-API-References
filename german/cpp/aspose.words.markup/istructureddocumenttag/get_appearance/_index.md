---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance-Methode"
linktitle: "get_Appearance"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance-Methode. Ruft das Aussehen des strukturierten Dokument-Tags ab oder legt es fest in C++."
type: docs
weight: 1500
url: /de/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


Liest oder setzt das Erscheinungsbild des strukturierten Dokument-Tags.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
```


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

* Enum [SdtAppearance](../../sdtappearance/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
