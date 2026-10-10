---
title: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag constructeur"
linktitle: "StructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag constructeur. Initialise une nouvelle instance de la classe Structured document tag en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Initialise une nouvelle instance de la classe **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
| type | Aspose::Words::Markup::SdtType | Type de nœud SDT. |
| niveau | Aspose::Words::Markup::MarkupLevel | Niveau du nœud SDT dans le document. |
## Remarques


Les types de SDT suivants peuvent être créés :

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



## Exemples



Montrez comment créer une balise de document structuré sous forme de case à cocher.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Nous pouvons définir les symboles utilisés pour représenter l'état coché/décoché d'un contrôle de contenu case à cocher.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Voir aussi

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
