---
title: "Aspose::Words::Drawing::Stroke::get_Color2 metodu"
linktitle: "get_Color2"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_Color2 metodu. C++'da bir çizgi için ikinci rengi tanımlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Bir çizgi için ikinci bir renk tanımlar.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Açıklamalar


Bir [Shape](../../shape/) için varsayılan değer **White**'dır.

## Örnekler



Şekil çizgi özelliklerini nasıl işleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Çizgiler iki renk alabilir; bu renkler iki tonlu görüntü verileriyle tanımlanan bir desen oluşturmak için kullanılır.
// Tek renkli çizgiler Color2 özelliğini kullanmaz.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Ayrıca Bakınız

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
