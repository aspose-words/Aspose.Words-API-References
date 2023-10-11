---
title: TextColumnCollection.Item
second_title: Aspose.Words for .NET API Referansı
description: TextColumnCollection mülk. Belirtilen dizindeki bir metin sütununu döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Belirtilen dizindeki bir metin sütununu döndürür.

```csharp
public TextColumn this[int index] { get; }
```

### Örnekler

Düzensiz aralıklı sütunların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Sütunları düzenlemek için elimizde bulunan alan miktarını belirleyin.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// İlk sütunu dar olacak şekilde ayarlayın.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// İkinci sütunu, sayfanın kenar boşluklarındaki kalan alanı kaplayacak şekilde ayarlayın.
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
* ad alanı [Aspose.Words](../../textcolumncollection/)
* toplantı [Aspose.Words](../../../)


