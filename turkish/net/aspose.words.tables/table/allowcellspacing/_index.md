---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words for .NET
description: Table AllowCellSpacing mülk. Hücreler arasındaki boşluğa izin ver seçeneğini alır veya ayarlar C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

"Hücreler arasındaki boşluğa izin ver" seçeneğini alır veya ayarlar.

```csharp
public bool AllowCellSpacing { get; set; }
```

## Örnekler

Tablodaki tek tek hücreler arasındaki boşluğun nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Hücreler arasındaki boşluğu etkinleştirmek için "AllowCellSpacing" özelliğini "true" olarak ayarlayın
// "CellSpacing" özelliğinin değerine eşit büyüklükte, nokta cinsinden.
// Hücre aralığını devre dışı bırakmak için "AllowCellSpacing" özelliğini "false" olarak ayarlayın
// ve "CellSpacing" özelliğinin değerini yok sayın.
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// "CellSpacing" özelliğinin ayarlanması hücre aralığını otomatik olarak etkinleştirecektir.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
