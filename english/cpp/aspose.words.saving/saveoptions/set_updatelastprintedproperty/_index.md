---
title: Aspose::Words::Saving::SaveOptions::set_UpdateLastPrintedProperty method
linktitle: set_UpdateLastPrintedProperty
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::set_UpdateLastPrintedProperty method. Sets a value determining whether the LastPrinted property is updated before saving in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words.saving/saveoptions/set_updatelastprintedproperty/
---
## SaveOptions::set_UpdateLastPrintedProperty method


Sets a value determining whether the [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving.

```cpp
void Aspose::Words::Saving::SaveOptions::set_UpdateLastPrintedProperty(bool value)
```

## Examples


Shows how to update a document's "Last printed" property when saving.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// This flag determines whether the last printed date, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the print date.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
// It can also be displayed in the document's body by using a PRINTDATE field.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Open the saved document, then verify the value of the property.
doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc"));

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```
## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
