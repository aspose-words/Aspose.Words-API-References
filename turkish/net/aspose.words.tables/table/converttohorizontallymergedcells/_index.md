---
title: Table.ConvertToHorizontallyMergedCells
second_title: Aspose.Words for .NET API Referansı
description: Table yöntem. Genişliğe göre yatay olarak birleştirilmiş hücreleri genişliklerine göre birleştirilmiş hücrelere dönüştürür.HorizontalMerge .
type: docs
weight: 390
url: /tr/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Genişliğe göre yatay olarak birleştirilmiş hücreleri, genişliklerine göre birleştirilmiş hücrelere dönüştürür.[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

### Notlar

Tablo hücreleri, birleştirme bayrakları kullanılarak yatay olarak birleştirilebilir[`HorizontalMerge`](../../cellformat/horizontalmerge/) veya hücre genişliğini kullanarak[`Width`](../../cellformat/width/).

Tablo hücresi genişlik özelliğiyle birleştirildiğinde[`HorizontalMerge`](../../cellformat/horizontalmerge/) anlamsızdır, ancak bazen birleştirme bayraklarına sahip olmak daha uygun bir yoldur.

Genişliğe göre yatay olarak birleştirilmiş tablo hücrelerini birleştirme bayraklarıyla birleştirilmiş hücrelere dönüştürmek için bu yöntemi kullanın.

### Örnekler

Genişliğe göre yatay olarak birleştirilmiş hücrelerin CellFormat.HorizontalMerge tarafından birleştirilmiş hücrelere nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word artık birleştirme bayrakları yazmıyor, bunun yerine birleştirilmiş hücreleri genişliğe göre tanımlıyor.
// Aspose.Words varsayılan olarak bir satırda yalnızca 5 hücre tanımlar ve bunların hiçbirinde yatay birleştirme bayrağı yoktur,
// yatay birleştirme gerçekleşmeden önce satırda 7 hücre olmasına rağmen.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Yatay olarak birleştirilmiş hücreleri dönüştürmek için "ConvertToHorizontallyMergedCells" yöntemini kullanın
// genişliğine göre hücreye yatay olarak bayraklarla birleştirilir.
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
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


