---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: .NET için Aspose.Words
description: OfficeMath çıktısını özelleştirmek için MarkdownSaveOptions OfficeMathExportMode özelliğini keşfedin. Esnek dışa aktarma ayarlarıyla dosyalarınızı optimize edin!
type: docs
weight: 120
url: /tr/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değerText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Örnekler

OfficeMath'in belgeye nasıl yazılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Ayrıca bakınız

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
