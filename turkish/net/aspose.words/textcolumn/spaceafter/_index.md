---
title: TextColumn.SpaceAfter
second_title: Aspose.Words for .NET API Referansı
description: TextColumn mülk. Bu sütun ile sonraki sütun arasındaki boşluğu puan olarak alır veya ayarlar. Son sütun için gerekli değil.
type: docs
weight: 10
url: /tr/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Bu sütun ile sonraki sütun arasındaki boşluğu puan olarak alır veya ayarlar. Son sütun için gerekli değil.

```csharp
public double SpaceAfter { get; set; }
```

### Örnekler

Eşit olmayan aralıklı sütunların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Sütunları düzenlemek için elimizdeki oda miktarını belirleyin.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// İlk sütunu dar olacak şekilde ayarlayın.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// İkinci sütunu sayfanın kenar boşluklarında kalan kullanılabilir alanı alacak şekilde ayarlayın.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Ayrıca bakınız

* class [TextColumn](../)
* ad alanı [Aspose.Words](../../textcolumn/)
* toplantı [Aspose.Words](../../../)


