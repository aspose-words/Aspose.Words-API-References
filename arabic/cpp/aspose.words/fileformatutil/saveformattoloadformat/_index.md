---
title: "طريقة Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat"
linktitle: "SaveFormatToLoadFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat. يحول قيمة SaveFormat إلى قيمة LoadFormat إذا كان ذلك ممكنًا في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


يحول قيمة [SaveFormat](../../saveformat/) إلى قيمة [LoadFormat](../../loadformat/) إذا كان ذلك ممكنًا.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## أمثلة



يوضح كيفية تحويل تنسيق حفظ إلى تنسيق تحميل المقابل له.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// بعض أنواع الملفات يمكن حفظ المستندات إليها، ولكن لا يمكن تحميلها باستخدام Aspose.Words.
// إذا حاولنا تحويل تنسيق حفظ من هذا النوع إلى تنسيق تحميل، سيتم إلقاء استثناء.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## انظر أيضًا

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
