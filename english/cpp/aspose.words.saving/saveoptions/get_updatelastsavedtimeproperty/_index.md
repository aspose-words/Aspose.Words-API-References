---
title: get_UpdateLastSavedTimeProperty
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether the LastSavedTime property is updated before saving.
type: docs
weight: 235
url: /cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Gets or sets a value determining whether the [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Examples



Shows how to determine whether to preserve the document's "Last saved time" property when saving. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "UpdateLastSavedTimeProperty" property to "true" to
// set the output document's "Last saved time" built-in property to the current date/time.
// Set the "UpdateLastSavedTimeProperty" property to "false" to
// preserve the original value of the input document's "Last saved time" built-in property.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(ArtifactsDir + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = MakeObject<Document>(ArtifactsDir + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_GT(System::DateTime::get_Now(), lastSavedTimeNew.AddDays(-1));
    ASSERT_LT(System::DateTime::get_Now(), lastSavedTimeNew.AddDays(1));
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
