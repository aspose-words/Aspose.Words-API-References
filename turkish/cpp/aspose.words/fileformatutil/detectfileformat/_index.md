---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat metodu"
linktitle: "DetectFileFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat metodu. C++'ta bir akışta depolanan bir belgenin formatı hakkında bilgiyi algılar ve döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Bir akışta depolanan belgenin formatı hakkında bilgiyi algılar ve döndürür.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Akış. |

### ReturnValue

Algılanan bilgileri içeren bir [FileFormatInfo](../../fileformatinfo/) nesnesi.
## Açıklamalar


Akış, belgenin başına konumlandırılmış olmalıdır.

Bu metod döndüğünde, akıştaki konum orijinal konuma geri yüklenir.

Bu metod belge formatını algılsa bile, belirtilen belgenin geçerli olduğunu garanti etmez. Bu metod yalnızca tespit için yeterli verileri okuyarak belge formatını algılar. Bir belgenin tamamen geçerli olduğunu doğrulamak için belgeyi bir [Document](../../document/) nesnesine yüklemeniz gerekir.

Bu yöntem, format tanındığında, ancak bozulma nedeniyle algılama tamamlanamadığında [FileCorruptedException](../../filecorruptedexception/) fırlatır.

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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Disk dosyasında depolanan bir belgenin formatı hakkında bilgiyi algılar ve döndürür.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Dosya adı. |

### ReturnValue

Algılanan bilgileri içeren bir [FileFormatInfo](../../fileformatinfo/) nesnesi.
## Açıklamalar


Bu metod belge formatını algılsa bile, belirtilen belgenin geçerli olduğunu garanti etmez. Bu metod yalnızca tespit için yeterli verileri okuyarak belge formatını algılar. Bir belgenin tamamen geçerli olduğunu doğrulamak için belgeyi bir [Document](../../document/) nesnesine yüklemeniz gerekir.

Bu yöntem, format tanındığında, ancak bozulma nedeniyle algılama tamamlanamadığında [FileCorruptedException](../../filecorruptedexception/) fırlatır.

## Örnekler



Belge formatını ve şifrelemeyi tespit etmek için [FileFormatUtil](../) sınıfının nasıl kullanılacağını gösterir.
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


Belge formatını ve dijital imzaların varlığını tespit etmek için [FileFormatUtil](../) sınıfının nasıl kullanılacağını gösterir.
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

## Ayrıca Bakınız

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
