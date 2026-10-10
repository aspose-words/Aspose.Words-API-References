---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 method"
linktitle: "get_ExportFontsAsBase64"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 method. Specifica se le risorse dei font devono essere incorporate in HTML con codifica Base64. Il valore predefinito è false in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Specifica se le risorse dei font devono essere incorporate in HTML con codifica Base64. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Note


Per impostazione predefinita, i font vengono scritti in file separati. Se questa opzione è impostata su **true**, i font saranno incorporati nel CSS del documento con codifica Base64.

## Esempi



Mostra come salvare un documento .html con le immagini incorporate al suo interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Mostra come incorporare i font all'interno di un documento HTML salvato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
