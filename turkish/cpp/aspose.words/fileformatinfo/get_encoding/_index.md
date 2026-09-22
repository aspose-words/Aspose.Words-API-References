---
title: "Aspose::Words::FileFormatInfo::get_Encoding yöntemi"
linktitle: "get_Encoding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo::get_Encoding yöntemi. Mevcut belge formatına uygulanabiliyorsa tespit edilen kodlamayı alır. Şu anda yalnızca C++'ta HTML belgeleri için kodlamayı tespit eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Mevcut belge formatına uygulanabiliyorsa algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


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

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
