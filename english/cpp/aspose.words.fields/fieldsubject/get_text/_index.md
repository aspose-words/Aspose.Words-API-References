---
title: Aspose::Words::Fields::FieldSubject::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSubject::get_Text method. Gets or sets the text of the subject in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Gets or sets the text of the subject.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Examples



Shows how to use the SUBJECT field. 
```cpp
auto doc = MakeObject<Document>();

// Set a value for the document's "Subject" built-in property.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Create a SUBJECT field to display the value of that built-in property.
auto builder = MakeObject<DocumentBuilder>(doc);
auto field = System::ExplicitCast<FieldSubject>(builder->InsertField(FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// If we give the SUBJECT field's Text property value and update it, the field will
// overwrite the current value of the "Subject" built-in property with the value of its Text property,
// and then display the new value.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(ArtifactsDir + u"Field.SUBJECT.docx");
```

## See Also

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
