---
title: "метод Aspose::Words::Drawing::Stroke::get_Color2"
linktitle: "get_Color2"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Stroke::get_Color2. Определяет второй цвет для штриха в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Определяет второй цвет обводки.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Примечания


Значение по умолчанию для [Shape](../../shape/) — **White**.

## Примеры



Показывает, как обрабатывать свойства штриха формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Штрихи могут иметь два цвета, которые используются для создания узора, определяемого двухтонными данными изображения.
// Штрихи с одним цветом не используют свойство Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## См. также

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
