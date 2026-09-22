---
title: "Aspose::Words::FileFormatInfo::get_HasMacros yöntemi"
linktitle: "get_HasMacros"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatInfo::get_HasMacros yöntemi. C++'ta bu belgenin bir VBA makrosu içeriyorsa true döndürür."
type: docs
weight: 3500
url: /tr/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


**true** döndürür eğer bu belge bir VBA makrosu içeriyorsa.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Örnekler



Belgeyi yüklemeden VBA makrosu varlığını nasıl kontrol edeceğini gösterir.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Ayrıca Bakınız

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
