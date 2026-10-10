---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_SdtType méthode"
linktitle: "get_SdtType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_SdtType méthode. Obtient le type de cette balise de document structuré en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_sdttype/
---
## StructuredDocumentTag::get_SdtType method


Obtient le type de cette **Structured document tag**.

```cpp
Aspose::Words::Markup::SdtType Aspose::Words::Markup::StructuredDocumentTag::get_SdtType() override
```


## Exemples



Montre comment obtenir le type d'une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSection, tags->idx_get(0)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSectionItem, tags->idx_get(1)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RichText, tags->idx_get(2)->get_SdtType());
```

## Voir aussi

* Enum [SdtType](../../sdttype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
