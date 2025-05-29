---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.MarkdownOfficeMathExportMode'un OfficeMath'ten Markdown'a aktarımı nasıl geliştirdiğini, belge dönüşümünün doğru ve etkili olmasını nasıl sağladığını keşfedin.
type: docs
weight: 6050
url: /tr/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Aspose.Words'ün OfficeMath'i Markdown'a nasıl aktaracağını belirtir.

```csharp
public enum MarkdownOfficeMathExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Text | `0` | OfficeMath'i düz metin olarak dışa aktar. |
| Image | `1` | OfficeMath'i görüntü olarak dışa aktar. |
| MathML | `2` | OfficeMath'i MathML olarak dışa aktar. |

## Örnekler

OfficeMath'in belgeye nasıl yazılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
