---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: .NET için Aspose.Words
description: RowFormat AllowBreakAcrossPages özelliğini keşfedin, gelişmiş okunabilirlik ve sunum için sayfa sonlarında tablo satırlarında kesintisiz metin akışını etkinleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğrudur.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Örnekler

Bir tablodaki her satır için sayfalar arası satır kırılmasının nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Satırı tutmak için "AllowBreakAcrossPages" özelliğini "false" olarak ayarlayın
// eğer bir tablo iki sayfaya yayılıyorsa ve sayfalar o satır boyunca bölünüyorsa tek parça halinde.
// Eğer satır bir sayfaya sığmayacak kadar büyükse, Microsoft Word onu bir sonraki sayfaya itecektir.
// Satırın iki sayfaya bölünmesine izin vermek için "AllowBreakAcrossPages" özelliğini "true" olarak ayarlayın.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Ayrıca bakınız

* class [RowFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
