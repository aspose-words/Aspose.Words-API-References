---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words for .NET
description: Font EmphasisMark mülk. Bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Örnekler

Glif karakterinin üstünde/altında oluşturulan ek karakterlerin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Olası vurgu işareti türleri:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Ayrıca bakınız

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
