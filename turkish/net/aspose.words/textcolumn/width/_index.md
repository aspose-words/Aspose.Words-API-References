---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: .NET için Aspose.Words
description: Gelişmiş düzen kontrolü ve okunabilirlik için metin sütununuzun genişliğini noktalar halinde kolayca özelleştirmek üzere TextColumn Width özelliğini ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

Metin sütununun genişliğini noktalar halinde alır veya ayarlar.

```csharp
public double Width { get; set; }
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

* class [TextColumn](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
