---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the text to retrieve.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote.get_Text method


Gets or sets the text to retrieve.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Examples




Shows to use the QUOTE field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a QUOTE field, which will display the value of its Text property.
auto field = System::DynamicCast<FieldQuote>(builder->InsertField(FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Insert a QUOTE field and nest a DATE field inside it.
// DATE fields update their value to the current date every time we open the document using Microsoft Word.
// Nesting the DATE field inside the QUOTE field like this will freeze its value
// to the date when we created the document.
builder->Write(u"\nDocument creation date: ");
field = System::DynamicCast<FieldQuote>(builder->InsertField(FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(FieldType::FieldDate, true);

ASSERT_EQ(String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Update all the fields to display their correct results.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(ArtifactsDir + u"Field.QUOTE.docx");
```

