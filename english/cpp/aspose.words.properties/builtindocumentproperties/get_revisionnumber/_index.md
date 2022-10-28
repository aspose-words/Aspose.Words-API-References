---
title: get_RevisionNumber
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the document revision number.
type: docs
weight: 287
url: /cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties.get_RevisionNumber method


Gets or sets the document revision number.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```


Aspose.Words does not update this property.

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


Shows how to work with REVNUM fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// Insert a REVNUM field, which displays the document's current revision number property.
auto field = System::DynamicCast<FieldRevNum>(builder->InsertField(FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// This property counts how many times a document has been saved in Microsoft Word,
// and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
// via Properties -> Details. We can update this property manually.
doc->get_BuiltInDocumentProperties()->set_RevisionNumber(doc->get_BuiltInDocumentProperties()->get_RevisionNumber() + 1);
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

