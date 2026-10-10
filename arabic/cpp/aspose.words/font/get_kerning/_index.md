---
title: "طريقة Aspose::Words::Font::get_Kerning"
linktitle: "get_Kerning"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Kerning. يحصل أو يضبط حجم الخط الذي يبدأ عنده التباعد في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


يحصل على أو يضبط حجم الخط الذي يبدأ عنده التباعد بين الحروف.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## أمثلة



يوضح كيفية تحديد حجم الخط الذي يبدأ عنده التباعد في التأثير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// حدد حجم خط المُنشئ، والحجم الأدنى الذي سيؤثر فيه التباعد.
// حجم الخط ينخفض تحت عتبة التباعد، لذا فإن المقطع أدناه لن يحتوي على التباعد.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// حدد عتبة التباعد بحيث يكون حجم خط المُنشئ الحالي أعلى منها.
// أي نص نضيفه من هذه النقطة سيُطبق عليه التباعد. المسافات بين الأحرف
// ستُضبط، عادةً ما ينتج عنها مقطع نصي أكثر جماليةً قليلاً.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
