---
title: "Aspose::Words::TextureIndex enum"
linktitle: "TextureIndex"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextureIndex enum. Указывает текстуру затенения в C++."
type: docs
weight: 125000
url: /ru/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Указывает текстуру затенения.

```cpp
enum class TextureIndex
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Texture2Pt5Percent | 35 |  |
| Texture30Percent | 6 |  |
| Texture32Pt5Percent | 42 |  |
| Texture35Percent | 43 |  |
| Текстура37Pt5Процент | 44 |  |
| Текстура40Процент | 7 |  |
| Текстура42Pt5Процент | 45 |  |
| Текстура45Процент | 46 |  |
| Текстура47Pt5Процент | 47 |  |
| Текстура50Процент | 8 |  |
| Текстура52Pt5Процент | 48 |  |
| Текстура55Процент | 49 |  |
| Текстура57Pt5Процент | 50 |  |
| Текстура5Процент | 2 |  |
| Текстура60Процент | 9 |  |
| Текстура62Pt5Процент | 51 |  |
| Текстура65Процент | 52 |  |
| Текстура67Pt5Процент | 53 |  |
| Текстура70Процент | 10 |  |
| Текстура72Pt5Процент | 54 |  |
| Текстура75Процент | 11 |  |
| Текстура77Pt5Процент | 55 |  |
| Текстура7Pt5Процент | 36 |  |
| Текстура80Процент | 12 |  |
| Текстура82Pt5Процент | 56 |  |
| Текстура85Процент | 57 |  |
| Текстура87Pt5Процент | 58 |  |
| Текстура90Процент | 13 |  |
| Текстура92Pt5Процент | 59 |  |
| Texture95Percent | 60 |  |
| Texture97Pt5Percent | 61 |  |
| TextureCross | 24 |  |
| TextureDarkCross | 18 |  |
| TextureDarkDiagonalCross | 19 |  |
| TextureDarkDiagonalDown | 16 |  |
| TextureDarkDiagonalUp | 17 |  |
| TextureDarkHorizontal | 14 |  |
| TextureDarkVertical | 15 |  |
| TextureDiagonalCross | 25 |  |
| TextureDiagonalDown | 22 |  |
| TextureDiagonalUp | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | Указывает, что не должно использоваться никакое узор на текущем затенённом регионе (т.е. узор должен полностью заполняться цветом фона). |


## Примеры



Показывает, как оформить текст границами и затенением.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```


Показывает, как применить контурную границу к таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Выровняйте таблицу по центру страницы.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Очистите любые существующие границы и заливку в таблице.
table->ClearBorders();
table->ClearShading();

// Добавьте зеленые границы к контуру таблицы.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Заполните ячейки светло-зелёным сплошным цветом.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
