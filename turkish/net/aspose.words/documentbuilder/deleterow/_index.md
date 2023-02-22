---
title: DocumentBuilder.DeleteRow
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Tablodan bir satırı siler.
type: docs
weight: 180
url: /tr/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Tablodan bir satırı siler.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableIndex | Int32 | Tablonun dizini. |
| rowIndex | Int32 | Tablodaki satırın dizini. |

### Geri dönüş değeri

Az önce kaldırılan satır düğümü.

### Notlar

İmleç silinmekte olan satırın içindeyse, imleç sonraki satıra veya tablodan sonraki paragrafa taşınır.

Yalnızca bir satır içeren bir tablodan bir satırı silerseniz, bütün tablosu silinir.

İndeks parametreleri için, indeks 0'dan büyük veya 0'a eşit olduğunda, ilk eleman 0 olmak üzere, başlangıç olan bir indeks belirtir. Dizin 0'dan küçük olduğunda, son öğe olan -1 olmak üzere sondan bir dizin belirledi.

### Örnekler

Tablodan bir satırın nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Belgedeki ilk tablonun ilk satırını silin.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Ayrıca bakınız

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


