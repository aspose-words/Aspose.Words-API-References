---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 Methode"
linktitle: "get_ExportImagesAsBase64"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 Methode. Gibt an, ob Bilder im Base64-Format in die Ausgabedatei gespeichert werden. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


Gibt an, ob Bilder im Base64-Format in die Ausgabedatei gespeichert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## Hinweise


Wenn diese Eigenschaft auf **true** gesetzt ist, werden Bilddaten direkt in die **img**-Elemente exportiert und separate Dateien werden nicht erstellt.

## Beispiele



Zeigt, wie man ein .md-Dokument mit eingebetteten Bildern speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## Siehe auch

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
