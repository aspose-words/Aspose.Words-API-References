---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: .NET için Aspose.Words
description: En iyi EMF Dual meta dosyası oluşturma için Aspose.Words' EMF Plus Dual Rendering Mode enum'unu keşfedin. Belge işlemenizi hassasiyetle geliştirin!
type: docs
weight: 5730
url: /tr/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Aspose.Words'ün EMF+ Dual meta dosyalarını nasıl işleyeceğini belirtir.

```csharp
public enum EmfPlusDualRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ kısmını işlemeye çalışır. EMF+ kayıtlarından bazıları desteklenmiyorsa Aspose.Words, EMF+ Dual meta dosyasının EMF kısmını işler. |
| EmfPlus | `1` | Aspose.Words, EMF+ Dual meta dosyasının EMF+ kısmını oluşturur. |
| Emf | `2` | Aspose.Words, EMF+ Dual meta dosyasının EMF kısmını oluşturur. |

## Örnekler

PDF'ye kaydederken Gelişmiş Windows Meta Dosyası ile ilgili işleme seçeneklerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.Emf" olarak ayarlayın
// EMF+ ikili meta dosyasının yalnızca EMF kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlus" olarak ayarlayın
// EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlusWithFallback" olarak ayarlayın
// EMF+ kayıtlarının tümü destekleniyorsa, EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// Aksi halde Aspose.Words EMF kısmını işleyecektir.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Gömülü EMF verilerini işlemek için "UseEmfEmbeddedToWmf" özelliğini "true" olarak ayarlayın
// vektörel grafikler olarak işlenebilecek meta dosyaları için.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
