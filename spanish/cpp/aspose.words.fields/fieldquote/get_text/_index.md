---
title: "Aspose::Words::Fields::FieldQuote::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldQuote::get_Text method. Obtiene o establece el texto a recuperar en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Obtiene o establece el texto a recuperar.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Ejemplos



Muestra cómo usar el campo QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un campo QUOTE, que mostrará el valor de su propiedad Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Inserte un campo QUOTE y anide dentro de él un campo DATE.
// Los campos DATE actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo DATE dentro del campo QUOTE de esta manera congelará su valor
// a la fecha en que creamos el documento.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Actualice todos los campos para que muestren sus resultados correctos.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Ver también

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
