---
title: Row.PreviousRow
second_title: Aspose.Words for .NET API Referansı
description: Row mülk. Öncekini alırRow düğüm.
type: docs
weight: 100
url: /tr/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Öncekini alır[`Row`](../) düğüm.

```csharp
public Row PreviousRow { get; }
```

### Notlar

Bu yöntem, tablo satırlarına erişim yazmanız gerektiğinde kullanılabilir. Eğer a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)düğüm bir satır yerine bir tabloda bulunur, içinde yer alan bir satırı elde etmek için otomatik olarak geçilir.

### Örnekler

Tüm tablo hücrelerinin nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//Tablonun tüm hücrelerini numaralandırıyoruz.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Ayrıca bakınız

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../row/)
* toplantı [Aspose.Words](../../../)


