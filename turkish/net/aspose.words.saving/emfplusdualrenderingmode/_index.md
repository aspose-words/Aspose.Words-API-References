---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.EmfPlusDualRenderingMode Sıralama. Aspose.Wordsün EMF Dual meta dosyalarını nasıl oluşturacağını belirtir.
type: docs
weight: 4720
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
| EmfPlusWithFallback | `0` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ parçasını oluşturmaya çalışır. EMF+ kayıtlarından bazıları desteklenmiyorsa o zaman Aspose.Words, EMF'yi EMF+ Dual meta dosyasının bir parçası haline getirir. |
| EmfPlus | `1` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ parçasını oluşturur. |
| Emf | `2` | Aspose.Words, EMF+ Dual meta dosyasının EMF parçasını oluşturur. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


