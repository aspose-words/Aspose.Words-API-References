---
title: get_NameOfApplication
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the application.
type: docs
weight: 261
url: /cpp/aspose.words.properties/builtindocumentproperties/get_nameofapplication/
---
## BuiltInDocumentProperties::get_NameOfApplication method


Gets or sets the name of the application.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication()
```


## Examples



Shows how to work with document properties in the "Origin" category. 
```cpp
// Open a document that we have created and edited using Microsoft Word.
auto doc = MakeObject<Document>(MyDir + u"Properties.docx");
SharedPtr<BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// The following built-in properties contain information regarding the creation and editing of this document.
// We can right-click this document in Windows Explorer and find
// these properties via "Properties" -> "Details" -> "Origin" category.
// Fields such as PRINTDATE and EDITTIME can display these values in the document body.
std::cout << "Created using " << properties->get_NameOfApplication() << ", on " << properties->get_CreatedTime() << std::endl;
std::cout << "Minutes spent editing: " << properties->get_TotalEditingTime() << std::endl;
std::cout << "Date/time last printed: " << properties->get_LastPrinted() << std::endl;
std::cout << "Template document: " << properties->get_Template() << std::endl;

// We can also change the values of built-in properties.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
properties->set_RevisionNumber(properties->get_RevisionNumber() + 1);

// Microsoft Word updates the following properties automatically when we save the document.
// To use these properties with Aspose.Words, we will need to set values for them manually.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc->Save(ArtifactsDir + u"DocumentProperties.Origin.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words](../../../)
