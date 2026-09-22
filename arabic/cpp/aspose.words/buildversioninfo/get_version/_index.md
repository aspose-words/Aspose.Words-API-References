---
title: "طريقة Aspose::Words::BuildVersionInfo::get_Version"
linktitle: "get_Version"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BuildVersionInfo::get_Version. يحصل على إصدار المنتج في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


يحصل على إصدار المنتج.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## ملاحظات


إصدار المنتج بتنسيق "Major.Minor.Hotfix.0".

## أمثلة



يوضح كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## انظر أيضًا

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
