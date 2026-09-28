---
title: "Класс Aspose::Words::FrameFormat"
linktitle: "FrameFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::FrameFormat. Представляет форматирование, связанное с рамкой, для абзаца в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/frameformat/
---
## FrameFormat class


Представляет форматирование, связанное с рамкой, для абзаца.

```cpp
class FrameFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Height](./get_height/)() | Получает высоту указанного кадра. |
| [get_HeightRule](./get_heightrule/)() | Получает правило определения высоты указанного кадра. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Получает горизонтальное выравнивание указанного кадра. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Получает горизонтальное расстояние между кадром и окружающим текстом в пунктах. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Получает горизонтальное расстояние между краем кадра и элементом, указанным свойством [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | Возвращает **true**, если абзац является кадром. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Получает относительное горизонтальное положение кадра. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Получает относительное вертикальное положение кадра. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Получает вертикальное выравнивание указанного кадра. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Указывает вертикальное расстояние (в пунктах) между кадром и окружающим текстом. |
| [get_VerticalPosition](./get_verticalposition/)() | Получает вертикальное расстояние между краем кадра и элементом, указанным свойством [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | Получает ширину указанного кадра в пунктах. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Этот объект всегда создаётся. Если абзац является кадром, все свойства будут содержать соответствующие значения, в противном случае все свойства устанавливаются в значения по умолчанию.

Используйте [IsFrame](./get_isframe/) для проверки, является ли абзац кадром.

## Примеры



Показывает, как получить информацию о свойствах форматирования абзацев, которые являются кадрами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
