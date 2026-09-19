---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance metodo"
linktitle: "get_Appearance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance metodo. Ottiene o imposta l'aspetto del tag di documento strutturato in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


Ottiene o imposta l'aspetto del tag di documento strutturato.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
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
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
