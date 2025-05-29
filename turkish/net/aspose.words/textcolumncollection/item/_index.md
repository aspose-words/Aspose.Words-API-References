---
title: TextColumnCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: TextColumnCollection Item özelliği ile dizine göre belirli bir metin sütununa erişin. Veri yönetimini basitleştirin ve kodlama verimliliğinizi artırın.
type: docs
weight: 30
url: /tr/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Belirtilen dizinde bir metin sütunu döndürür.

```csharp
public TextColumn this[int index] { get; }
```

## Örnekler

Eşit olmayan aralıklı sütunların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Sütunları düzenlemek için kullanabileceğimiz alan miktarını belirleyelim.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// İlk sütunu dar olarak ayarla.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// İkinci sütunun, sayfanın kenar boşlukları içinde kalan boş alanı kaplamasını sağlar.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Ayrıca bakınız

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
