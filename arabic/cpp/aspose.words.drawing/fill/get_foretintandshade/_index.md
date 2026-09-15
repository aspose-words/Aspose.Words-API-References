---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade method"
linktitle: "get_ForeTintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade method. يحصل على أو يضبط قيمة مزدوجة تُفتح أو تُغميق لون المقدمة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


يحصل أو يعيّن قيمة double التي تُفتح أو تُغيم لون المقدمة.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## ملاحظات


القيم المسموح بها تقع في النطاق من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة



يوضح كيفية إدارة إفتح وإغمق لون خط المقدمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
