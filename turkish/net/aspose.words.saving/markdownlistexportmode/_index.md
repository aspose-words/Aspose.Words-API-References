---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: .NET için Aspose.Words
description: Aspose.Words' MarkdownListExportMode enum'unun, Markdown'a liste aktarımını nasıl geliştirdiğini, belgeleriniz için hassas biçimlendirme ve kusursuz entegrasyon sağladığını keşfedin.
type: docs
weight: 6040
url: /tr/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Listelerin Markdown'a nasıl aktarılacağını belirtir.

```csharp
public enum MarkdownListExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| MarkdownSyntax | `0` | Markdown sözdizimiyle uyumlu liste öğelerini dışa aktar. |
| PlainText | `1` | Liste öğelerini düz metin olarak dışa aktar. |

## Örnekler

Öğelerin listelenmesinin markdown belgesine nasıl yazılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Listeyi dışa aktarmak için MarkdownListExportMode.PlainText veya MarkdownListExportMode.MarkdownSyntax'ı kullanın.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
