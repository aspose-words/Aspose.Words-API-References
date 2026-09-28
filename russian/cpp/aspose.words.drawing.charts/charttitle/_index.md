---
title: "Aspose::Words::Drawing::Charts::ChartTitle класс"
linktitle: "ChartTitle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle класс. Предоставляет доступ к свойствам заголовка диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Предоставляет доступ к свойствам заголовка диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта заголовка диаграммы. |
| [get_Format](./get_format/)() | Предоставляет доступ к форматированию заливки и линий заголовка диаграммы. |
| [get_Orientation](./get_orientation/)() | Возвращает или задаёт ориентацию текста заголовка диаграммы. |
| [get_Overlay](./get_overlay/)() | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. По умолчанию наложение **false**. |
| [get_Rotation](./get_rotation/)() | Возвращает или задаёт вращение заголовка диаграммы в градусах. |
| [get_Show](./get_show/)() | Определяет, будет ли заголовок отображаться для этой диаграммы. Значение по умолчанию **true**. |
| [get_Text](./get_text/)() | Возвращает или задаёт текст заголовка диаграммы. Если указано **null** или пустое значение, будет отображён автоматически сгенерированный заголовок. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Сеттер для [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вставить диаграмму и задать заголовок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму диаграммы с помощью DocumentBuilder и получите её диаграмму.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Используйте свойство "Title", чтобы задать нашей диаграмме заголовок, который отображается в верхнем центре области диаграммы.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Установите свойство "Show" в значение "true", чтобы сделать заголовок видимым.
title->set_Show(true);

// Установите свойство "Overlay" в значение "true" Чтобы дать другим элементам диаграммы больше места, позволяя им перекрывать заголовок
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
