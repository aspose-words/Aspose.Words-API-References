---
title: "طريقة Aspose::Words::ParagraphFormat::get_Borders"
linktitle: "get_Borders"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_Borders. يحصل على مجموعة الحدود للفقرة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/paragraphformat/get_borders/
---
## ParagraphFormat::get_Borders method


يحصل على مجموعة حدود الفقرة.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::ParagraphFormat::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
