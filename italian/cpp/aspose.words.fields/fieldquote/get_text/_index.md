---
title: "Metodo Aspose::Words::Fields::FieldQuote::get_Text"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldQuote::get_Text. Ottiene o imposta il testo da recuperare in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Ottiene o imposta il testo da recuperare.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Esempi



Mostra come usare il campo QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un campo QUOTE, che visualizzerà il valore della sua proprietà Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Inserisci un campo QUOTE e annida un campo DATE al suo interno.
// I campi DATE aggiornano il loro valore alla data corrente ogni volta che apriamo il documento con Microsoft Word.
// Annidare il campo DATE all'interno del campo QUOTE in questo modo bloccherà il suo valore
// alla data in cui abbiamo creato il documento.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Aggiorna tutti i campi per visualizzare i risultati corretti.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Vedi anche

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
