---
title: get_UpdateSdtContent
second_title: Aspose.Words for C++ API Reference
description: Gets or sets value determining whether content of StructuredDocumentTag is updated before saving.
type: docs
weight: 248
url: /cpp/aspose.words.saving/saveoptions/get_updatesdtcontent/
---
## SaveOptions::get_UpdateSdtContent method


Gets or sets value determining whether content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) is updated before saving.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateSdtContent() const
```


## Examples



Shows how to update structured document tags while saving a document to PDF. 
```cpp
auto doc = MakeObject<Document>();

// Insert a drop-down list structured document tag.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::DropDownList, MarkupLevel::Block);
tag->get_ListItems()->Add(MakeObject<SdtListItem>(u"Value 1"));
tag->get_ListItems()->Add(MakeObject<SdtListItem>(u"Value 2"));
tag->get_ListItems()->Add(MakeObject<SdtListItem>(u"Value 3"));

// The drop-down list currently displays "Choose an item" as the default text.
// Set the "SelectedValue" property to one of the list items to get the tag to
// display that list item's value instead of the default text.
tag->get_ListItems()->set_SelectedValue(tag->get_ListItems()->idx_get(1));

doc->get_FirstSection()->get_Body()->AppendChild(tag);

// Create a "PdfSaveOptions" object to pass to the document's "Save" method
// to modify how that method saves the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "UpdateSdtContent" property to "false" not to update the structured document tags
// while saving the document to PDF. They will display their default values as they were at the time of construction.
// Set the "UpdateSdtContent" property to "true" to make sure the tags display updated values in the PDF.
options->set_UpdateSdtContent(updateSdtContent);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
