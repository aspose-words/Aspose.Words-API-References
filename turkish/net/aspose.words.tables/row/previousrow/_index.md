---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: .NET için Aspose.Words
description: Önceki Satır özelliğine erişerek önceki Satır düğümünü kolayca alabilir, veri gezintinizi geliştirebilir ve kodlama iş akışınızı hızlandırabilirsiniz.
type: docs
weight: 100
url: /tr/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Öncekini alır[`Row`](../) düğüm.

```csharp
public Row PreviousRow { get; }
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
