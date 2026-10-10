---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding yöntemi"
linktitle: "get_Encoding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding yöntemi. Metin formatlarında dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer C++'ta Encoding.UTF8'tir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/txtsaveoptionsbase/get_encoding/
---
## TxtSaveOptionsBase::get_Encoding method


Metin formatlarında dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer **Encoding.UTF8**'dir.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding() const
```


## Örnekler



.txt çıktı belgesi için kodlamayı nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ASCII karakter kümesinin dışındaki karakterler içeren bazı metinler ekleyin.
builder->Write(u"À È Ì Ò Ù.");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// "Encoding" özelliğinin belge içeriğimiz için uygun kodlamayı içerdiğini doğrulayın.
ASPOSE_ASSERT_EQ(System::Text::Encoding::get_UTF8(), txtSaveOptions->get_Encoding());

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

System::String docText = System::Text::Encoding::get_UTF8()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt"));

ASSERT_EQ(u"\ufeffÀ È Ì Ò Ù.\r\n", docText);

// Uygun olmayan bir kodlama kullanmak belge içeriğinin kaybolmasına neden olabilir.
txtSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());
doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System::Text::Encoding::get_ASCII()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt"));

ASSERT_EQ(u"? ? ? ? ?.\r\n", docText);
```

## Ayrıca Bakınız

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
