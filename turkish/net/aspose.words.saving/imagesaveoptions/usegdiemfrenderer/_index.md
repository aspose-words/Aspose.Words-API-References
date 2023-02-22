---
title: ImageSaveOptions.UseGdiEmfRenderer
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. EMFye kaydederken GDI veya Aspose.Words meta dosyası oluşturucu kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

EMF'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucu kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

### Notlar

olarak ayarlanırsa`doğru`GDI+ meta dosyası oluşturucu kullanılır. Yani içerik GDI+graphics nesnesine yazılır ve meta dosyasına kaydedilir.

olarak ayarlanırsa`yanlış` Aspose.Words meta dosyası oluşturucu kullanılmaktadır. Yani içerik Aspose.Words ile doğrudan meta dosyası formatına yazılır.

Yalnızca EMF'ye kaydederken etkilidir.

GDI+ tasarrufu yalnızca .NET'te çalışır.

Varsayılan değer`doğru`.

### Örnekler

Bir belgeyi .emf'ye dönüştürürken bir oluşturucunun nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgeyi bir EMF görüntüsü olarak kaydettiğimizde, görüntü için bir oluşturucu seçmek için bir SaveOptions nesnesi iletebiliriz.
            // "UseGdiEmfRenderer" bayrağını "true" olarak ayarlarsak, Aspose.Words GDI+ oluşturucuyu kullanacaktır.
            // "UseGdiEmfRenderer" bayrağını "false" olarak ayarlarsak, Aspose.Words kendi metafile oluşturucusunu kullanır.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // GDI+ oluşturucu genellikle daha büyük dosyalar oluşturur.
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


