---
title: "Aspose::Words::FileFormatInfo::get_IsEncrypted yöntemi"
linktitle: "get_IsEncrypted"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo::get_IsEncrypted yöntemi. C++'ta belge şifrelenmişse ve açmak için bir parola gerektiriyorsa true döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


**true** döndürür eğer belge şifrelenmişse ve açmak için bir parola gerektiriyorsa.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Açıklamalar


Bu özellik, şifrelenmiş belgeleri şifrelenmemişlerden ayırmanıza yardımcı olmak için vardır. Aspose.Words kullanarak bir şifreli belgeyi parola sağlamadan yüklemeye çalışırsanız bir istisna fırlatılır. Bu özelliği, bir belgenin parola gerektirip gerektirmediğini tespit etmek ve belgeyi yüklemeden önce bir işlem yapmak için kullanabilirsiniz; örneğin, kullanıcıdan parola istemek.

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

## Ayrıca Bakınız

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
