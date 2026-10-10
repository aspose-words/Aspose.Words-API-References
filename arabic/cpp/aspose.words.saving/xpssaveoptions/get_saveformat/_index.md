---
title: "Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat طريقة"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat طريقة. يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون Xps فقط في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/xpssaveoptions/get_saveformat/
---
## XpsSaveOptions::get_SaveFormat method


يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون [Xps](../../../aspose.words/saveformat/) فقط.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat() override
```


## أمثلة



يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند XPS المحفوظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج عناوين يمكن أن تُستخدم كمدخلات جدول المحتويات للمستويات 1 و2 ثم 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// سيتضمن مستند XPS الناتج مخططًا، جدول محتويات يسرد العناوين في جسم المستند.
// النقر على إدخال في هذا المخطط سينقلك إلى موقع العنوان المقابل.
// عيّن الخاصية "HeadingsOutlineLevels" إلى "2" لاستبعاد جميع العناوين التي مستوياتها أعلى من 2 من المخطط.
// العناوين الأخيرة التي أدرجناها أعلاه لن تظهر.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
