---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: .NET için Aspose.Words
description: Uygulamalarınızda gelişmiş veri sunumu için hücre biçimlendirme seçeneklerine kolayca erişmek ve bunları özelleştirmek amacıyla Cell CellFormat özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Hücrenin biçimlendirme özelliklerine erişim sağlar.

```csharp
public CellFormat CellFormat { get; }
```

## Örnekler

Bir tablo hücresinin biçimlendirmesinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Bir hücrenin görünümünü değiştiren biçimlendirmeyi ayarlamak için o hücrenin "CellFormat" özelliğini kullanın.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

İki tablodaki satırların nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Aşağıda bir belgeden tablo almanın iki yolu bulunmaktadır.
// 1 - Bir Body düğümünün "Tablolar" koleksiyonundan:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - "GetChild" metodunu kullanarak:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Mevcut tablodaki tüm satırları bir sonrakine ekle.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Boş tablo kabını kaldır.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Bir tablodaki satır ve hücrelerin biçiminin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Biçimlendirmeyi değiştirmek için ilk satırın "RowFormat" özelliğini kullanın
// Bu satırdaki tüm hücrelerin içerikleri.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Son satırdaki ilk hücrenin "CellFormat" özelliğini kullanarak o hücrenin içeriğinin biçimlendirmesini değiştirin.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Ayrıca bakınız

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
