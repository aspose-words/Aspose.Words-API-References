---
title: "Aspose::Words::Fields::FieldKeywords::get_Text method"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldKeywords::get_Text method. Ottiene o imposta il testo delle parole chiave in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Ottiene o imposta il testo delle parole chiave.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Esempi



Mostra come inserire un campo KEYWORDS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi alcune parole chiave, note anche come \"tag\" in Esplora File.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// Il campo KEYWORDS visualizza il valore di questa proprietà.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Impostare un valore per la proprietà Text del campo,
// e quindi aggiornare il campo sovrascriverà anche la proprietà incorporata corrispondente con il nuovo valore.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Vedi anche

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
