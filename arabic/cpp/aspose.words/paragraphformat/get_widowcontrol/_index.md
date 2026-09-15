---
title: "Aspose::Words::ParagraphFormat::get_WidowControl طريقة"
linktitle: "get_WidowControl"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_WidowControl طريقة. صحيح إذا كانت السطرين الأول والأخير في الفقرة يبقيان على نفس الصفحة مع باقي الفقرة في C++."
type: docs
weight: 41000
url: /ar/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## أمثلة



يعرض كيفية تمكين التحكم في اليتيم/الأرملة للفقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عند كتابة النص الذي لا يتسع في صفحة واحدة، قد تتدفق سطر واحد إلى الصفحة التالية.
// السطر الوحيد الذي ينتهي به الأمر في الصفحة التالية يُسمى "يتيم",
// والسطر السابق حيث انقطع اليتيم يُسمى "أرملة".
// يمكننا إصلاح اليتامى والأرامل عن طريق إعادة ترتيب النص عبر حجم الخط أو التباعد أو هوامش الصفحة.
// إذا أردنا الحفاظ على أبعاد مستندنا، يمكننا ضبط هذه العلامة إلى "true"
// لدفع الأرامل إلى نفس الصفحة مع اليتامى المقابلين لها.
// ترك هذه العلامة كـ "false" سيترك أزواج اليتيم/الأرملة في النص.
// كل فقرة لديها هذا الإعداد المتاح في Microsoft Word عبر الرئيسية -> الفقرة -> إعدادات الفقرة
// (زر في الزاوية السفلية اليمنى من علامة تبويب "Paragraph") -> "التحكم في اليتيم/الأرملة".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// أدرج نصًا ينتج يتيمًا وأرملة.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
