---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metodu"
linktitle: "SaveFormatToLoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metodu. C++'ta bir SaveFormat değerini mümkünse bir LoadFormat değerine dönüştürür."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Mümkünse bir [SaveFormat](../../saveformat/) değerini bir [LoadFormat](../../loadformat/) değerine dönüştürür.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Örnekler



Bir kaydetme formatını karşılık gelen yükleme formatına nasıl dönüştüreceğinizi gösterir.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Bazı dosya türleri Aspose.Words kullanılarak belge kaydedilebilir, ancak yüklenemez.
// Bu tür bir kaydetme formatını bir yükleme formatına dönüştürmeye çalışırsak, bir istisna fırlatılır.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Ayrıca Bakınız

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
