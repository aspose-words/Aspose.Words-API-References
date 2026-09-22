---
title: "طريقة Aspose::Words::Drawing::Stroke::get_BackTintAndShade"
linktitle: "get_BackTintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_BackTintAndShade. تحصل أو تعيّن قيمة مزدوجة تُفتح أو تُغمق لون خلفية الخط في C++."
type: docs
weight: 2334
url: /ar/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


يحصل أو يعيّن قيمة مزدوجة تُفتح أو تُغميق لون خلفية الحد.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## ملاحظات


القيم المسموح بها تقع ضمن النطاق من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية. الصفر (0) محايد. محاولة ضبط هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 ينتج عنها [ArgumentOutOfRangeException](../).

## أمثلة



يوضح كيفية تعيين لون السمة الخلفية وتدرّج اللون والظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## انظر أيضًا

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
