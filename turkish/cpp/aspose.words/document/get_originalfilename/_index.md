---
title: "Aspose::Words::Document::get_OriginalFileName yöntemi"
linktitle: "get_OriginalFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_OriginalFileName yöntemi. Belgenin orijinal dosya adını C++'ta alır."
type: docs
weight: 40000
url: /tr/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Belgenin orijinal dosya adını alır.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Açıklamalar


Belge bir akıştan yüklendiyse veya boş oluşturulduysa **null** döndürür.

## Örnekler



Bir belgenin yükleme işleminin ayrıntılarını nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Bir belgenin biçimini tespit etmek için [FileFormatUtil](../../fileformatutil/) yöntemlerini nasıl kullanacağınızı gösterir.
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
