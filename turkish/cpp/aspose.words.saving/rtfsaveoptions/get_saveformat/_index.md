---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat metodu"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat metodu. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. C++'ta yalnızca Rtf olabilir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Rtf](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
