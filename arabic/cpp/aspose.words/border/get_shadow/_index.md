---
title: "طريقة Aspose::Words::Border::get_Shadow"
linktitle: "get_Shadow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_Shadow. يسترجع أو يعيّن قيمة تشير إلى ما إذا كان الحد يحتوي على ظل في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


يحصل أو يضبط قيمة تشير إلى ما إذا كان للحد ظل.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## ملاحظات


في Microsoft Word، لكي يكون للحد ظل، يجب أن تكون الحدود على جميع الجوانب الأربعة (اليسار، الأعلى، اليمين والأسفل) من نفس النوع والعرض واللون ويجب أن تكون خاصية Shadow مضبوطة على **true**.

## أمثلة



يظهر كيفية إنشاء حد صفحة متموج أخضر مع ظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## انظر أيضًا

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
