---
title: CellVerticalAlignment Enum
linktitle: CellVerticalAlignment
articleTitle: CellVerticalAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.CellVerticalAlignment Sıralama. Bir tablo hücresi içindeki metnin dikey hizalamasını belirtir C#'da.
type: docs
weight: 6280
url: /tr/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

Bir tablo hücresi içindeki metnin dikey hizalamasını belirtir.

```csharp
public enum CellVerticalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Top | `0` | Metin hücrenin üstüne hizalanır. |
| Center | `1` | Metin hücrenin ortasına hizalanır. |
| Bottom | `2` | Metin hücrenin altına hizalanır. |

## Örnekler

Biçimlendirilmiş bir 2x2 tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Tabloyu oluştururken belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecin bulunduğu geçerli satıra/hücreye ve onları oluştururken yeni satırlara/hücrelere.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Önceden eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesindeki değişikliklerden geriye dönük olarak etkilenmez.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
