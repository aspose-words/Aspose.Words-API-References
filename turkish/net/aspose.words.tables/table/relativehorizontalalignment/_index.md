---
title: Table.RelativeHorizontalAlignment
linktitle: RelativeHorizontalAlignment
articleTitle: RelativeHorizontalAlignment
second_title: .NET için Aspose.Words
description: Tablonuzun yatay hizalamasını kolayca ayarlayarak gelişmiş düzen kontrolü ve görsel çekicilik için Table RelativeHorizontalAlignment özelliğini keşfedin.
type: docs
weight: 230
url: /tr/net/aspose.words.tables/table/relativehorizontalalignment/
---
## Table.RelativeHorizontalAlignment property

Yüzen tablonun göreli yatay hizalamasını alır veya ayarlar.

```csharp
public HorizontalAlignment RelativeHorizontalAlignment { get; set; }
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

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
