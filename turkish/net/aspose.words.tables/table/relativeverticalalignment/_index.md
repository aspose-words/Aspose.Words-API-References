---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: .NET için Aspose.Words
description: Yüzen tablolar için dikey hizalamayı kolayca yönetmek, düzeninizin hassasiyetini ve tasarımını geliştirmek için Table RelativeVerticalAlignment özelliğini keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Yüzen tablonun göreli dikey hizalamasını alır veya ayarlar.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
```

## Örnekler

Yüzen tabloların konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Tablonun konumunu sayfadaki bir yere, örneğin bu durumda sağ alt köşeye ayarlayın.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Ayrıca tabloyu eklediğimiz paragrafın konumundan itibaren yatay ve dikey olarak puan cinsinden bir ofset de ayarlayabiliriz.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Ayrıca bakınız

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
