---
title: "طريقة Aspose::Words::Border::get_Color"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_Color. يسترجع أو يعيّن لون الحدود في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/border/get_color/
---
## Border::get_Color method


يحصل أو يضبط لون الحد.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


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
