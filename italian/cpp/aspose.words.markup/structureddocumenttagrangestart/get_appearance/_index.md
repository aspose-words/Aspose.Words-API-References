---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance metodo"
linktitle: "get_Appearance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance metodo. Ottiene o imposta l'aspetto del tag di documento strutturato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangestart/get_appearance/
---
## StructuredDocumentTagRangeStart::get_Appearance method


Ottiene o imposta l'aspetto del tag di documento strutturato.

```cpp
Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance() override
```


## Esempi



Mostra come visualizzare il tag attorno al contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Vedi anche

* Enum [SdtAppearance](../../sdtappearance/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
