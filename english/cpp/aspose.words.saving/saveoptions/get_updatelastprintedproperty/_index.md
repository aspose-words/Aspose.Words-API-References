---
title: get_UpdateLastPrintedProperty
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether the LastPrinted property is updated before saving.
type: docs
weight: 196
url: /cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Gets or sets a value determining whether the [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Examples



Shows how to update a document's "Last printed" property when saving. 
```cpp
auto doc = MakeObject<Document>();
doc->get_BuiltInDocumentProperties()->set_LastPrinted(System::DateTime(2019, 12, 20));

// This flag determines whether the last printed date, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the print date.
auto saveOptions = MakeObject<DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
// It can also be displayed in the document's body by using a PRINTDATE field.
doc->Save(ArtifactsDir + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Open the saved document, then verify the value of the property.
doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

ASPOSE_ASSERT_NE(isUpdateLastPrintedProperty, System::DateTime(2019, 12, 20) == doc->get_BuiltInDocumentProperties()->get_LastPrinted());
```


Shows how to update a document's "CreatedTime" property when saving. 
```cpp
auto doc = MakeObject<Document>();
doc->get_BuiltInDocumentProperties()->set_CreatedTime(System::DateTime(2019, 12, 20));

// This flag determines whether the created time, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the created time.
auto saveOptions = MakeObject<DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(ArtifactsDir + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Open the saved document, then verify the value of the property.
doc = MakeObject<Document>(ArtifactsDir + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

ASPOSE_ASSERT_NE(isUpdateCreatedTimeProperty, System::DateTime(2019, 12, 20) == doc->get_BuiltInDocumentProperties()->get_CreatedTime());
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
