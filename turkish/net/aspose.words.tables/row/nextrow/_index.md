---
title: Row.NextRow
second_title: Aspose.Words for .NET API Referansı
description: Row mülk. Sonrakini alırRow düğüm.
type: docs
weight: 70
url: /tr/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Sonrakini alır[`Row`](../) düğüm.

```csharp
public Row NextRow { get; }
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


