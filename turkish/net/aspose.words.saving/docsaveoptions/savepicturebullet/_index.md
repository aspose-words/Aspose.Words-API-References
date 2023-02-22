---
title: DocSaveOptions.SavePictureBullet
second_title: Aspose.Words for .NET API Referansı
description: DocSaveOptions mülk. Ne zamanyanlış  PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer doğru .
type: docs
weight: 50
url: /tr/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Ne zaman`yanlış` , PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer **doğru** .

```csharp
public bool SavePictureBullet { get; set; }
```

### Notlar

Bu seçenek, PictureBullet verileriyle düzgün çalışamayan Word 97 için sağlanmıştır. PictureBullet verilerini kaldırmak için seçeneği "yanlış" olarak ayarlayın.

### Örnekler

Kaydederken PictureBullet verilerinin belgeden nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");

// Microsoft Word 97 gibi bazı kelime işlemciler PictureBullet verileriyle uyumlu değil.
// SaveOptions nesnesinde bir bayrak ayarlayarak,
// Kaydederken tüm resim madde işaretlerini sıradan madde işaretlerine çevirebiliriz.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Ayrıca bakınız

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../docsaveoptions/)
* toplantı [Aspose.Words](../../../)


