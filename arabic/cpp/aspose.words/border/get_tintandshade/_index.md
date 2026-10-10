---
title: "Aspose::Words::Border::get_TintAndShade method"
linktitle: "get_TintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Border::get_TintAndShade طريقة. يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغميق اللون في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق اللون.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## ملاحظات


القيم المسموح بها في النطاق من -1 (الأكثر ظلامًا) إلى 1 (الأكثر إضاءة) لهذه الخاصية. الصفر (0) محايد.

## أمثلة



يوضح كيفية إدراج فقرة ذات حد علوي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// قم بتعيين ThemeColor فقط عندما يتم تعيين LineWidth أو LineStyle.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## انظر أيضًا

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
