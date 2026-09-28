---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. Предоставляет доступ к свойствам заголовка оси. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5750
url: /ru/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Предоставляет доступ к свойствам заголовка оси. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта заголовка оси. |
| [get_Format](./get_format/)() | Предоставляет доступ к заполнению и форматированию линий заголовка оси. |
| [get_Orientation](./get_orientation/)() | Получает или задает ориентацию текста заголовка оси. |
| [get_Overlay](./get_overlay/)() | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. Значение по умолчанию — **false**. |
| [get_Rotation](./get_rotation/)() | Получает или задает поворот заголовка оси в градусах. |
| [get_Show](./get_show/)() | Определяет, будет ли отображаться заголовок оси. Значение по умолчанию — **false**. |
| [get_Text](./get_text/)() | Получает или задает текст заголовка оси. Если указано **null** или пустое значение, будет показан автоматически сгенерированный заголовок. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как установить заголовок оси диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Удалить автоматически сгенерированную серию.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
