---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize metodu"
linktitle: "get_ExportCompactSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize metodu. Çıktı RTF belgelerinin boyutunu küçültmeye izin verir, ancak RTL (sağdan sola) metin içeriyorlarsa doğru görüntülenmez. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Çıktı RTF belgelerinin boyutunu küçültmeye izin verir, ancak RTL (sağdan sola) metin içeriyorlarsa doğru görüntülenmez. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Açıklamalar


Aspose.Words kullanarak RTF'ye dönüştürmek istediğiniz belge Arapça gibi dillerde sağdan sola metin içermiyorsa, bu seçeneği **true** olarak ayarlayarak ortaya çıkan RTF'nin boyutunu küçültebilirsiniz.

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
