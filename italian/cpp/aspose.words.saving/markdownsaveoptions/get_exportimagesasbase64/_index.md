---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 metodo"
linktitle: "get_ExportImagesAsBase64"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 metodo. Specifica se le immagini vengono salvate in formato Base64 nel file di output. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


Specifica se le immagini sono salvate in formato Base64 nel file di output. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## Note


Quando questa proprietà è impostata su **true**, i dati delle immagini vengono esportati direttamente negli elementi **img** e non vengono creati file separati.

## Esempi



Mostra come salvare un documento .md con le immagini incorporate al suo interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## Vedi anche

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
