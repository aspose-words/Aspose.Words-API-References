---
title: Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty method
linktitle: get_UpdateCreatedTimeProperty
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty method. Gets or sets a value determining whether the CreatedTime property is updated before saving. Default value is false; in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Gets or sets a value determining whether the [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Examples



Shows how to update a document's "CreatedTime" property when saving. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// This flag determines whether the created time, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the created time.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Open the saved document, then verify the value of the property.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
