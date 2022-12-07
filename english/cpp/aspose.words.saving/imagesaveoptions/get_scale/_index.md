---
title: get_Scale
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the zoom factor for the generated images.
type: docs
weight: 170
url: /cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Gets or sets the zoom factor for the generated images.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Examples



Shows how to edit the image while Aspose.Words converts a document to one. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Png);
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
options->set_Scale(96.f / 72.f);

doc->Save(ArtifactsDir + u"ImageSaveOptions.EditImage.png", options);
```


Shows how to render an Office [Math](../../../aspose.words.math/) object into an image file in the local file system. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto math = System::DynamicCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
auto saveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(ArtifactsDir + u"Shape.RenderOfficeMath.png", saveOptions);
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
