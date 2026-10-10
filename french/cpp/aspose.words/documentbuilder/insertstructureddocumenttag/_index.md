---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag méthode"
linktitle: "InsertStructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag méthode. Insère un StructuredDocumentTag dans le document en C++."
type: docs
weight: 46500
url: /fr/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Insère un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) dans le document.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Le nœud [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) qui vient d'être inséré.

## Exemples



Montre comment insérer simplement une balise de document structué.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Remarque, seuls les types StructuredDocumentTag suivants sont autorisés pour l'insertion :
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Le niveau de balisage du StructuredDocumentTag inséré sera détecté automatiquement et dépend de la position d'insertion.
// Le StructuredDocumentTag ajouté héritera du formatage du paragraphe et de la police à partir de la position du curseur.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Voir aussi

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
