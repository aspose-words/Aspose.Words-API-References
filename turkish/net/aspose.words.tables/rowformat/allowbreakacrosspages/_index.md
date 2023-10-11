---
title: RowFormat.AllowBreakAcrossPages
second_title: Aspose.Words for .NET API Referansı
description: RowFormat mülk. Tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğrudur.
type: docs
weight: 10
url: /tr/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğrudur.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### Örnekler

Bir tablodaki her satır için satırların sayfalar arasında bölünmesinin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Satırı korumak için "AllowBreakAcrossPages" özelliğini "false" olarak ayarlayın
// eğer bir tablo o satır boyunca bölünen iki sayfayı kapsıyorsa tek parça halinde.
// Satır bir sayfaya sığmayacak kadar büyükse, Microsoft Word onu bir sonraki sayfaya itecektir.
// Satırın iki sayfaya bölünmesine izin vermek için "AllowBreakAcrossPages" özelliğini "true" olarak ayarlayın.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Ayrıca bakınız

* class [RowFormat](../)
* ad alanı [Aspose.Words.Tables](../../rowformat/)
* toplantı [Aspose.Words](../../../)


