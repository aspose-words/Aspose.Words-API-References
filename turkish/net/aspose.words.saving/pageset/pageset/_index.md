---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: .NET için Aspose.Words
description: Hassas sayfa dizini ve kusursuz kullanıcı deneyimi için tasarlanmış PageSet oluşturucusu ile zahmetsizce size özel tek sayfalık bir set oluşturun.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Tam sayfa dizinine dayalı tek sayfalık bir küme oluşturur.

```csharp
public PageSet(int page)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| page | Int32 | Sayfanın sıfır tabanlı indeksi. |

## Notlar

Belgede olmayan bir sayfayla karşılaşılırsa, işleme sırasında bir istisna atılır. MaxValue belgenin son sayfası anlamına gelir.

## Örnekler

Bir belgenin bir sayfasının JPEG görüntüsüne nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// İkinci sayfayı seçmek için "PageSet"i "1" olarak ayarlayın
// belgenin oluşturulmaya başlanacağı sıfır tabanlı dizin.
options.PageSet = new PageSet(1);

// Belgeyi JPEG formatında kaydettiğimizde Aspose.Words yalnızca bir sayfa oluşturur.
// Bu resim ikinci sayfadan başlayarak tek bir sayfa içerecektir,
// bu sadece orijinal belgenin ikinci sayfası olacak.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Ayrıca bakınız

* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Tam sayfa dizinlerine dayalı bir sayfa kümesi oluşturur.

```csharp
public PageSet(params int[] pages)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pages | Int32[] | Sayfaların sıfır tabanlı indeksleri. |

## Notlar

Belgede olmayan bir sayfayla karşılaşılırsa, işleme sırasında bir istisna atılır. MaxValue belgenin son sayfası anlamına gelir.

## Örnekler

Sayfaların kesin sayfa indekslerine göre nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgeye beş sayfa ekle.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Çıkış XPS'e kaydedilecek belgenin sayfalarının bir kümesini seçmek için "PageSet" özelliğini kullanın.
// Bu durumda, sıfır tabanlı bir dizin aracılığıyla yalnızca üç sayfa seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Ayrıca bakınız

* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Aralıklara dayalı bir sayfa kümesi oluşturur.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| ranges | PageRange[] | Sayfa aralıkları dizisi. |

## Notlar

Belgedeki son sayfadan sonra başlayan bir aralıkla karşılaşılırsa, işleme sırasında bir istisna atılır. Son sayfadan sonra biten tüm aralıklar, belgeye sığacak şekilde kesilir.

## Örnekler

Sayfaların tam sayfa aralıklarına göre nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Ayrıca bakınız

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
