---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words for .NET
description: Font DoubleStrikeThrough mülk. Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğrudur.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Örnekler

Metne üstü çizili çizginin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
