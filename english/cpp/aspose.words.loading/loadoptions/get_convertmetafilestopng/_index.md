---
title: get_ConvertMetafilesToPng
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to convert metafile (Wmf or Emf) images to Png image format.
type: docs
weight: 27
url: /cpp/aspose.words.loading/loadoptions/get_convertmetafilestopng/
---
## LoadOptions.get_ConvertMetafilesToPng method


Gets or sets whether to convert metafile (**Wmf** or **Emf**) images to **Png** image format.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng() const
```


## Examples




Shows how to convert WMF/EMF to PNG during loading document. 
```cpp
auto doc = MakeObject<Document>();

auto shape = MakeObject<Shape>(doc, ShapeType::Image);
shape->get_ImageData()->SetImage(ImageDir + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(shape);

doc->Save(ArtifactsDir + u"Image.CreateImageDirectly.docx");

shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

TestUtil::VerifyImageInShape(1600, 1600, ImageType::Wmf, shape);

auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_ConvertMetafilesToPng(true);

doc = MakeObject<Document>(ArtifactsDir + u"Image.CreateImageDirectly.docx", loadOptions);
shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
```

