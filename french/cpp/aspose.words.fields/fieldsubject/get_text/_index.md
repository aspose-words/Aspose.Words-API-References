---
title: "Aspose::Words::Fields::FieldSubject::get_Text method"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldSubject::get_Text method. Obtient ou définit le texte du sujet en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Obtient ou définit le texte du sujet.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Exemples



Montre comment utiliser le champ SUBJECT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Définissez une valeur pour la propriété intégrée « Subject » du document.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Créez un champ SUBJECT pour afficher la valeur de cette propriété intégrée.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Si nous donnons la valeur de la propriété Text du champ SUBJECT et le mettons à jour, le champ sera
// écraser la valeur actuelle de la propriété intégrée "Subject" avec la valeur de sa propriété Text,
// et affichera ensuite la nouvelle valeur.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Voir aussi

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
