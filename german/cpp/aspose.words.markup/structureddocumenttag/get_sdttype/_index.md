---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_SdtType Methode"
linktitle: "get_SdtType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_SdtType Methode. Gibt den Typ dieses strukturierten Dokument-Tags in C++ zurück."
type: docs
weight: 28000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_sdttype/
---
## StructuredDocumentTag::get_SdtType method


Liest den Typ dieses **Structured document tag**.

```cpp
Aspose::Words::Markup::SdtType Aspose::Words::Markup::StructuredDocumentTag::get_SdtType() override
```


## Beispiele



Zeigt, wie man den Typ eines strukturierten Dokument-Tags ermittelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSection, tags->idx_get(0)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSectionItem, tags->idx_get(1)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RichText, tags->idx_get(2)->get_SdtType());
```

## Siehe auch

* Enum [SdtType](../../sdttype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
