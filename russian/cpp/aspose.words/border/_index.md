---
title: "Aspose::Words::Border класс"
linktitle: "Border"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border класс. Представляет границу объекта. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/border/
---
## Border class


Представляет границу объекта. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает свойства границы к значениям по умолчанию. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Определяет, равна ли указанная граница по значению текущей границе. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_Color](./get_color/)() | Получает или задает цвет границы. |
| [get_DistanceFromText](./get_distancefromtext/)() | Получает или задаёт расстояние границы от текста или от края страницы в пунктах. |
| [get_IsVisible](./get_isvisible/)() | Возвращает **true**, если [LineStyle](./get_linestyle/) не является [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Получает или задает стиль границы. |
| [get_LineWidth](./get_linewidth/)() | Получает или задает ширину границы в пунктах. |
| [get_Shadow](./get_shadow/)() | Получает или задает значение, указывающее, имеет ли граница тень. |
| [get_ThemeColor](./get_themecolor/)() | Получает или задаёт цвет темы в применяемой цветовой схеме, связанной с этим объектом [Border](./). |
| [get_TintAndShade](./get_tintandshade/)() | Получает или задаёт двойное значение, которое осветляет или затемняет цвет. |
| [GetHashCode](./gethashcode/)() const override | Служит хеш-функцией для этого типа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Сеттер для [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Сеттер для [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Сеттер для [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Сеттер для [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Сеттер для [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Примечания


Границы могут применяться к различным элементам документа, включая абзац, последовательность текста внутри абзаца или ячейку таблицы.

## Примеры



Показывает, как вставить строку, окружённую границей, в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
