---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_Author method
linktitle: get_Author
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_Author method. Gets or sets the name of the document''s author in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_author/
---
## BuiltInDocumentProperties::get_Author method


Gets or sets the name of the document's author.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Author()
```


## Examples



Shows how to work with built-in document properties in the "Description" category. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Below are four built-in document properties that have fields that can display their values in the document body.
// 1 -  "Author" property, which we can display using an AUTHOR field:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  "Title" property, which we can display using a TITLE field:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  "Subject" property, which we can display using a SUBJECT field:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  "Comments" property, which we can display using a COMMENTS field:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// The "Category" built-in property does not have a field that can display its value.
properties->set_Category(u"My category");

// We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
// The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
