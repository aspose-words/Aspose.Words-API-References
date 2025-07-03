---
title: Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer method
linktitle: get_UseGdiEmfRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer method. Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Remarks


If set to **true** GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to **false** Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is **true**.

## Examples



Shows how to choose a renderer when converting a document to .emf. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
// If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
// If we set the "UseGdiEmfRenderer" flag to "false", Aspose.Words will use its own metafile renderer.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
