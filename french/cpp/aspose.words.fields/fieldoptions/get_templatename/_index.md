---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName méthode"
linktitle: "get_TemplateName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName méthode. Obtient ou définit le nom de fichier du modèle utilisé par le document en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Obtient ou définit le nom de fichier du modèle utilisé par le document.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Remarques


Cette propriété est utilisée par le champ [FieldTemplate](../../fieldtemplate/) si la propriété [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) est vide.

Si cette propriété est vide, le nom de fichier du modèle par défaut **Normal.dotm** est utilisé.

## Exemples



Montre comment utiliser un champ TEMPLATE pour afficher l'emplacement du système de fichiers local du modèle d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nous pouvons définir un nom de modèle à l'aide des champs. Cette propriété est utilisée lorsque \"doc.AttachedTemplate\" est vide.
// Si cette propriété est vide, le nom de fichier de modèle par défaut \"Normal.dotm\" est utilisé.
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
