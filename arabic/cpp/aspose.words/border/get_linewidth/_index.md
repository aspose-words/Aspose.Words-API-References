---
title: "طريقة Aspose::Words::Border::get_LineWidth"
linktitle: "get_LineWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_LineWidth. يسترجع أو يعيّن عرض الحد بالنقاط في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


يحصل أو يضبط عرض الحد بالنقاط.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## ملاحظات


إذا قمت بتعيين عرض الخط أكبر من الصفر عندما يكون نمط الخط None، يتم تغيير نمط الخط تلقائيًا إلى خط واحد.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
