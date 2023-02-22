---
title: Class TextColumn
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TextColumn sınıf. Tek bir metin sütununu temsil eder. Metin Sütunu üyesidirTextColumnCollection koleksiyon.  Metin Sütunları koleksiyon bir belgenin bir bölümündeki tüm sütunları içerir.
type: docs
weight: 6090
url: /tr/net/aspose.words/textcolumn/
---
## TextColumn class

Tek bir metin sütununu temsil eder. **Metin Sütunu** üyesidir[`TextColumnCollection`](../textcolumncollection/) koleksiyon.  **Metin Sütunları** koleksiyon, bir belgenin bir bölümündeki tüm sütunları içerir.

```csharp
public class TextColumn
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Bu sütun ile sonraki sütun arasındaki boşluğu puan olarak alır veya ayarlar. Son sütun için gerekli değil. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Nokta olarak metin sütununun genişliğini alır veya ayarlar. |

### Notlar

**Metin Sütunu** nesneler yalnızca özel genişlik ve aralıklı sütunları belirtmek için kullanılır. Belgedeki sütunların eşit genişlikte olmasını istiyorsanız, TextColumns'u ayarlayın.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) ile **doğru**.

ne zaman yeni **Metin Sütunu** oluşturulduğunda genişliği ve aralığı sıfıra ayarlanmıştır.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


