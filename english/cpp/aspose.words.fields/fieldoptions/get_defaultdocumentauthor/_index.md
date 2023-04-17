---
title: Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor method
linktitle: get_DefaultDocumentAuthor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor method. Gets or sets default document author''s name. If author''s name is already specified in built-in document properties, this option is not considered in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fields/fieldoptions/get_defaultdocumentauthor/
---
## FieldOptions::get_DefaultDocumentAuthor method


Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor() const
```


## Examples



Shows how to use an AUTHOR field to display a document creator's name. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// AUTHOR fields source their results from the built-in document property called "Author".
// If we create and save a document in Microsoft Word,
// it will have our username in that property.
// However, if we create a document programmatically using Aspose.Words,
// the "Author" property, by default, will be an empty string.
ASSERT_EQ(String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Set a backup author name for AUTHOR fields to use
// if the "Author" property contains an empty string.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::DynamicCast<FieldAuthor>(builder->InsertField(FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Updating an AUTHOR field that contains a value
// will apply that value to the "Author" built-in property.
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Changing this property, then updating the AUTHOR field will apply this value to the field.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// If we update an AUTHOR field after changing its "Name" property,
// then the field will display the new name and apply the new name to the built-in property.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// AUTHOR fields do not affect the DefaultDocumentAuthor property.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(ArtifactsDir + u"Field.AUTHOR.docx");
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
