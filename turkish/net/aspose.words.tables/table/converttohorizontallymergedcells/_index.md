---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: .NET için Aspose.Words
description: ConvertToHorizontallyMergedCells yönteminin geniş birleştirilmiş hücreleri yatay birleştirilmiş hücrelere nasıl dönüştürdüğünü ve böylece veri organizasyonunuzu nasıl geliştirdiğini keşfedin.
type: docs
weight: 410
url: /tr/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Genişliğe göre yatay olarak birleştirilen hücreleri, genişliğe göre birleştirilen hücrelere dönüştürür.[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Notlar

Tablo hücreleri, birleştirme bayrakları kullanılarak yatay olarak birleştirilebilir[`HorizontalMerge`](../../cellformat/horizontalmerge/) veya hücre genişliğini kullanarak[`Width`](../../cellformat/width/).

Tablo hücresi genişlik özelliğine göre birleştirildiğinde[`HorizontalMerge`](../../cellformat/horizontalmerge/) anlamsızdır ancak bazen birleştirme bayrakları kullanmak daha kullanışlı bir yoldur.

Bu yöntemi, genişliğe göre yatay olarak birleştirilen tablo hücrelerini birleştirme bayraklarıyla birleştirilen hücrelere dönüştürmek için kullanın.

## Örnekler

Genişliğe göre yatay olarak birleştirilen hücrelerin, CellFormat.HorizontalMerge kullanılarak birleştirilen hücrelere nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word artık birleştirme bayrakları yazmıyor, bunun yerine birleştirilmiş hücreleri genişliğe göre tanımlıyor.
// Aspose.Words varsayılan olarak bir satırda yalnızca 5 hücre tanımlar ve bunların hiçbiri yatay birleştirme bayrağına sahip değildir.
// yatay birleştirme gerçekleşmeden önce satırda 7 hücre olmasına rağmen.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Yatay olarak birleştirilmiş hücreleri dönüştürmek için "ConvertToHorizontallyMergedCells" yöntemini kullanın
// yatay olarak bayraklarla birleştirilen hücrenin genişliğine göre.
// Şimdi 7 hücremiz var ve bazılarının yatay birleştirme değerleri var.
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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
