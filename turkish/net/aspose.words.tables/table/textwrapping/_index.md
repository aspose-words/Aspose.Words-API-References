---
title: Table.TextWrapping
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Alır veya ayarlarTextWrapping tablo. için
type: docs
weight: 310
url: /tr/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Alır veya ayarlar`TextWrapping` tablo. için

```csharp
public TextWrapping TextWrapping { get; set; }
```

### Örnekler

Tablo metni kaydırmayla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Tablonun etrafındaki metni sarmasını sağlamak için "TextWrapping" özelliğini "TextWrapping.Around" olarak ayarlayın,
// ve konumu ayarlayarak aşağıdaki paragrafın içine doğru itin.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ayrıca bakınız

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


