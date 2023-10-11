---
title: ImageSaveOptions.UseGdiEmfRenderer
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. EMF. ye kaydederken GDI veya Aspose.Words meta dosyası oluşturucusunun kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

EMF. 'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucusunun kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

### Notlar

Eğer ayarlanmışsa`doğru` GDI+ meta dosyası oluşturucusu kullanılır. Yani içerik GDI+ Graphics nesnesine yazılır ve meta dosyasına kaydedilir.

Eğer ayarlanmışsa`YANLIŞ` Aspose.Words meta dosyası oluşturucusu kullanılır. Yani içerik Aspose.Words ile direkt meta dosyası formatına yazılır.

Yalnızca EMF'ye kaydederken etkili olur.

GDI+ kaydetme yalnızca .NET'te çalışır.

Varsayılan değer:`doğru`.

### Örnekler

Bir belgeyi .emf'ye dönüştürürken oluşturucunun nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgeyi bir EMF görüntüsü olarak kaydettiğimizde, görüntü için bir oluşturucu seçmek üzere SaveOptions nesnesini iletebiliriz.
            // "UseGdiEmfRenderer" bayrağını "true" olarak ayarlarsak Aspose.Words GDI+ oluşturucuyu kullanacaktır.
            // "UseGdiEmfRenderer" bayrağını "false" olarak ayarlarsak Aspose.Words kendi meta dosyası oluşturucusunu kullanacaktır.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // GDI+ oluşturucusu genellikle daha büyük dosyalar oluşturur.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


