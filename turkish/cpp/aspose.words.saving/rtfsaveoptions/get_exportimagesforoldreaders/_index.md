---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders yöntemi"
linktitle: "get_ExportImagesForOldReaders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders yöntemi. \"Eski okuyucular\" için anahtar kelimelerin RTF'ye yazılıp yazılmayacağını belirtir. Bu, RTF belgesinin boyutunu önemli ölçüde etkileyebilir. Varsayılan değer C++'ta true'dir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


"Eski okuyucular" için anahtar kelimelerin RTF'ye yazılıp yazılmayacağını belirtir. Bu, RTF belgesinin boyutunu önemli ölçüde etkileyebilir. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Açıklamalar


"Eski okuyucular", Microsoft Word 97 öncesi uygulamalar ve ayrıca WordPad'dir. Bu seçenek **true** olduğunda Aspose.Words ek RTF anahtar kelimeleri yazar. Bu anahtar kelimeler, belge bir "eski okuyucu" uygulamasında açıldığında doğru görüntülenmesini sağlar, ancak belgenin boyutunu önemli ölçüde artırabilir.

Bu seçeneği **false** olarak ayarlarsanız, yalnızca WMF, EMF ve BMP formatındaki görüntüler "eski okuyucularda" görüntülenir.

## Örnekler



Özel seçeneklerle bir belgeyi .rtf olarak kaydetmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir "RtfSaveOptions" nesnesi oluşturup belgeye ait "Save" yöntemine geçirerek, RTF olarak nasıl kaydedileceğini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// "ExportCompactSize" özelliğini "true" olarak ayarlayın
// sağdan sola metin uyumluluğu pahasına kaydedilen belgenin boyutunu azaltır.
options->set_ExportCompactSize(true);

// "ExportImagesFotOldReaders" özelliğini "true" olarak ayarlayın, böylece ek anahtar kelimeler kullanarak belgemizin
// Microsoft Word 97 öncesi okuyucular ve WordPad ile uyumlu olmasını sağlarsınız.
// "ExportImagesFotOldReaders" özelliğini "false" olarak ayarlayarak belgenin boyutunu azaltın,
// ancak eski okuyucuların belge içinde olabilecek metafile olmayan veya BMP görüntüleri okumasını engeller.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Ayrıca Bakınız

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
