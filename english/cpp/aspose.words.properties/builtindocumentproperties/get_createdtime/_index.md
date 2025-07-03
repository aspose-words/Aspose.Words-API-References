---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime method
linktitle: get_CreatedTime
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime method. Gets or sets date of the document creation in UTC in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_createdtime/
---
## BuiltInDocumentProperties::get_CreatedTime method


Gets or sets date of the document creation in UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime()
```

## Remarks


For documents originated from RTF format this property returns local time of the author's machine at the moment of document creation.

Aspose.Words does not update this property.

## Examples



Shows how to work with document properties in the "Origin" category. 
```cpp
// Open a document that we have created and edited using Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// The following built-in properties contain information regarding the creation and editing of this document.
// We can right-click this document in Windows Explorer and find
// these properties via "Properties" -> "Details" -> "Origin" category.
// Fields such as PRINTDATE and EDITTIME can display these values in the document body.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// We can also change the values of built-in properties.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word updates the following properties automatically when we save the document.
// To use these properties with Aspose.Words, we will need to set values for them manually.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
