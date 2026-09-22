---
title: "Aspose::Words::FileFormatInfo::get_LoadFormat yöntemi"
linktitle: "get_LoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo::get_LoadFormat yöntemi. C++'ta tespit edilen belge formatını alır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/fileformatinfo/get_loadformat/
---
## FileFormatInfo::get_LoadFormat method


Algılanan belge formatını alır.

```cpp
Aspose::Words::LoadFormat Aspose::Words::FileFormatInfo::get_LoadFormat() const
```

## Açıklamalar


Bir OOXML belgesi şifrelenmiş olduğunda, önce şifresini çözmeden bunun Excel, Word veya PowerPoint belgesi olup olduğunu belirlemek mümkün değildir; bu nedenle şifreli bir OOXML belgesi için bu özellik her zaman [Docx](../../loadformat/) döndürür.

## Örnekler



Belge formatını ve şifrelemeyi tespit etmek için [FileFormatUtil](../../fileformatutil/) sınıfının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Belgeyi şifrelemek için bir SaveOptions nesnesi yapılandırın
// kaydederken bir parola ile ve ardından belgeyi kaydedin.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Belgemizin dosya türünü ve şifreleme durumunu doğrulayın.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Belge formatını ve dijital imzaların varlığını tespit etmek için [FileFormatUtil](../../fileformatutil/) sınıfının nasıl kullanılacağını gösterir.
```cpp
// Bir FileFormatInfo örneğini, bir belgenin dijital olarak imzalanmadığını doğrulamak için kullanın.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Yeni bir FileFormatInstance kullanarak imzalı olduğunu onaylayın.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// İmzalı bir belgenin imzalarını bu şekilde bir koleksiyonda yükleyebilir ve erişebiliriz.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
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

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
