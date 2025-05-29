---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: .NET için Aspose.Words
description: Aspose.Words MarkdownLinkExportMode enum'unun Markdown'da bağlantı dışa aktarımını nasıl geliştirdiğini ve belge dönüştürme sürecinizi zahmetsizce nasıl optimize ettiğini keşfedin.
type: docs
weight: 6030
url: /tr/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Bağlantıların Markdown'a nasıl aktarılacağını belirtir.

```csharp
public enum MarkdownLinkExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Her bağlantı için dışa aktarma modunu otomatik olarak algıla. |
| Inline | `1` | Tüm bağlantıları satır içi bloklar olarak dışa aktar. |
| Reference | `2` | Tüm bağlantıları referans blokları olarak dışa aktar. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
