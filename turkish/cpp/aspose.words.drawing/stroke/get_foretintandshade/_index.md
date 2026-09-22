---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metodu"
linktitle: "get_ForeTintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metodu. C++'da çizgi ön plan rengini aydınlatan veya karartan bir çift (double) değer alır veya ayarlar."
type: docs
weight: 10667
url: /tr/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Çizgi ön plan rengini açan veya karartan bir double değerini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en açık) arasındadır. Sıfır (0) nötrdür. Bu özelliği -1'den daha düşük veya 1'den daha yüksek bir değere ayarlamaya çalışmak [ArgumentOutOfRangeException](../) hatasına neden olur.

## Örnekler



Ön tema rengini ve tonlama ile gölgelendirmeyi nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Ayrıca Bakınız

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
