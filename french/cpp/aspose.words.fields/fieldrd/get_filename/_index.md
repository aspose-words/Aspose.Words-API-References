---
title: "Méthode Aspose::Words::Fields::FieldRD::get_FileName"
linktitle: "get_FileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldRD::get_FileName. Obtient ou définit le nom du fichier à inclure lors de la génération d’une table des matières, d’une table des autorités ou d’un index en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


Obtient ou définit le nom du fichier à inclure lors de la génération d'une table des matières, d'une table des autorités ou d'un index.

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## Exemples



Montre comment utiliser le champ RD pour créer des entrées de table des matières à partir des titres d'autres documents.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un constructeur de document pour insérer une table des matières,
// et ajoutez ensuite une entrée pour la table des matières à la page suivante.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Insérez un champ RD, qui fait référence à un autre document du système de fichiers local dans sa propriété FileName.
// La table des matières acceptera désormais également tous les titres du document référencé comme entrées pour sa table.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Créez le document auquel le champ RD fait référence et insérez un titre.
// Ce titre apparaîtra comme une entrée dans le champ TOC de notre premier document.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Voir aussi

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
