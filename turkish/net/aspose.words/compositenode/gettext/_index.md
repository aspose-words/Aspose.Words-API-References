---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: CompositeNode GetText yöntem. Bu düğümün ve tüm alt öğelerinin metnini alır C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Bu düğümün ve tüm alt öğelerinin metnini alır.

```csharp
public override string GetText()
```

## Notlar

Döndürülen dize, yukarıda açıklandığı gibi tüm kontrol ve özel karakterleri içerir.[`ControlChar`](../../controlchar/).

## Örnekler

Bir düğümde GetText ve ToString yöntemlerinin çağrılması arasındaki farkı gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText görünür metni, alan kodlarını ve özel karakterleri de alacaktır.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString, eğer başarılı bir kaydetme biçiminde kaydedilirse, belgenin görünümünü bize verecektir.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Bir belgedeki liste öğesi olan tüm paragrafların çıktısının nasıl alınacağını gösterir.

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

* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
