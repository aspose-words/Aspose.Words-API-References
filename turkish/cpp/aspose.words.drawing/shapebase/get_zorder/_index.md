---
title: "Aspose::Words::Drawing::ShapeBase::get_ZOrder metodu"
linktitle: "get_ZOrder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_ZOrder metodu. Üst üste gelen şekillerin görüntüleme sırasını C++'ta belirler."
type: docs
weight: 57000
url: /tr/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Üst üste binen şekillerin görüntüleme sırasını belirler.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Açıklamalar


Yalnızca üst düzey şekiller için etkilidir.

Varsayılan değer 0'dır.

Sayı, yığılma önceliğini temsil eder. Daha yüksek bir sayıya sahip bir şekil, daha düşük sayıya sahip bir şeklin üstünde ("önünde") bulunuyormuş gibi görüntülenir.

Üst üste gelen şekillerin sırası, belgenin başlığındaki ve ana metnindeki şekiller için bağımsızdır.

Bir grup şeklinin içindeki alt şekillerin görüntüleme sırası, grup şekli içindeki sıralarına göre belirlenir.

## Örnekler



Şekillerin sırasını nasıl manipüle edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Birbirlerinin bir kısmını üst üste kaplayan üç farklı renkte dikdörtgen ekleyin.
// Bir şekli başka bir şeklin üzerine eklediğimizde, Aspose.Words yeni şekli eski şeklin üzerine yerleştirir.
// Açık yeşil dikdörtgen, açık mavi dikdörtgenin üzerine binecek ve onu kısmen gizleyecek,
// ve açık mavi dikdörtgen turuncu dikdörtgeni gizleyecek.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// "ZOrder" özelliği, bir şeklin diğer üst üste gelen şekiller arasındaki yığılma önceliğini belirler.
// İki üst üste gelen şeklin farklı "ZOrder" değerleri varsa,
// Microsoft Word, daha yüksek değere sahip şekli daha düşük değere sahip şeklin üzerine yerleştirir.
// "ZOrder" değerlerini ayarlayarak ilk turuncu dikdörtgeni ikinci açık mavi dikdörtgenin üzerine yerleştirin
// ve ikinci açık mavi dikdörtgeni üçüncü açık yeşil dikdörtgenin üzerine yerleştirin.
// Bu, orijinal yığılma sıralarını tersine çevirecektir.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
