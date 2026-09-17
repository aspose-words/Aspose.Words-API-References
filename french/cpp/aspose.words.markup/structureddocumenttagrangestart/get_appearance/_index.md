---
title: "Méthode Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance"
linktitle: "get_Appearance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance. Obtient ou définit l'apparence du tag de document structuré en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_appearance/
---
## StructuredDocumentTagRangeStart::get_Appearance method


Obtient ou définit l'apparence de la balise de document structuré.

```cpp
Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance() override
```


## Exemples



Montre comment afficher la balise autour du contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Voir aussi

* Enum [SdtAppearance](../../sdtappearance/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
