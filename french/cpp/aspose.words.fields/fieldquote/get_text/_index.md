---
title: "Méthode Aspose::Words::Fields::FieldQuote::get_Text"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldQuote::get_Text. Obtient ou définit le texte à récupérer en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Obtient ou définit le texte à récupérer.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Exemples



Montre comment utiliser le champ QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un champ QUOTE, qui affichera la valeur de sa propriété Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Insérez un champ QUOTE et imbriquez-y un champ DATE.
// Les champs DATE mettent à jour leur valeur à la date actuelle chaque fois que nous ouvrons le document avec Microsoft Word.
// Imbriquer le champ DATE à l'intérieur du champ QUOTE de cette manière figera sa valeur
// à la date à laquelle nous avons créé le document.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Mettez à jour tous les champs pour afficher leurs résultats corrects.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Voir aussi

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
