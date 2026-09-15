---
title: "Aspose::Words::BuildVersionInfo::get_Product طريقة"
linktitle: "get_Product"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BuildVersionInfo::get_Product طريقة. يحصل على الاسم الكامل للمنتج في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


يحصل على الاسم الكامل للمنتج.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## أمثلة



يوضح كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## انظر أيضًا

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
