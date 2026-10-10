---
title: "Aspose::Words::FileFormatUtil class"
linktitle: "FileFormatUtil"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil sınıfı. Dosya formatlarıyla çalışmak için yardımcı yöntemler sağlar; örneğin dosya formatını algılamak veya dosya uzantılarını dosya formatı enum'larına/enum'larından dönüştürmek gibi. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 28000
url: /tr/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Dosya formatlarıyla çalışmak için yardımcı yöntemler sağlar, örneğin dosya formatını algılamak veya dosya uzantılarını dosya formatı enum'larına/enum'lardan dönüştürmek. Daha fazla bilgi edinmek için [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) dokümantasyon makalesini ziyaret edin.

```cpp
class FileFormatUtil
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | IANA içerik tipini bir yükleme formatı enum değerine dönüştürür. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | IANA içerik tipini bir kaydetme formatı enum değerine dönüştürür. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Disk dosyasında depolanan bir belgenin formatı hakkında bilgiyi algılar ve döndürür. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Bir akışta depolanan belgenin formatı hakkında bilgiyi algılar ve döndürür. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Bir dosya adı uzantısını bir [SaveFormat](../saveformat/) değerine dönüştürür. |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Bir Aspose.Words görüntü tipi enum değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Bir yükleme formatı enum değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Mümkünse bir [LoadFormat](../loadformat/) değerini bir [SaveFormat](../saveformat/) değerine dönüştürür. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Bir kaydetme formatı enum değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Mümkünse bir [SaveFormat](../saveformat/) değerini bir [LoadFormat](../loadformat/) değerine dönüştürür. |

## Örnekler



Bir html dosyasında kodlamayı nasıl tespit edeceğinizi gösterir.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Encoding özelliği yalnızca bir HTML belgesi için FileFormatInfo nesnesi oluşturduğumuzda kullanılır.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
