---
title: "Méthode SetUncheckedSymbol de Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "SetUncheckedSymbol"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode SetUncheckedSymbol de Aspose::Words::Markup::StructuredDocumentTag. Définit le symbole utilisé pour représenter l'état non coché d'un contrôle de contenu case à cocher en C++."
type: docs
weight: 59000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


Définit le symbole utilisé pour représenter l'état décoché d'un contrôle de contenu case à cocher.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| characterCode | int32_t | Le code de caractère pour le symbole spécifié. |
| fontName | const System::String\& | Le nom de la police qui contient le symbole. |
## Remarques


L'accès à cette méthode ne fonctionnera que pour les types SDT [Checkbox](../../sdttype/).

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
