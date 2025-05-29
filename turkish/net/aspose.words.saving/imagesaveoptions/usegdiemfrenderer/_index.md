---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: .NET için Aspose.Words
description: ImageSaveOptions ile EMF tasarrufunu optimize edin. Gelişmiş görüntü kalitesi ve performansı için GDI veya Aspose.Words renderer ayarlarını kontrol edin.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

EMF'ye kaydederken GDI+ veya Aspose.Words meta dosyası oluşturucusunun kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Notlar

Eğer ayarlanırsa`doğru` GDI+ metafile renderer kullanıldı. Yani içerik GDI+ graphics nesnesine yazıldı ve metafile'a kaydedildi.

Eğer ayarlanırsa`YANLIŞ` Aspose.Words metafile renderer'ı kullanıldı. Yani içerik doğrudan Aspose.Words ile metafile formatına yazıldı.

Sadece EMF'ye kaydedildiğinde etkilidir.

GDI+ kaydetme sadece .NET'te çalışır.

Varsayılan değer:`doğru`.

## Örnekler

Bir belgeyi .emf formatına dönüştürürken bir görüntü oluşturucunun nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi EMF görüntüsü olarak kaydettiğimizde, görüntü için bir görüntü oluşturucu seçmek üzere bir SaveOptions nesnesi geçirebiliriz.
// "UseGdiEmfRenderer" bayrağını "true" olarak ayarlarsak, Aspose.Words GDI+ renderer'ını kullanacaktır.
// "UseGdiEmfRenderer" bayrağını "false" olarak ayarlarsak, Aspose.Words kendi meta dosyası oluşturucusunu kullanacaktır.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
