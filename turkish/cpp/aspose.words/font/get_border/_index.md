---
title: "Aspose::Words::Font::get_Border yöntemi"
linktitle: "get_Border"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Border yöntemi. C++ içinde font için kenarlığı belirten bir Border nesnesi döndürür."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Font için kenarlığı belirten bir [Border](../../border/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## Örnekler



Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Ayrıca Bakınız

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
