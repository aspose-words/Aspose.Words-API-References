---
title: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature yöntemi"
linktitle: "get_HasDigitalSignature"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature yöntemi. C++'ta bu belgenin bir dijital imza içeriyorsa true döndürür. Bu özellik yalnızca bir dijital imzanın belgede bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


**true** döndürür eğer bu belge bir dijital imza içeriyorsa. Bu özellik yalnızca bir dijital imzanın belgede bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Açıklamalar


Bu özellik, dijital olarak imzalanmış belgeleri imzası olmayanlardan ayırmanıza yardımcı olmak için vardır. Aspose.Words kullanarak dijital imzalı bir belgeyi değiştirir ve kaydederseniz, dijital imza kaybolur. Bu, bir dijital imzanın belgenin özgünlüğünü korumak için var olduğu tasarım gereği böyle olur. Bu özelliği kullanarak dijital imzalı belgeleri normal belgeler gibi işlemeye başlamadan önce tespit edebilir ve dijital imzanın kaybolmasını önlemek için bir işlem yapabilirsiniz; örneğin kullanıcıyı bilgilendirmek.

## Örnekler



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

## Ayrıca Bakınız

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
