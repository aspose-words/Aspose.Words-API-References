---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_Category method
linktitle: get_Category
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_Category method. Gets or sets the category of the document in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_category/
---
## BuiltInDocumentProperties::get_Category method


Gets or sets the category of the document.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Category()
```


## Examples



Shows how to work with built-in document properties in the "Description" category. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Below are four built-in document properties that have fields that can display their values in the document body.
// 1 -  "Author" property, which we can display using an AUTHOR field:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(FieldType::FieldAuthor, true);

// 2 -  "Title" property, which we can display using a TITLE field:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(FieldType::FieldTitle, true);

// 3 -  "Subject" property, which we can display using a SUBJECT field:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(FieldType::FieldSubject, true);

// 4 -  "Comments" property, which we can display using a COMMENTS field:
properties->set_Comments(String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(FieldType::FieldComments, true);
builder->Write(u"\"");

// The "Category" built-in property does not have a field that can display its value.
properties->set_Category(u"My category");

// We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
// The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc->Save(ArtifactsDir + u"DocumentProperties.Description.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
