---
title: "Aspose::Words::Border::get_LineWidth metodu"
linktitle: "get_LineWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_LineWidth metodu. C++'ta kenar genişliğini puan cinsinden alır veya ayarlar."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Kenar genişliğini puan cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Açıklamalar


Çizgi stili none (yok) iken çizgi genişliğini sıfırdan büyük bir değere ayarlarsanız, çizgi stili otomatik olarak tek çizgiye değiştirilecektir.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
