---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words for .NET
description: Row RowFormat mülk. Satırın biçimlendirme özelliklerine erişim sağlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Satırın biçimlendirme özelliklerine erişim sağlar.

```csharp
public RowFormat RowFormat { get; }
```

## Örnekler

Bir tablo satırının formatının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tüm satırın görünümünü değiştiren biçimlendirmeyi ayarlamak için ilk satırın "RowFormat" özelliğini kullanın.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Bir tablodaki satırların ve hücrelerin biçiminin nasıl değiştirileceğini gösterir.

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
// bu satırdaki tüm hücrelerin içeriği.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Hücrenin içeriğinin biçimlendirmesini değiştirmek için son satırdaki ilk hücrenin "CellFormat" özelliğini kullanın.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Ayrıca bakınız

* class [RowFormat](../../rowformat/)
* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
