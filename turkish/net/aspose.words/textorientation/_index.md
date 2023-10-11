---
title: Enum TextOrientation
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TextOrientation Sıralama. Bir sayfadaki bir tablo hücresindeki veya bir metin çerçevesindeki metnin yönünü belirtir.
type: docs
weight: 6430
url: /tr/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Bir sayfadaki, bir tablo hücresindeki veya bir metin çerçevesindeki metnin yönünü belirtir.

```csharp
public enum TextOrientation
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Metin yatay olarak düzenlenmiştir (lr-tb). |
| Downward | `1` | Metin yukarıdan aşağıya doğru görünecek şekilde 90 derece sağa döndürülür (tb-rl). |
| Upward | `3` | Metin aşağıdan yukarıya doğru görünecek şekilde 90 derece sola döndürülür (bt-lr). |
| HorizontalRotatedFarEast | `4` | Metin yatay olarak düzenlenmiştir ancak Uzak Doğu karakterleri 90 derece sola döndürülmüştür (lr-tb-v). |
| VerticalFarEast | `5` | Uzak Doğu karakterleri dikey görünür, diğer metinler yukarıdan aşağıya doğru görünecek şekilde 90 derece sağa döndürülür (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Uzak Doğu karakterleri dikey görünür, diğer metinler dikey olarak yukarıdan aşağıya, ardından yatay olarak soldan sağa görünecek şekilde 90 derece sağa döndürülür (tb-lr-v). |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


