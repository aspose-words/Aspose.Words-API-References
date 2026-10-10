---
title: "Aspose::Words::Fields::FieldComments::get_Text méthode"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldComments::get_Text méthode. Obtient ou définit le texte des commentaires en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Obtient ou définit le texte des commentaires.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Exemples



Montre comment utiliser le champ COMMENTS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez une valeur pour la propriété intégrée "Comments" du document.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Créez un champ COMMENTS pour afficher la valeur de cette propriété intégrée.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Si nous attribuons une valeur à la propriété Text du champ COMMENTS et le mettons à jour, le champ
// écrasera la valeur actuelle de la propriété intégrée "Comments" avec la valeur de sa propriété Text,
// et affichera ensuite la nouvelle valeur.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Voir aussi

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
