---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: MetafileRenderingOptions mülk. EMF Dual meta dosyalarının nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

EMF+ Dual meta dosyalarının nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### Notlar

EMF+ Dual meta dosyaları hem EMF+ hem de EMF parçalarını içerir. MS Word ve GDI+ her zaman EMF+ bölümünü oluşturur. Aspose.Words şu anda tüm EMF+ kayıtlarını tam olarak desteklememektedir ve bazı durumlarda EMF bölümünün sonucunun oluşturulması, EMF+ bölümünün sonucunun oluşturulmasından daha iyi görünmektedir.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır. Meta dosyası bitmap'e işlendiğinde, her zaman EMF+ kısmı kullanılır.

Varsayılan değerEmfPlusWithFallback.

### Örnekler

PDF'ye kaydederken Gelişmiş Windows Meta Dosyası ile ilgili işleme seçeneklerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.Emf" olarak ayarlayın
// bir EMF+ ikili meta dosyasının yalnızca EMF bölümünü oluşturmak için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlus" olarak ayarlayın.
// bir EMF+ ikili meta dosyasının EMF+ bölümünü oluşturmak için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlusWithFallback" olarak ayarlayın
// EMF+ kayıtlarının tümü destekleniyorsa, bir EMF+ ikili meta dosyasının EMF+ bölümünü oluşturmak için.
// Aksi takdirde Aspose.Words EMF kısmını oluşturacaktır.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Gömülü EMF verilerini işlemek için "UseEmfEmbeddedToWmf" özelliğini "true" olarak ayarlayın
// vektör grafikleri olarak oluşturabileceğimiz meta dosyalar için.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../metafilerenderingoptions/)
* toplantı [Aspose.Words](../../../)


