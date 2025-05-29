---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: .NET için Aspose.Words
description: AlwaysCompressMetafiles özelliğiyle belge yönetiminizi optimize edin. Verimlilik için metafile sıkıştırmasını kontrol ederek performansı iyileştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Ne zaman`YANLIŞ` , küçük meta dosyaları performans nedeniyle sıkıştırılmaz. Varsayılan değer`doğru` , tüm meta dosyaları boyutuna bakılmaksızın sıkıştırılır.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Örnekler

Bir belgeyi kaydederken meta dosyalarının sıkıştırmasının nasıl değiştirileceğini gösterir.

```csharp
// Microsoft Equation 3.0 formülü içeren bir belgeyi açın.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Bir belgeyi kaydettiğimizde, performans nedenlerinden dolayı daha küçük meta dosyaları sıkıştırılmaz.
// SaveOptions nesnesinde, kaydederken her meta dosyasını sıkıştırmak için bir bayrak ayarlayabiliriz.
// LibreOffice gibi bazı editörler sıkıştırılmamış meta dosyalarını okuyamaz.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Ayrıca bakınız

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
