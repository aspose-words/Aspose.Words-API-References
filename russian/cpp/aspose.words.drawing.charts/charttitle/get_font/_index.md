---
title: "Метод Aspose::Words::Drawing::Charts::ChartTitle::get_Font method"
linktitle: "get_Font"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartTitle::get_Font. Предоставляет доступ к форматированию шрифта заголовка диаграммы в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.drawing.charts/charttitle/get_font/
---
## ChartTitle::get_Font method


Предоставляет доступ к форматированию шрифта заголовка диаграммы.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartTitle::get_Font()
```


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

* Class [Font](../../../aspose.words/font/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
