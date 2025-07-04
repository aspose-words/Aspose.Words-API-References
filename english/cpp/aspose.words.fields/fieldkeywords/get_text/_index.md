---
title: Aspose::Words::Fields::FieldKeywords::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldKeywords::get_Text method. Gets or sets the text of the keywords in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Gets or sets the text of the keywords.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Examples



Shows to insert a KEYWORDS field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add some keywords, also referred to as "tags" in File Explorer.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// The KEYWORDS field displays the value of this property.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Setting a value for the field's Text property,
// and then updating the field will also overwrite the corresponding built-in property with the new value.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## See Also

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
