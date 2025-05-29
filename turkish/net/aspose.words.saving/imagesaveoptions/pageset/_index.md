---
title: ImageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: .NET için Aspose.Words
description: Belgenizin işlenmesini özelleştirmek için ImageSaveOptions PageSet özelliğini keşfedin. Optimize edilmiş çıktı için hangi sayfaların kaydedileceğini kontrol edin. Şimdi keşfedin!
type: docs
weight: 100
url: /tr/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

İşlenecek sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır.

```csharp
public PageSet PageSet { get; set; }
```

## Notlar

Bu özellik yalnızca belge sayfaları işlenirken etkilidir. Şekiller resimlere işlenirken bu özellik göz ardı edilir.

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

Bir belgedeki hangi sayfanın görüntü olarak işleneceğini nasıl belirteceğinizi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// Belgeyi resim olarak kaydettiğimizde Aspose.Words varsayılan olarak yalnızca ilk sayfayı işler.
// Farklı bir sayfanın nasıl işleneceğini belirtmek için SaveOptions nesnesini geçirebiliriz.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);
// Belgenin her sayfasını ayrı bir resim dosyasına dönüştür.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

Bir belgenin her sayfasının ayrı bir TIFF görüntüsüne nasıl dönüştürüleceğini gösterir.

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
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgenin hangisinden oluşturulmaya başlanacağı.
    options.PageSet = new PageSet(i);
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

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

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
