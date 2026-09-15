---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade طريقة"
linktitle: "get_BackTintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade طريقة. يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق لون الخلفية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


يحصل أو يعيّن قيمة double التي تُفتح أو تُغيم لون الخلفية.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## ملاحظات


القيم المسموح بها تقع في النطاق من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة



يظهر كيفية تعيين لون السمة للون الشكل في المقدمة/الخلفية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// ملاحظة: لا تستخدم "BackThemeColor" و "BackTintAndShade" لتعبئة الخط.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
