---
title: "Méthode Aspose::Words::Markup::StructuredDocumentTag::get_Checked"
linktitle: "get_Checked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::StructuredDocumentTag::get_Checked. Obtient/Définit l'état actuel du SDT Checkbox. La valeur par défaut de cette propriété est false en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Obtient/Définit l'état actuel de la case à cocher **SDT**. La valeur par défaut de cette propriété est **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Remarques


L'accès à cette propriété ne fonctionnera que pour les types de SDT [Checkbox](../../sdttype/).

Pour tous les autres types de SDT, une exception se produira.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
