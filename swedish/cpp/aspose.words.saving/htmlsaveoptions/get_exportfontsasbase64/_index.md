---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 metod"
linktitle: "get_ExportFontsAsBase64"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 metod. Anger om teckensnittresurser ska bäddas in i HTML i Base64‑kodning. Standard är false i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Anger om teckensnittresurser ska bäddas in i HTML med Base64‑kodning. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Anmärkningar


Som standard skrivs teckensnitt till separata filer. Om detta alternativ är satt till **true**, kommer teckensnitt att bäddas in i dokumentets CSS i Base64‑kodning.

## Exempel



Visar hur man sparar ett .html-dokument med bilder inbäddade i det.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Visar hur man bäddar in teckensnitt i ett sparat HTML-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
