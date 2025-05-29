---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportImagesAsBase64 di MarkdownSaveOptions migliora i tuoi file di output consentendo il salvataggio delle immagini in formato Base64. Il valore predefinito è false.
type: docs
weight: 40
url: /it/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Specifica se le immagini vengono salvate in formato Base64 nel file di output. Il valore predefinito è`falso` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata su`VERO` i dati delle immagini vengono esportati direttamente nel**immagine** non vengono creati elementi e file separati.

## Esempi

Mostra come salvare un documento .md con immagini incorporate al suo interno.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
