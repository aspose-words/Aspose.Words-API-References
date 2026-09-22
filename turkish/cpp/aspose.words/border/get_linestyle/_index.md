---
title: "Aspose::Words::Border::get_LineStyle metodu"
linktitle: "get_LineStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_LineStyle metodu. C++'ta kenar stilini alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Kenar stilini alır veya ayarlar.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Açıklamalar


Satır stilini none olarak ayarlarsanız, satır genişliği otomatik olarak sıfıra değiştirilir.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
