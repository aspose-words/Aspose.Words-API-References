---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions ExportImagesAsBase64 özelliğinin, görüntü kaydetmeyi Base64 biçiminde sağlayarak çıktı dosyalarınızı nasıl geliştirdiğini keşfedin. Varsayılan, false.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Görüntülerin çıktı dosyasına Base64 biçiminde kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:`doğru` görüntü verileri doğrudan olarak dışa aktarılır**resim** öğeler ve ayrı dosyalar oluşturulmaz.

## Örnekler

İçerisine resimler yerleştirilmiş bir .md belgesinin nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Ayrıca bakınız

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
