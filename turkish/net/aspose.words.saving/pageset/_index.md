---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: .NET için Aspose.Words
description: Verimli belge yönetimi için Aspose.Words.Saving.PageSet sınıfını keşfedin. Rastgele sayfa kümelerini kolayca tanımlayın ve iş akışınızı bugün geliştirin!
type: docs
weight: 6170
url: /tr/net/aspose.words.saving/pageset/
---
## PageSet class

Rastgele bir sayfa kümesini tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Tam sayfa dizinine dayalı tek sayfalık bir küme oluşturur. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Tam sayfa dizinlerine dayalı bir sayfa kümesi oluşturur. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Aralıklara dayalı bir sayfa kümesi oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Belgenin tüm sayfalarını orijinal sıralarında içeren bir küme alır. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Belgenin tüm çift sayfalarını orijinal sıralarında içeren bir küme alır. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Belgenin tüm tek sayfalarını orijinal sıralarında içeren bir küme alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
