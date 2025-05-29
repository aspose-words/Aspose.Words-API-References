---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: .NET için Aspose.Words
description: Düzeninizdeki sütunlar arasındaki boşlukları kolayca ayarlamak için TextColumn SpaceAfter özelliğini keşfedin. Okunabilirliği ve tasarımı hassasiyetle geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Bu sütun ile bir sonraki sütun arasındaki boşluğu noktalar halinde alır veya ayarlar. Son sütun için gerekli değildir.

```csharp
public double SpaceAfter { get; set; }
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
