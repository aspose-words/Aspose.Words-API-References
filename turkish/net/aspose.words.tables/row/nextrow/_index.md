---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: .NET için Aspose.Words
description: Sonraki Satır düğümüne zahmetsizce erişmek için NextRow özelliğini keşfedin, böylece veri gezinme ve yönetim deneyiminizi geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Bir sonrakini alır[`Row`](../) düğüm.

```csharp
public Row NextRow { get; }
```

## Notlar

Bu yöntem, tablo satırlarına yazılmış erişime ihtiyaç duyduğunuzda kullanılabilir. Eğer a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) düğüm bir satır yerine bir tabloda bulunursa, içinde bulunan satırı almak için otomatik olarak dolaşılır.

## Örnekler

Tüm tablo hücrelerinde numaralandırmanın nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablonun tüm hücrelerini numaralandır.
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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
