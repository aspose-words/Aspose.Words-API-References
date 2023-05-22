---
title: Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf method
linktitle: get_SaveImagesAsWmf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf method. When true all images will be saved as WMF in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


When **true** all images will be saved as WMF.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Examples



Shows how to convert all images in a document to the Windows Metafile format as we save the document as an RTF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
SharedPtr<Shape> imageShape = builder->InsertImage(ImageDir + u"Logo.jpg");

ASSERT_EQ(ImageType::Jpeg, imageShape->get_ImageData()->get_ImageType());

builder->InsertParagraph();
builder->Writeln(u"Png image:");
imageShape = builder->InsertImage(ImageDir + u"Transparent background logo.png");

ASSERT_EQ(ImageType::Png, imageShape->get_ImageData()->get_ImageType());

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
auto rtfSaveOptions = MakeObject<RtfSaveOptions>();

// Set the "SaveImagesAsWmf" property to "true" to convert all images in the document to WMF as we save it to RTF.
// Doing so will help readers such as WordPad to read our document.
// Set the "SaveImagesAsWmf" property to "false" to preserve the original format of all images in the document
// as we save it to RTF. This will preserve the quality of the images at the cost of compatibility with older RTF readers.
rtfSaveOptions->set_SaveImagesAsWmf(saveImagesAsWmf);

doc->Save(ArtifactsDir + u"RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = MakeObject<Document>(ArtifactsDir + u"RtfSaveOptions.SaveImagesAsWmf.rtf");

SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

if (saveImagesAsWmf)
{
    ASSERT_EQ(ImageType::Wmf, (System::ExplicitCast<Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(ImageType::Wmf, (System::ExplicitCast<Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(ImageType::Jpeg, (System::ExplicitCast<Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(ImageType::Png, (System::ExplicitCast<Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
```

## See Also

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
