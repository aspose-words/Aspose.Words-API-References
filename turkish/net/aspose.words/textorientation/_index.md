---
title: Enum TextOrientation
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TextOrientation Sıralama. Bir sayfadaki tablo hücresindeki veya metin çerçevesindeki metnin yönünü belirtir.
type: docs
weight: 6130
url: /tr/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Bir sayfadaki, tablo hücresindeki veya metin çerçevesindeki metnin yönünü belirtir.

```csharp
public enum TextOrientation
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Metin yatay olarak düzenlenir (lr-tb). |
| Downward | `1` | Metin yukarıdan aşağıya (tb-rl) görünecek şekilde 90 derece sağa döndürülür. |
| Upward | `3` | Metin, aşağıdan yukarıya doğru görünmesi için 90 derece sola döndürülür (bt-lr). |
| HorizontalRotatedFarEast | `4` | Metin yatay olarak düzenlenir, ancak Uzak Doğu karakterleri 90 derece sola döndürülür (lr-tb-v). |
| VerticalFarEast | `5` | Uzak Doğu karakterleri dikey görünür, diğer metinler 90 derece döndürülür yukarıdan aşağıya doğru görünecek şekilde (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Uzak Doğu karakterleri dikey görünür, diğer metinler 90 derece döndürülür dikey olarak yukarıdan aşağıya, ardından soldan sağa yatay olarak (tb-lr-v). |

### Örnekler

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

// Tabloyu oluştururken, belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecinin içinde bulunduğu geçerli satıra/hücreye ve bunları oluştururken yeni satırlara/hücrelere.
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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


