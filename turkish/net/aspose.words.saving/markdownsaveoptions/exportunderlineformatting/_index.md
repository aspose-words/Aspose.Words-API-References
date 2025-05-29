---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions ExportUnderlineFormatting özelliğinin metin dışa aktarımınızı nasıl geliştirdiğini keşfedin. Bu boolean ayarıyla alt çizgi biçimlendirmesini kolayca kontrol edin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Alt çizgi metin biçimlendirmesini iki artı karakter dizisi "++" olarak dışa aktarmayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Örnekler

Alt çizgi biçimlendirmesinin ++ olarak nasıl dışarı aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Ayrıca bakınız

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
