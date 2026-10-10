---
title: "Méthode Aspose::Words::Fields::FieldTitle::get_Text"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldTitle::get_Text. Obtient ou définit le texte du titre en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Obtient ou définit le texte du titre.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Exemples



Montre comment utiliser le champ TITLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Définissez une valeur pour la propriété de document intégrée "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Nous pouvons utiliser le champ TITLE pour afficher la valeur de cette propriété dans le document.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Définir une valeur pour la propriété Text du champ,
// et la mise à jour du champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## Voir aussi

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
