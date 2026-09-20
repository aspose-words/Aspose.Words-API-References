---
title: "Класс Aspose::Words::BorderCollection"
linktitle: "BorderCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::BorderCollection. Коллекция объектов Border. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Коллекция объектов [Border](../border/). Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Удаляет все границы объекта. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Сравнивает коллекции границ. |
| [get_Bottom](./get_bottom/)() | Получает нижнюю границу. |
| [get_Color](./get_color/)() | Получает или задает цвет границы. |
| [get_Count](./get_count/)() | Получает количество границ в коллекции. |
| [get_DistanceFromText](./get_distancefromtext/)() | Получает или задает расстояние границы от текста в пунктах. |
| [get_Horizontal](./get_horizontal/)() | Получает горизонтальную границу, используемую между ячейками или соответствующими абзацами. |
| [get_Left](./get_left/)() | Получает левую границу. |
| [get_LineStyle](./get_linestyle/)() | Получает или задает стиль границы. |
| [get_LineWidth](./get_linewidth/)() | Получает или задает ширину границы в пунктах. |
| [get_Right](./get_right/)() | Получает правую границу. |
| [get_Shadow](./get_shadow/)() | Получает или задает значение, указывающее, имеет ли граница тень. |
| [get_Top](./get_top/)() | Получает верхнюю границу. |
| [get_Vertical](./get_vertical/)() | Получает вертикальную границу, используемую между ячейками. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех границ в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Получает объект [Border](../border/) по типу границы. |
| [idx_get](./idx_get/)(int32_t) | Получает объект [Border](../border/) по индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Сеттер для [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Сеттер для [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Сеттер для [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Сеттер для [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вставить абзац с верхней границей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Устанавливайте ThemeColor только когда заданы LineWidth или LineStyle.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
