---
title: "Aspose::Words::ParagraphFormat::get_LineSpacing طريقة"
linktitle: "get_LineSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacing طريقة. يحصل أو يضبط تباعد السطر (بالنقاط) للفقرة في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


يحصل أو يضبط تباعد السطر (بالنقاط) للفقرة.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## ملاحظات


عند ضبط خاصية [LineSpacingRule](../get_linespacingrule/) إلى [AtLeast](../../linespacingrule/)، يمكن أن يكون تباعد السطر أكبر من أو يساوي، ولكن لا يكون أبداً أقل من القيمة المحددة لـ [LineSpacing](./).

عند ضبط خاصية [LineSpacingRule](../get_linespacingrule/) إلى [Exactly](../../linespacingrule/)، لا يتغير تباعد السطر أبداً عن القيمة المحددة لـ [LineSpacing](./)، حتى إذا تم استخدام خط أكبر داخل الفقرة.

## أمثلة



يظهر كيفية العمل مع تباعد الأسطر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي ثلاث قواعد لتباعد الأسطر يمكننا تعريفها باستخدام
// خاصية الفقرة "LineSpacingRule" لتكوين التباعد بين الفقرات.
// 1 -  تعيين الحد الأدنى من التباعد.
// سيؤدي هذا إلى إضافة حشو عمودي لأسطر النص بأي حجم
// التي تكون صغيرة جداً للحفاظ على الحد الأدنى لارتفاع السطر.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  ضبط التباعد الدقيق.
// استخدام أحجام الخط الكبيرة جدًا بالنسبة للتباعد سيؤدي إلى قطع النص.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  ضبط التباعد كمتعدد من التباعد الافتراضي للسطر، والذي يكون 12 نقطة بشكل افتراضي.
// هذا النوع من التباعد سيتكيف مع أحجام الخط المختلفة.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
