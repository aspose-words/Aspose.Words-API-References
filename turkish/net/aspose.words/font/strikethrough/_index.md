---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: .NET için Aspose.Words
description: Font StrikeThrough özelliğini keşfedin. Tasarımlarınızda net görsel vurgular için metni kolayca üstü çizili olarak biçimlendirin. Okunabilirliği bugün artırın!
type: docs
weight: 400
url: /tr/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Yazı tipi üstü çizili metin olarak biçimlendirilmişse doğrudur.

```csharp
public bool StrikeThrough { get; set; }
```

## Örnekler

Metne çizgi üstü çizmenin nasıl ekleneceğini gösterir.

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
