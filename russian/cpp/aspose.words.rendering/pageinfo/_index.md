---
title: "Aspose::Words::Rendering::PageInfo класс"
linktitle: "PageInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::PageInfo класс. Представляет информацию о конкретной странице документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Представляет информацию о конкретной странице документа. Чтобы узнать больше, посетите статью документации [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Colored](./get_colored/)() | Возвращает **true**, если страница содержит цветное содержимое. |
| [get_HeightInPoints](./get_heightinpoints/)() | Получает высоту страницы в пунктах. |
| [get_Landscape](./get_landscape/)() const | Возвращает **true**, если ориентация страницы, указанная в документе для этой страницы, альбомная. |
| [get_PaperSize](./get_papersize/)() | Получает размер бумаги как перечисление. |
| [get_PaperTray](./get_papertray/)() const | Получает лоток бумаги (bin) для этой страницы, указанный в документе. Значение зависит от реализации (принтера). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Получает размер страницы в пунктах. |
| [get_WidthInPoints](./get_widthinpoints/)() | Получает ширину страницы в пунктах. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Ширина и высота страницы, возвращаемые этим объектом, представляют \"финальный\" размер страницы, т.е. они уже повернуты в правильную ориентацию.

## См. также

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
