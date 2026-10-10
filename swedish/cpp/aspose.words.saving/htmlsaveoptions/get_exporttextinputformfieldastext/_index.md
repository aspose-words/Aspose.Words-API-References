---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText metod"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText metod. Styr hur textinmatningsformulärfält sparas till HTML eller MHTML. Standardvärdet är false i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Styr hur textinmatningsformulärfält sparas till HTML eller MHTML. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Anmärkningar


När den är satt till **true**, exporteras textinmatningsformulärfält som vanlig text. När den är **false**, exporteras Word‑textinmatningsformulärfält som INPUT‑element i HTML.

När du exporterar till EPUB sparas textinmatningsformulärfält alltid som text på grund av formatets krav.

## Exempel



Visar hur du anger mappen för lagring av länkade bilder efter att ha sparat till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML‑inmatningselement.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
