---
title: Paragraph.ListFormat
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Paragrafın liste biçimlendirme özelliklerine erişim sağlar.
type: docs
weight: 150
url: /tr/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Paragrafın liste biçimlendirme özelliklerine erişim sağlar.

```csharp
public ListFormat ListFormat { get; }
```

### Örnekler

Liste öğeleri olan bir belgedeki tüm paragrafların nasıl çıktısının alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ayrıca bakınız

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


