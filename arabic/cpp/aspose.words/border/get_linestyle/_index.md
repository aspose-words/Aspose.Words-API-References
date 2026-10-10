---
title: "طريقة Aspose::Words::Border::get_LineStyle"
linktitle: "get_LineStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_LineStyle. يسترجع أو يعيّن نمط الحد في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


يحصل أو يضبط نمط الحد.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## ملاحظات


إذا قمت بتعيين نمط الخط إلى لا شيء، فسيتم تغيير عرض الخط تلقائيًا إلى الصفر.

## أمثلة



يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## انظر أيضًا

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
