---
title: "طريقة Aspose::Words::FileFormatInfo::get_Encoding"
linktitle: "get_Encoding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatInfo::get_Encoding. تحصل على الترميز المكتشف إذا كان ذلك مناسبًا لتنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط للمستندات HTML في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


يحصل على الترميز المكتشف إذا كان مناسبًا لتنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط للمستندات HTML.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## أمثلة



يوضح كيفية اكتشاف الترميز في ملف html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// يُستخدم خاصية Encoding فقط عندما نقوم بإنشاء كائن FileFormatInfo لمستند html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## انظر أيضًا

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
