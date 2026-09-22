---
title: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing yöntemi"
linktitle: "get_UseAntiAliasing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing yöntemi. C++'da renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Renderleme için anti-aliasing kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Açıklamalar


Varsayılan değer **false**'tur. Bu değer **true** olarak ayarlandığında renderleme için anti-aliasing kullanılır.

Bu özellik, belge aşağıdaki biçimlere dışa aktarıldığında kullanılır: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Belge [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) veya [Mobi](../../../aspose.words/saveformat/) biçimlerine dışa aktarıldığında bu seçenek raster görüntüler için kullanılır.

## Örnekler



Render edilmiş bir belgenin kalitesini [SaveOptions](../) ile nasıl artıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
