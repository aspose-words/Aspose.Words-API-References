---
title: Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize method
linktitle: get_ExportCompactSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize method. Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is false in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Remarks


If the document that you want to convert to RTF using Aspose.Words does not contain right-to-left text in languages like Arabic, then you can set this option to **true** to reduce the size of the resulting RTF.

## Examples



Shows how to save a document to .rtf with custom options. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Set the "ExportCompactSize" property to "true" to
// reduce the saved document's size at the cost of right-to-left text compatibility.
options->set_ExportCompactSize(true);

// Set the "ExportImagesFotOldReaders" property to "true" to use extra keywords to ensure that our document is
// compatible with pre-Microsoft Word 97 readers and WordPad.
// Set the "ExportImagesFotOldReaders" property to "false" to reduce the size of the document,
// but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## See Also

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
