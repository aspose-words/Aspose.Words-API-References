---
title: "Класс Aspose::Words::Shading"
linktitle: "Shading"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Shading. Содержит атрибуты затенения для объекта. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 60000
url: /ru/cpp/aspose.words/shading/
---
## Shading class


Содержит атрибуты затенения для объекта. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Удаляет затенение из объекта. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Определяет, равен ли указанный [Shading](./) по значению текущему [Shading](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Получает или задаёт цвет, применяемый к фону объекта [Shading](./). |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Получает или задаёт цвет темы фонового узора в применяемой цветовой схеме, связанной с этим объектом [Shading](./). |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Получает или задаёт двойное значение, которое осветляет или затемняет цвет темы фона. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Получает или задает цвет, который применяется к переднему плану объекта [Shading](./). |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Получает или задает цвет темы узора переднего плана в применяемой цветовой схеме, связанной с этим объектом [Shading](./). |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Получает или задает значение типа double, которое осветляет или затемняет цвет темы переднего плана. |
| [get_Texture](./get_texture/)() | Получает или задает текстуру затенения. |
| [GetHashCode](./gethashcode/)() const override | Служит хеш-функцией для этого типа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Сеттер для [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Сеттер для [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Сеттер для [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как применить цвет границы и затенения при построении таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте таблицу и задайте цвет/толщину по умолчанию для её границ.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Создайте строку с двумя ячейками, имеющими разные цвета фона.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Сбросьте форматирование ячейки, чтобы отключить цвета фона
// установите пользовательскую толщину границы для всех новых ячеек, создаваемых построителем,
// затем создайте вторую строку.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


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

## См. также

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
