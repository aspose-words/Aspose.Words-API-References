---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet yöntemi"
linktitle: "get_SavePictureBullet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet yöntemi. false olduğunda, PictureBullet verisi çıktı belgesine kaydedilmez. Varsayılan değer C++'da true'dur."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


**false** olduğunda, PictureBullet verileri çıktı belgesine kaydedilmez. Varsayılan değer **true**dır.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Açıklamalar


Bu seçenek Word 97 için sağlanmıştır; Word 97, PictureBullet verisiyle doğru çalışamaz. PictureBullet verisini kaldırmak için seçeneği "false" olarak ayarlayın.

## Örnekler



Kaydetme sırasında belgeden PictureBullet verisinin nasıl çıkarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Microsoft Word 97 gibi bazı kelime işlemciler, PictureBullet verisiyle uyumsuzdur.
// SaveOptions nesnesinde bir bayrak ayarlayarak,
// kaydetme sırasında tüm resim madde işaretlerini sıradan madde işaretlerine dönüştürebiliriz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Ayrıca Bakınız

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
