---
title: Class TextColumn
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TextColumn sınıf. Tek bir metin sütununu temsil eder.TextColumn üyesidirTextColumnCollection koleksiyon. TextColumn koleksiyon bir belgenin bir bölümündeki tüm sütunları içerir.
type: docs
weight: 6390
url: /tr/net/aspose.words/textcolumn/
---
## TextColumn class

Tek bir metin sütununu temsil eder.`TextColumn` üyesidir[`TextColumnCollection`](../textcolumncollection/) koleksiyon. `TextColumn` koleksiyon, bir belgenin bir bölümündeki tüm sütunları içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bölümlerle Çalışmak](https://docs.aspose.com/words/net/working-with-sections/) dokümantasyon makalesi.

```csharp
public class TextColumn
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Bu sütun ile sonraki sütun arasındaki boşluğu nokta cinsinden alır veya ayarlar. Son sütun için gerekli değildir. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Metin sütununun genişliğini nokta cinsinden alır veya ayarlar. |

### Notlar

`TextColumn` nesneler yalnızca özel genişlik ve aralıklara sahip sütunları belirtmek için kullanılır. Belgedeki sütunların eşit genişlikte olmasını istiyorsanız TextColumns'u ayarlayın.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) ile`doğru`.

Ne zaman yeni`TextColumn` oluşturulduğunda genişliği ve aralığı sıfıra ayarlanmıştır.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


