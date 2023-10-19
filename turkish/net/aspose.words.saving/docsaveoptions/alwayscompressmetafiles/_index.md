---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words for .NET
description: DocSaveOptions AlwaysCompressMetafiles mülk. Ne zamanYANLIŞ  küçük meta dosyalar performans nedeniyle sıkıştırılmaz. Varsayılan değerdoğru  tüm meta dosyalar boyutuna bakılmaksızın sıkıştırılır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Ne zaman`YANLIŞ` , küçük meta dosyalar performans nedeniyle sıkıştırılmaz. Varsayılan değer:`doğru` , tüm meta dosyalar boyutuna bakılmaksızın sıkıştırılır.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Örnekler

Bir belgeyi kaydederken meta dosya sıkıştırmasının nasıl değiştirileceğini gösterir.

```csharp
// Microsoft Denklem 3.0 formülünü içeren bir belgeyi açın.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Bir belgeyi kaydettiğimizde performans nedeniyle daha küçük meta dosyalar sıkıştırılmaz.
// Kaydederken her meta dosyayı sıkıştırmak için SaveOptions nesnesine bir bayrak ayarlayabiliriz.
// LibreOffice gibi bazı düzenleyiciler sıkıştırılmamış meta dosyaları okuyamaz.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### Ayrıca bakınız

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
