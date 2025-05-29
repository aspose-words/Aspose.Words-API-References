---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: .NET için Aspose.Words
description: Tablolarınızdaki metin akışını kolayca yönetmek için Table TextWrapping özelliğini keşfedin. Esnek metin seçenekleriyle okunabilirliği ve tasarımı geliştirin!
type: docs
weight: 310
url: /tr/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Alır veya ayarlar`TextWrapping` tablo için.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## Örnekler

Tablo metin kaydırmanın nasıl yapılacağını gösterir.

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

// Tablonun metni etrafına sarmasını sağlamak için "TextWrapping" özelliğini "TextWrapping.Around" olarak ayarlayın,
// ve pozisyonunu ayarlayarak aşağıdaki paragrafa doğru itin.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ayrıca bakınız

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
