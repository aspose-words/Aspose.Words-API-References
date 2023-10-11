---
title: Table.ConvertToHorizontallyMergedCells
second_title: Aspose.Words for .NET API Referansı
description: Table yöntem. Yatay olarak genişliğe göre birleştirilmiş hücreleri genişliğe göre birleştirilmiş hücrelere dönüştürürHorizontalMerge .
type: docs
weight: 410
url: /tr/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Yatay olarak genişliğe göre birleştirilmiş hücreleri, genişliğe göre birleştirilmiş hücrelere dönüştürür[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

### Notlar

Tablo hücreleri, birleştirme bayrakları kullanılarak yatay olarak birleştirilebilir[`HorizontalMerge`](../../cellformat/horizontalmerge/) veya hücre genişliğini kullanarak[`Width`](../../cellformat/width/).

Tablo hücresi genişlik özelliğine göre birleştirildiğinde[`HorizontalMerge`](../../cellformat/horizontalmerge/) anlamsızdır ancak bazen birleştirme bayraklarına sahip olmak daha uygun bir yoldur.

Genişliğe göre yatay olarak birleştirilen tablo hücrelerini, birleştirme bayraklarıyla birleştirilen hücrelere dönüştürmek için bu yöntemi kullanın.

### Örnekler

Genişliğe göre yatay olarak birleştirilen hücrelerin CellFormat.HorizontalMerge tarafından birleştirilen hücrelere nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word artık birleştirme bayrakları yazmıyor, bunun yerine birleştirilmiş hücreleri genişliğe göre tanımlıyor.
// Aspose.Words varsayılan olarak arka arkaya yalnızca 5 hücre tanımlar ve bunların hiçbirinde yatay birleştirme bayrağı yoktur,
// yatay birleştirme gerçekleşmeden önce satırda 7 hücre olmasına rağmen.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Yatay olarak birleştirilmiş hücreleri dönüştürmek için "ConvertToHorizontallyMergedCells" yöntemini kullanın
// hücrenin genişliğine göre yatay olarak bayraklarla birleştirilir.
// Artık 7 hücremiz var ve bunların bazılarının yatay birleştirme değerleri var.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


