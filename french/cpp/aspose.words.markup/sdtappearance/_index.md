---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::SdtAppearance enum. Spécifie l'apparence d'une balise de document structuré en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Spécifie l'apparence d'une balise de document structuré.

```cpp
enum class SdtAppearance
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| BoundingBox | 0 | Représente une balise de document structuré affichée sous forme de rectangle ombré ou de boîte englobante. |
| Tags | 1 | Représente une balise de document structuré affichée comme marqueurs de début et de fin. |
| Masqué | 2 | Représente une balise de document structuré qui n'est pas affichée. |
| Default | n/a | Par défaut, [BoundingBox](./). |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
