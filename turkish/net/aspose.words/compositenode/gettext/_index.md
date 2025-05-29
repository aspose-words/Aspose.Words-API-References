---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: .NET için Aspose.Words
description: Düğümlerden ve alt düğümlerinden metni etkili bir şekilde almak ve veri işleme yeteneklerinizi geliştirmek için CompositeNode GetText yöntemini keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Bu düğümün ve tüm alt düğümlerinin metnini alır.

```csharp
public override string GetText()
```

## Notlar

Döndürülen dize, aşağıda açıklandığı gibi tüm denetim ve özel karakterleri içerir[`ControlChar`](../../controlchar/).

## Örnekler

Bir düğümde GetText ve ToString yöntemlerini çağırma arasındaki farkı gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText görünür metni, alan kodlarını ve özel karakterleri alacaktır.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString bize belgenin, geçilen bir kaydetme biçimine göre kaydedildiğinde nasıl görüneceğini verecektir.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Bir belgedeki liste öğelerinden oluşan tüm paragrafların nasıl çıktı alınacağını gösterir.

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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ayrıca bakınız

* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
