---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words for .NET
description: DocumentBuilder DeleteRow yöntem. Tablodan bir satırı siler C#'da.
type: docs
weight: 200
url: /tr/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Tablodan bir satırı siler.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableIndex | Int32 | Tablonun indeksi. |
| rowIndex | Int32 | Tablodaki satırın dizini. |

### Geri dönüş değeri

Az önce kaldırılan satır düğümü.

## Notlar

İmleç silinen satırın içindeyse, imleç dışarı doğru bir sonraki satıra veya tablodan sonraki bir sonraki paragrafa taşınır.

Yalnızca bir satır içeren bir tablodan bir satırı silerseniz, bütün tablosu silinir.

İndeks parametreleri için, indeks 0'dan büyük veya ona eşit olduğunda, ilk öğe 0 olacak şekilde başlangıç 'den bir indeks belirtir. İndeks 0'dan küçük olduğunda, son öğe -1 olacak şekilde, from dizini belirtilir.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
