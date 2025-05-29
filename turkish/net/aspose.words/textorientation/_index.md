---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: .NET için Aspose.Words
description: Tablo hücrelerinde ve metin çerçevelerinde metin hizalamasını kolayca kontrol etmek, belge sunumunu ve okunabilirliğini geliştirmek için Aspose.Words.TextOrientation enum'unu keşfedin.
type: docs
weight: 7280
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
| Upward | `3` | Metin, aşağıdan yukarıya doğru görünecek şekilde 90 derece sola döndürülür (bt-lr). |
| HorizontalRotatedFarEast | `4` | Metin yatay olarak düzenlenmiştir, ancak Uzak Doğu karakterleri 90 derece sola döndürülmüştür (lr-tb-v). |
| VerticalFarEast | `5` | Uzak Doğu karakterleri dikey görünür, diğer metin yukarıdan aşağıya doğru görünmesi için 90 derece sağa döndürülür (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Uzak Doğu karakterleri dikey görünür, diğer metinler 90 derece sağa döndürülür ve dikey olarak yukarıdan aşağıya, sonra yatay olarak soldan sağa (tb-lr-v) görünür. |

## Örnekler

Biçimlendirilmiş 2x2'lik bir tablonun nasıl oluşturulacağını gösterir.

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

// Tablo oluşturulurken, belge oluşturucu geçerli RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecin bulunduğu geçerli satıra/hücreye ve bunları oluştururken oluşacak yeni satırlara/hücrelere.
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

// Daha önce eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesinde yapılan değişikliklerden geriye dönük olarak etkilenmez.
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
