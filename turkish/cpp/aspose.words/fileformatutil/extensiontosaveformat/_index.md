---
title: "Aspose::Words::FileFormatUtil::ExtensionToSaveFormat method"
linktitle: "ExtensionToSaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::ExtensionToSaveFormat method. Bir dosya adı uzantısını C++'da bir SaveFormat değerine dönüştürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil::ExtensionToSaveFormat method


Bir dosya adı uzantısını [SaveFormat](../../saveformat/) değerine dönüştürür.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(const System::String &extension)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| uzantı | const System::String\& | Dosya uzantısı. Başında nokta ile ya da nokta olmadan olabilir. Büyük/küçük harfe duyarsız. |
## Açıklamalar


Uzantı tanınamazsa, [Unknown](../../saveformat/) döndürür.

## Örnekler



[FileFormatUtil](../) yöntemlerini bir belgenin formatını tespit etmek için nasıl kullanacağınızı gösterir.
```cpp
// Dosya uzantısı eksik bir dosyadan belge yükleyin ve ardından dosya formatını tespit edin.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Aşağıda bir LoadFormat'u ilgili SaveFormat'a dönüştürmenin iki yöntemi verilmiştir.
    // 1 -  LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden ilgili SaveFormat'ı elde edin:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  LoadFormat'u doğrudan SaveFormat'ına dönüştürün:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından otomatik tespit edilen dosya uzantısına kaydedin.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
