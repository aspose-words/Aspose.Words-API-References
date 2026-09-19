---
title: "Metodo get_Text di Aspose::Words::Fields::FieldComments"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Text di Aspose::Words::Fields::FieldComments. Ottiene o imposta il testo dei commenti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Ottiene o imposta il testo dei commenti.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Esempi



Mostra come utilizzare il campo COMMENTS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta un valore per la proprietà incorporata "Comments" del documento.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Crea un campo COMMENTS per visualizzare il valore di quella proprietà incorporata.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Se forniamo al campo COMMENTS il valore della proprietà Text e lo aggiorniamo, il campo
// sovrascriverà il valore corrente della proprietà incorporata "Comments" con il valore della sua proprietà Text,
// e poi visualizzerà il nuovo valore.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Vedi anche

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
