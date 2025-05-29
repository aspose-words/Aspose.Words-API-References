---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: .NET için Aspose.Words
description: DocumentBuilder DeleteRow yöntemiyle tablolardan satırları zahmetsizce kaldırın. Belge düzenlemenizi kolaylaştırın ve iş akışınızı geliştirin!
type: docs
weight: 200
url: /tr/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Bir tablodan bir satırı siler.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableIndex | Int32 | Tablonun indeksi. |
| rowIndex | Int32 | Tablodaki satırın indeksi. |

### Geri dönüş değeri

Az önce kaldırılan satır düğümü.

## Notlar

Eğer imleç silinen satırın içindeyse, imleç tablodan sonraki satıra veya paragrafa taşınır.

Yalnızca bir satır içeren bir tablodan bir satırı silerseniz, whole tablosu silinir.

Dizin parametreleri için, dizin 0'dan büyük veya eşit olduğunda, 0'ın ilk öğe olduğu başlangıç olan from dizini belirtir. Dizin 0'dan küçük olduğunda, -1'in son öğe olduğu bitiş olan from dizini belirtir.

## Örnekler

Bir tablodan satırın nasıl silineceğini gösterir.

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

// Belgedeki ilk tablonun ilk satırını sil.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Ayrıca bakınız

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
