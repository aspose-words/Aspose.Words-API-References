---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.EmfPlusDualRenderingMode Sıralama. Aspose.Wordsün EMF Dual meta dosyalarını nasıl oluşturacağını belirtir.
type: docs
weight: 4980
url: /tr/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Aspose.Words'ün EMF+ Dual meta dosyalarını nasıl oluşturacağını belirtir.

```csharp
public enum EmfPlusDualRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ kısmını oluşturmaya çalışıyor. EMF+ kayıtlarından bazıları desteklenmiyorsa Aspose.Words, EMF+ Dual meta dosyasının EMF kısmını oluşturur. |
| EmfPlus | `1` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ kısmını oluşturur. |
| Emf | `2` | Aspose.Words, EMF+ Dual meta dosyasının EMF kısmını oluşturur. |

### Örnekler

PDF'ye kaydederken Gelişmiş Windows Meta Dosyası ile ilgili işleme seçeneklerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.Emf" olarak ayarlayın
// EMF+ ikili meta dosyasının yalnızca EMF kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlus" olarak ayarlayın
// EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlusWithFallback" olarak ayarlayın
// EMF+ kayıtlarının tümü destekleniyorsa, EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// Aksi takdirde Aspose.Words EMF kısmını oluşturacaktır.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Gömülü EMF verilerini oluşturmak için "UseEmfEmbeddedToWmf" özelliğini "true" olarak ayarlayın
// vektör grafikleri olarak oluşturabileceğimiz meta dosyalar için.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


