---
title: "Aspose::Words::Border::get_ThemeColor طريقة"
linktitle: "get_ThemeColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Border::get_ThemeColor طريقة. يحصل على أو يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


يحصل على أو يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Border](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
