---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: .NET için Aspose.Words
description: Font HighlightColor özelliğini keşfedin; gelişmiş okunabilirlik ve görsel çekicilik için metninizin vurgu rengini kolayca özelleştirin. Tasarımınızı yükseltin!
type: docs
weight: 150
url: /tr/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Vurgu (işaretleyici) rengini alır veya ayarlar.

```csharp
public Color HighlightColor { get; set; }
```

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
