---
title: "طريقة Aspose::Words::Story::get_LastParagraph"
linktitle: "get_LastParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Story::get_LastParagraph. يحصل على الفقرة الأخيرة في القصة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


يحصل على الفقرة الأخيرة في القصة.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## أمثلة



يوضح كيفية نقل موضع المؤشر الخاص بـ [DocumentBuilder](../../documentbuilder/)'s إلى عقدة محددة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// يمتلك منشئ المستند مؤشرًا، يعمل كجزء من المستند
// حيث يضيف المنشئ عقدًا جديدة عندما نستخدم طرق بناء المستند الخاصة به.
// هذا المؤشر يعمل بنفس طريقة مؤشر مايكروسوفت وورد الوميضي،
// وهو أيضًا **دائمًا** ينتهي **بعد** أي **عقدة** قام المنشئ بإدراجها للتو.
// لإضافة محتوى إلى جزء مختلف من المستند،
// يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// المؤشر الآن أمام العقدة التي نقلناه إليها.
// إضافة تشغيل ثانٍ سيُدرجه أمام التشغيل الأول.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// انقل المؤشر إلى نهاية المستند لمتابعة إضافة النص إلى النهاية كما كان من قبل.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
