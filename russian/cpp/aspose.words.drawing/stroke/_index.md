---
title: "Aspose::Words::Drawing::Stroke класс"
linktitle: "Stroke"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Stroke класс. Определяет обводку для фигуры. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.drawing/stroke/
---
## Stroke class


Определяет штрих для фигуры. Чтобы узнать больше, посетите статью документации [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

```cpp
class Stroke : public Aspose::Words::Drawing::Core::IFillable
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Получает или задаёт цвет фона обводки. |
| [get_BackThemeColor](./get_backthemecolor/)() | Получает или задаёт объект ThemeColor, представляющий цвет фона обводки. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Получает или задаёт значение типа double, которое осветляет или затемняет цвет фона обводки. |
| [get_BaseForeColor](./get_baseforecolor/)() | Возвращает базовый цвет переднего плана обводки без каких-либо модификаторов. |
| [get_Color](./get_color/)() | Определяет цвет обводки. |
| [get_Color2](./get_color2/)() | Определяет второй цвет обводки. |
| [get_DashStyle](./get_dashstyle/)() | Указывает шаблон точек и тире для обводки. |
| [get_EndArrowLength](./get_endarrowlength/)() | Определяет длину наконечника стрелки для конца обводки. |
| [get_EndArrowType](./get_endarrowtype/)() | Определяет форму наконечника стрелки для конца штриха. |
| [get_EndArrowWidth](./get_endarrowwidth/)() | Определяет ширину наконечника стрелки для конца штриха. |
| [get_EndCap](./get_endcap/)() | Определяет стиль заглушки для конца штриха. |
| [get_Fill](./get_fill/)() | Получает форматирование заливки для [Stroke](./). |
| [get_ForeColor](./get_forecolor/)() | Получает или задает цвет переднего плана штриха. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Получает или задает объект ThemeColor, представляющий цвет переднего плана штриха. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана штриха. |
| [get_ImageBytes](./get_imagebytes/)() | Определяет изображение для заливки штрихом изображения или узора. |
| [get_JoinStyle](./get_joinstyle/)() | Определяет стиль соединения полилинии. |
| [get_LineStyle](./get_linestyle/)() | Определяет стиль линии штриха. |
| [get_On](./get_on/)() | Определяет, будет ли путь обведён штрихом. |
| [get_Opacity](./get_opacity/)() | Определяет степень прозрачности штриха. Допустимый диапазон от 0 до 1. |
| [get_StartArrowLength](./get_startarrowlength/)() | Определяет длину наконечника стрелки для начала штриха. |
| [get_StartArrowType](./get_startarrowtype/)() | Определяет форму наконечника стрелки для начала штриха. |
| [get_StartArrowWidth](./get_startarrowwidth/)() | Определяет ширину наконечника стрелки для начала штриха. |
| [get_Transparency](./get_transparency/)() | Получает или задает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха. |
| [get_Visible](./get_visible/)() | Получает или задает флаг, указывающий, видим ли штрих. |
| [get_Weight](./get_weight/)() | Определяет толщину кисти, которой обводится путь фигуры, в пунктах. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Stroke::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Drawing::Stroke::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Сеттер для [Aspose::Words::Drawing::Stroke::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Stroke::get_Color](./get_color/). |
| [set_Color2](./set_color2/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Stroke::get_Color2](./get_color2/). |
| [set_DashStyle](./set_dashstyle/)(Aspose::Words::Drawing::DashStyle) | Указывает шаблон точек и тире для обводки. |
| [set_EndArrowLength](./set_endarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Определяет длину наконечника стрелки для конца обводки. |
| [set_EndArrowType](./set_endarrowtype/)(Aspose::Words::Drawing::ArrowType) | Определяет форму наконечника стрелки для конца штриха. |
| [set_EndArrowWidth](./set_endarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Определяет ширину наконечника стрелки для конца штриха. |
| [set_EndCap](./set_endcap/)(Aspose::Words::Drawing::EndCap) | Определяет стиль заглушки для конца штриха. |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Stroke::get_ForeColor](./get_forecolor/). |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Drawing::Stroke::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Сеттер для [Aspose::Words::Drawing::Stroke::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_JoinStyle](./set_joinstyle/)(Aspose::Words::Drawing::JoinStyle) | Сеттер для [Aspose::Words::Drawing::Stroke::get_JoinStyle](./get_joinstyle/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::Drawing::ShapeLineStyle) | Сеттер для [Aspose::Words::Drawing::Stroke::get_LineStyle](./get_linestyle/). |
| [set_On](./set_on/)(bool) | Сеттер для [Aspose::Words::Drawing::Stroke::get_On](./get_on/). |
| [set_Opacity](./set_opacity/)(double) | Определяет степень прозрачности штриха. Допустимый диапазон от 0 до 1. |
| [set_StartArrowLength](./set_startarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Определяет длину наконечника стрелки для начала штриха. |
| [set_StartArrowType](./set_startarrowtype/)(Aspose::Words::Drawing::ArrowType) | Определяет форму наконечника стрелки для начала штриха. |
| [set_StartArrowWidth](./set_startarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Определяет ширину наконечника стрелки для начала штриха. |
| [set_Transparency](./set_transparency/)(double) | Сеттер для [Aspose::Words::Drawing::Stroke::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Сеттер для [Aspose::Words::Drawing::Stroke::get_Visible](./get_visible/). |
| [set_Weight](./set_weight/)(double) | Сеттер для [Aspose::Words::Drawing::Stroke::get_Weight](./get_weight/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [Stroke](../shape/get_stroke/), чтобы получить доступ к свойствам обводки формы. Вы не создаёте экземпляры класса [Stroke](./) напрямую.

## Примеры



Показывает, как изменить свойства обводки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Базовые фигуры, такие как прямоугольник, имеют две видимые части.
// 1 —  Заливка, которая применяется к области внутри контура фигуры:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 —  Обводка, которая отмечает контур фигуры:
// Измените различные свойства обводки этой фигуры.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
