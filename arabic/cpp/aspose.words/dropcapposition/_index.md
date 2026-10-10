---
title: "Aspose::Words::DropCapPosition عدد"
linktitle: "DropCapPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DropCapPosition عدد. يحدد الموضع لنص الحرف الأول الكبير في C++."
type: docs
weight: 87000
url: /ar/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


يحدد موضع نص الحرف الأول الكبير.

```cpp
enum class DropCapPosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | الفقرة لا تحتوي على حرف أول كبير. |
| عادي | 1 | الحرف الأول الكبير موضعه داخل هامش النص في الفقرة المرجعية. |
| الهامش | 2 | الحرف الأول الكبير موضعه خارج هامش النص في الفقرة المرجعية. |


## أمثلة



يوضح كيفية إنشاء حرف أول كبير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج فقرة واحدة تحتوي على حرف كبير يبدأ به النص في الفقرتين الثانية والثالثة.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// حاليًا، ستظهر الفقرتان الثانية والثالثة تحت الفقرة الأولى.
// يمكننا تحويل الفقرة الأولى إلى حرف أول كبير للفقرتين الأخريين عبر كائن "ParagraphFormat" الخاص بها.
// عيّن خاصية "DropCapPosition" إلى "DropCapPosition.Margin" لوضع الحرف الأول الكبير
// خارج هامش الصفحة الأيسر إذا كان نصنا من اليسار إلى اليمين.
// عيّن خاصية "DropCapPosition" إلى "DropCapPosition.Normal" لوضع الحرف الأول الكبير داخل هوامش الصفحة
// وللف النص المتبقي حوله.
// "DropCapPosition.None" هو الحالة الافتراضية لجميع الفقرات.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
