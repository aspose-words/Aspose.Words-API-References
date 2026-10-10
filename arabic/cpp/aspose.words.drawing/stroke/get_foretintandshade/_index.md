---
title: "طريقة Aspose::Words::Drawing::Stroke::get_ForeTintAndShade method"
linktitle: "get_ForeTintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_ForeTintAndShade. يحصل على أو يضبط قيمة مزدوجة تُفتح أو تُغمق لون مقدمة الخط في C++."
type: docs
weight: 10667
url: /ar/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق لون مقدمة الخط.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## ملاحظات


القيم المسموح بها تقع ضمن النطاق من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية. الصفر (0) محايد. محاولة ضبط هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 ينتج عنها [ArgumentOutOfRangeException](../).

## أمثلة



يوضح كيفية ضبط لون السمة الأمامية وتدرج اللون والظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## انظر أيضًا

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
