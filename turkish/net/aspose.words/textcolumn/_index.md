---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: .NET için Aspose.Words
description: Belgelerinizdeki metin sütunlarını yönetmek için Aspose.Words.TextColumn sınıfını keşfedin. Metin bölümünüzdeki her sütuna kolayca erişin ve özelleştirin.
type: docs
weight: 7240
url: /tr/net/aspose.words/textcolumn/
---
## TextColumn class

Tek bir metin sütununu temsil eder.`TextColumn` üyesidir[`TextColumnCollection`](../textcolumncollection/) koleksiyon. `TextColumn`koleksiyon, bir belgenin bir bölümündeki tüm sütunları içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bölümlerle Çalışma](https://docs.aspose.com/words/net/working-with-sections/) belgeleme makalesi.

```csharp
public class TextColumn
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Bu sütun ile bir sonraki sütun arasındaki boşluğu noktalar halinde alır veya ayarlar. Son sütun için gerekli değildir. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Metin sütununun genişliğini noktalar halinde alır veya ayarlar. |

## Notlar

`TextColumn` nesneler yalnızca özel genişlik ve aralıklı sütunları belirtmek için kullanılır. Belgedeki sütunların eşit genişlikte olmasını istiyorsanız, TextColumns'ı ayarlayın.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) ile`doğru`.

Yeni bir`TextColumn` oluşturulduğunda genişliği ve aralığı sıfıra ayarlanır.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
