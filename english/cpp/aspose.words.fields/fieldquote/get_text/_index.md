---
title: Aspose::Words::Fields::FieldQuote::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldQuote::get_Text method. Gets or sets the text to retrieve in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Gets or sets the text to retrieve.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Examples



Shows to use the QUOTE field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a QUOTE field, which will display the value of its Text property.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Insert a QUOTE field and nest a DATE field inside it.
// DATE fields update their value to the current date every time we open the document using Microsoft Word.
// Nesting the DATE field inside the QUOTE field like this will freeze its value
// to the date when we created the document.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Update all the fields to display their correct results.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## See Also

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
