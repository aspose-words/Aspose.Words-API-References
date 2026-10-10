---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 metodu"
linktitle: "get_ExportFontsAsBase64"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 metodu. Yazı tipleri kaynaklarının HTML'e Base64 kodlamasıyla gömülüp gömülmeyeceğini belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Yazı tipi kaynaklarının Base64 kodlamasıyla HTML'ye gömülüp gömülmeyeceğini belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Açıklamalar


Varsayılan olarak, yazı tipleri ayrı dosyalara yazılır. Bu seçenek **true** olarak ayarlanırsa, yazı tipleri Base64 kodlamasıyla belgenin CSS'ine gömülür.

## Örnekler



.html belgesini içinde gömülü görüntülerle nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Kaydedilmiş bir HTML belgesine yazı tiplerini nasıl gömeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
