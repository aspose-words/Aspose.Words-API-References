---
title: "Méthode Aspose::Words::Fields::FieldInfo::get_InfoType"
linktitle: "get_InfoType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldInfo::get_InfoType. Obtient ou définit le type de la propriété du document à insérer en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Obtient ou définit le type de la propriété du document à insérer.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Exemples



Montre comment travailler avec les champs INFO.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez une valeur pour la propriété intégrée "Comments" puis insérez un champ INFO pour afficher la valeur de cette propriété.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Définir une valeur pour la propriété NewValue du champ et mettre à jour
// le champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Voir aussi

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
