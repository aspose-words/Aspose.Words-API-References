---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance méthode"
linktitle: "get_Appearance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance méthode. Obtient ou définit l'apparence de la balise de document structuré en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


Obtient ou définit l'apparence de la balise de document structuré.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
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
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
