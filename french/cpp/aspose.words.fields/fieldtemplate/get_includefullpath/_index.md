---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath méthode"
linktitle: "get_IncludeFullPath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath méthode. Obtient ou définit si le nom complet du chemin de fichier doit être inclus en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Obtient ou définit si le nom complet du chemin du fichier doit être inclus.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
