---
title: PageSet.PageSet
second_title: Aspose.Words for .NET API Referansı
description: PageSet inşaatçı. Tam sayfa dizinine dayalı olarak tek sayfalık bir grup oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pageset/pageset/
---
## PageSet(int) {#constructor_1}

Tam sayfa dizinine dayalı olarak tek sayfalık bir grup oluşturur.

```csharp
public PageSet(int page)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| page | Int32 | Sayfanın sıfır tabanlı dizini. |

### Notlar

Belgede bulunmayan bir sayfayla karşılaşılırsa oluşturma sırasında bir istisna atılır. MaxValue belgedeki son sayfa anlamına gelir.

### Ayrıca bakınız

* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../pageset/)
* toplantı [Aspose.Words](../../../)

---

## PageSet(params int[]) {#constructor_2}

Tam sayfa indekslerine dayalı bir sayfa seti oluşturur.

```csharp
public PageSet(params int[] pages)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pages | Int32[] | Sıfır tabanlı sayfa dizinleri. |

### Notlar

Belgede bulunmayan bir sayfayla karşılaşılırsa oluşturma sırasında bir istisna atılır. MaxValue belgedeki son sayfa anlamına gelir.

### Örnekler

Tam sayfa indekslerine göre sayfaların nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgeye beş sayfa ekleyin.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Save" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// XPS çıktısı olarak kaydedilecek belge sayfalarının bir kümesini seçmek için "PageSet" özelliğini kullanın.
// Bu durumda, sıfır tabanlı bir dizin aracılığıyla yalnızca üç sayfayı seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Ayrıca bakınız

* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../pageset/)
* toplantı [Aspose.Words](../../../)

---

## PageSet(params PageRange[]) {#constructor}

Aralıklara dayalı bir sayfa grubu oluşturur.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| ranges | PageRange[] | Sayfa aralıkları dizisi. |

### Notlar

Belgedeki son sayfadan sonra başlayan bir aralıkla karşılaşılırsa, oluşturma sırasında bir istisna atılır. Son sayfadan sonra biten tüm aralıklar belgeye sığacak şekilde kesilir.

### Örnekler

Tam sayfa aralıklarına göre sayfaların nasıl çıkarılacağını gösterir.

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
* ad alanı [Aspose.Words.Saving](../../pageset/)
* toplantı [Aspose.Words](../../../)


