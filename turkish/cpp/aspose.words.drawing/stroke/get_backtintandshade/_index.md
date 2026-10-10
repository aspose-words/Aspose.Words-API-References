---
title: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade yöntemi"
linktitle: "get_BackTintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade yöntemi. C++'da çizgi arka plan rengini aydınlatan veya karartan bir double değer alır veya ayarlar."
type: docs
weight: 2334
url: /tr/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Çizgi arka plan rengini aydınlatan veya karartan bir double değerini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en açık) arasındadır. Sıfır (0) nötrdür. Bu özelliği -1'den daha düşük veya 1'den daha yüksek bir değere ayarlamaya çalışmak [ArgumentOutOfRangeException](../) hatasına neden olur.

## Örnekler



Arka tema rengini ve tonlama ve gölgelendirmeyi nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Ayrıca Bakınız

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
