---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
articleTitle: AbsoluteVerticalDistance
second_title: .NET için Aspose.Words
description: Tablolar için AbsoluteVerticalDistance özelliğini keşfedin; hassas düzen için noktalardaki dikey konumlandırmayı kontrol edin. Varsayılan 0'dır. Tasarımınızı optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Tablo özellikleri tarafından belirtilen mutlak dikey yüzen tablo konumunu noktalar halinde alır veya ayarlar. Varsayılan değer 0'dır.

```csharp
public double AbsoluteVerticalDistance { get; set; }
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

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
