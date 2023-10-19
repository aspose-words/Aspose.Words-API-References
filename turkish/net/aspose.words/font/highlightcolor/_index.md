---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words for .NET
description: Font HighlightColor mülk. Vurgu işaretçi rengini alır veya ayarlar C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Vurgu (işaretçi) rengini alır veya ayarlar.

```csharp
public Color HighlightColor { get; set; }
```

## Örnekler

Font özelliğini kullanarak bir metin dizisinin nasıl biçimlendirileceğini gösterir.

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
