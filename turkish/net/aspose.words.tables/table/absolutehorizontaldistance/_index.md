---
title: Table.AbsoluteHorizontalDistance
linktitle: AbsoluteHorizontalDistance
articleTitle: AbsoluteHorizontalDistance
second_title: Aspose.Words for .NET
description: Table AbsoluteHorizontalDistance mülk. Tablo özellikleri tarafından belirtilen mutlak yatay kayan tablo konumunu puan cinsinden alır veya ayarlar. Varsayılan değer 0. dir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.tables/table/absolutehorizontaldistance/
---
## Table.AbsoluteHorizontalDistance property

Tablo özellikleri tarafından belirtilen mutlak yatay kayan tablo konumunu puan cinsinden alır veya ayarlar. Varsayılan değer 0. 'dir

```csharp
public double AbsoluteHorizontalDistance { get; set; }
```

## Örnekler

Kayan tabloların konumunun nasıl ayarlandığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Tablonun konumunu sayfada bir yere ayarlayın; bu durumda sağ alt köşe gibi.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Tabloyu eklediğimiz paragrafın konumundan itibaren noktalarda yatay ve dikey uzaklık da ayarlayabiliriz.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
