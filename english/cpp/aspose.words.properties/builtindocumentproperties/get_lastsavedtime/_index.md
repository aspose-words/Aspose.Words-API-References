---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime method
linktitle: get_LastSavedTime
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime method. Gets or sets the time of the last save in UTC in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Gets or sets the time of the last save in UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Remarks


For documents originated from RTF format this property returns the local time of last save operation.

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


Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// We can use the SAVEDATE field to display the last save operation's date and time on the document.
// The save operation that these fields refer to is the manual save in an application like Microsoft Word,
// not the document's Save method.
// Below are three different calendar types according to which the SAVEDATE field can display the date/time.
// 1 -  Islamic Lunar Calendar:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura calendar:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Indian National calendar:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
// The document's Save method will not update this value, but we can still update it manually.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
