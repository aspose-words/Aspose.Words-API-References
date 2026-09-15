---
title: "Aspose::Words::BuildVersionInfo فئة"
linktitle: "BuildVersionInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BuildVersionInfo فئة. توفر معلومات حول اسم المنتج الحالي وإصداره. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


يوفر معلومات حول اسم المنتج الحالي والإصدار. لمعرفة المزيد، زر مقالة الوثائق [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | يحصل على الاسم الكامل للمنتج. |
| static [get_Version](./get_version/)() | يحصل على إصدار المنتج. |

## أمثلة



يوضح كيفية عرض معلومات حول الإصدار المثبت من Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
