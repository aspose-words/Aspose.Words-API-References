---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::PresetTexture enum. Указывает текстуру, используемую для заполнения фигуры в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Указывает текстуру, которая будет использоваться для заполнения фигуры.

```cpp
enum class PresetTexture
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | -1 | Без текстуры. |
| BlueTissuePaper | 1 | Текстура синей бумажной салфетки. |
| Bouquet | 2 | Текстура букета. |
| КоричневыйМрамор | 3 | Текстура коричневого мрамора. |
| Холст | 4 | Текстура холста. |
| Пробка | 5 | Текстура пробки. |
| Джинсовая ткань | 6 | Текстура джинсовой ткани. |
| РыбныйФоссил | 7 | Текстура рыбного окаменелого. |
| Гранит | 8 | Текстура гранита. |
| ЗелёныйМрамор | 9 | Текстура зелёного мрамора. |
| СреднееДерево | 10 | Текстура среднего дерева. |
| ГазетнаяБумага | 11 | Текстура газетной бумаги. |
| Дуб | 12 | Текстура дуба. |
| БумажныйМешок | 13 | Текстура бумажного мешка. |
| Папирус | 14 | Текстура папируса. |
| Пергамент | 15 | Текстура пергамента. |
| PinkTissuePaper | 16 | Текстура розовой бумажной салфетки. |
| PurpleMesh | 17 | Текстура пурпурной сетки. |
| RecycledPaper | 18 | Текстура переработанной бумаги. |
| Песок | 19 | Текстура песка. |
| Канцелярия | 20 | Текстура канцелярии. |
| Грецкий орех | 21 | Текстура грецкого ореха. |
| WaterDroplets | 22 | Текстура водяных капель. |
| WhiteMarble | 23 | Текстура белого мрамора. |
| WovenMat | 24 | Текстура плетеного коврика. |


## Примеры



Показать, как задать форматирование маркера.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Удалить автоматически сгенерированную серию.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Задать форматирование маркера.
series->get_Marker()->set_Size(40);
series->get_Marker()->set_Symbol(Aspose::Words::Drawing::Charts::MarkerSymbol::Square);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_BackColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::WaterDroplets);
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_Visible(false);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::GreenMarble);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Oak);
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_Transparency(0.5);

doc->Save(get_ArtifactsDir() + u"Charts.MarkerFormatting.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
