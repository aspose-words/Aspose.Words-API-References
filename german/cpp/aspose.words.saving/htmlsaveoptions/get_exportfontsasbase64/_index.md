---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 Methode"
linktitle: "get_ExportFontsAsBase64"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 Methode. Gibt an, ob Schriftartressourcen in das HTML als Base64‑Kodierung eingebettet werden sollen. Standard ist false in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Gibt an, ob Schriftartressourcen in HTML im Base64-Format eingebettet werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Hinweise


Standardmäßig werden Schriftarten in separate Dateien geschrieben. Wenn diese Option auf **true** gesetzt ist, werden die Schriftarten in das CSS des Dokuments als Base64‑Kodierung eingebettet.

## Beispiele



Zeigt, wie man ein .html-Dokument mit eingebetteten Bildern speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Zeigt, wie man Schriftarten in ein gespeichertes HTML-Dokument einbettet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
