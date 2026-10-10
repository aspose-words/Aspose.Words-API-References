---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64‑metod"
linktitle: "get_ExportImagesAsBase64"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64‑metod. Anger om bilder sparas i Base64‑format till utdatafilen. Standardvärdet är false i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


Anger om bilder sparas i Base64-format till utdatafilen. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## Anmärkningar


När denna egenskap är inställd på **true** exporteras bilddata direkt till **img**-elementen och separata filer skapas inte.

## Exempel



Visar hur man sparar ett .md‑dokument med inbäddade bilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## Se även

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
