---
title: "طريقة Aspose::Words::FileFormatInfo::get_HasMacros"
linktitle: "get_HasMacros"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatInfo::get_HasMacros. تُعيد true إذا كان هذا المستند يحتوي على ماكرو VBA في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


يرجع **true** إذا كان هذا المستند يحتوي على ماكرو VBA.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## أمثلة



يظهر كيفية التحقق من وجود ماكرو VBA دون تحميل المستند.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## انظر أيضًا

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
