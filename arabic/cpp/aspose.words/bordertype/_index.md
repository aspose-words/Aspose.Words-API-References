---
title: "Aspose::Words::BorderType enum"
linktitle: "BorderType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::BorderType. يحدد جوانب الحد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 81000
url: /ar/cpp/aspose.words/bordertype/
---
## BorderType enum


يحدد جوانب الحد. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | -1 | القيمة الافتراضية. |
| أسفل | 0 | يحدد الحد السفلي لفقرة أو خلية جدول. |
| يسار | 1 | يحدد الحد الأيسر لفقرة أو خلية جدول. |
| يمين | 2 | يحدد الحد الأيمن لفقرة أو خلية جدول. |
| أعلى | 3 | يحدد الحد العلوي لفقرة أو خلية جدول. |
| أفقي | 4 | يحدد الحد الأفقي بين الخلايا في جدول أو بين الفقرات المتطابقة. |
| عمودي | 5 | يحدد الحد العمودي بين الخلايا في جدول. |
| DiagonalDown | 6 | يحدد الحد القطري في خلية جدول. |
| DiagonalUp | 7 | يحدد الحد القطري في خلية جدول. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
