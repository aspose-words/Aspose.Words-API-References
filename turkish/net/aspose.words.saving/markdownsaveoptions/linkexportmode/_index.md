---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: .NET için Aspose.Words
description: Çıktı dosyalarındaki bağlantı biçimlendirmesini kontrol etmek için MarkdownSaveOptions LinkExportMode özelliğini keşfedin. Belge dışa aktarımlarınızı zahmetsizce optimize edin!
type: docs
weight: 100
url: /tr/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Bağlantıların çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değerAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

## Örnekler

Bağlantıların .md dosyasına nasıl yazılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// Resim referans olarak yazılacak:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Resim satır içi olarak yazılacak:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Ayrıca bakınız

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
