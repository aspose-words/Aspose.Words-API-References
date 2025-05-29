---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: .NET için Aspose.Words
description: DocSaveOptions SavePictureBullet özelliğinin belge çıktınızı nasıl geliştirdiğini keşfedin. En iyi sonuçlar için PictureBullet veri kaydetmeyi zahmetsizce kontrol edin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Ne zaman`YANLIŞ` , PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer`doğru` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Notlar

Bu seçenek, PictureBullet verileriyle düzgün çalışamayan Word 97 için sağlanmıştır. PictureBullet verilerini kaldırmak için seçeneği "false" olarak ayarlayın.

## Örnekler

Kaydederken PictureBullet verilerinin belgeden nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Microsoft Word 97 gibi bazı kelime işlemciler PictureBullet verileriyle uyumlu değildir.
// SaveOptions nesnesinde bir bayrak ayarlayarak,
// kaydederken tüm resim madde işaretlerini normal madde işaretlerine dönüştürebiliriz.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Ayrıca bakınız

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
