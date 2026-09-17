---
title: "Aspose::Words::Fields::FieldKeywords::get_Text method"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldKeywords::get_Text method. Obtient ou définit le texte des mots-clés en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Obtient ou définit le texte des mots‑clés.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Exemples



Montre comment insérer un champ KEYWORDS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez quelques mots‑clés, également appelés « tags » dans l'Explorateur de fichiers.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// Le champ KEYWORDS affiche la valeur de cette propriété.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Définir une valeur pour la propriété Text du champ,
// et la mise à jour du champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Voir aussi

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
