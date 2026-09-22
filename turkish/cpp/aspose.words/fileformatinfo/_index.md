---
title: "Aspose::Words::FileFormatInfo sınıfı"
linktitle: "FileFormatInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo sınıfı. FileFormatUtil belge formatı algılama yöntemleri tarafından döndürülen verileri içerir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 27000
url: /tr/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Bu, [FileFormatUtil](../fileformatutil/) belge formatı algılama yöntemleri tarafından döndürülen verileri içerir. Daha fazla bilgi edinmek için [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) belge makalesini ziyaret edin.

```cpp
class FileFormatInfo : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Mevcut belge formatına uygulanabiliyorsa algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | **true** döndürür eğer bu belge bir dijital imza içeriyorsa. Bu özellik yalnızca bir dijital imzanın belgede bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez. |
| [get_HasMacros](./get_hasmacros/)() const | **true** döndürür eğer bu belge bir VBA makrosu içeriyorsa. |
| [get_IsEncrypted](./get_isencrypted/)() const | **true** döndürür eğer belge şifrelenmişse ve açmak için bir parola gerektiriyorsa. |
| [get_LoadFormat](./get_loadformat/)() const | Algılanan belge formatını alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bu sınıfın nesneleri [DetectFileFormat()](../) yöntemleri tarafından döndürülür.

## Örnekler



[FileFormatUtil](../fileformatutil/) sınıfını belge formatını ve şifrelemeyi algılamak için nasıl kullanacağınızı gösterir.
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


[FileFormatUtil](../fileformatutil/) sınıfını belge formatını ve dijital imzaların varlığını algılamak için nasıl kullanacağınızı gösterir.
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
