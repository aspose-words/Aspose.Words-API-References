---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: .NET için Aspose.Words
description: Font DoubleStrikeThrough özelliğini keşfedin. Belgelerinizde gelişmiş netlik ve stil için metni çift üstü çizili olarak kolayca biçimlendirin.
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
