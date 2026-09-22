---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 metodu"
linktitle: "get_ExportImagesAsBase64"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 metodu. Görüntülerin çıktı dosyasına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


Görüntülerin çıktı dosyasına Base64 formatında kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## Açıklamalar


Bu özellik **true** olarak ayarlandığında görüntü verileri doğrudan **img** öğelerine aktarılır ve ayrı dosyalar oluşturulmaz.

## Örnekler



.md belgesini içinde gömülü görüntülerle nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## Ayrıca Bakınız

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
