---
title: "Aspose::Words::FileFormatUtil::SaveFormatToExtension metodu"
linktitle: "SaveFormatToExtension"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::SaveFormatToExtension metodu. Bir kaydet formatı numaralandırılmış değerini dosya uzantısına dönüştürür. Döndürülen uzantı, C++'ta başında nokta bulunan küçük harfli bir dizedir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


Bir kaydetme formatı enum değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## Açıklamalar


[WordML](../../saveformat/) değeri \".wml\" olarak dönüştürülür.

[FlatOpc](../../saveformat/) değeri \".fopc\" olarak dönüştürülür.

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
