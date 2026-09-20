---
title: "Aspose::Words::Tables::CellFormat class"
linktitle: "CellFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat class. Представляет все форматирование ячейки таблицы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Представляет всё форматирование ячейки таблицы. Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает форматирование ячейки к значениям по умолчанию. Не изменяет ширину ячейки. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ ячейки. |
| [get_BottomPadding](./get_bottompadding/)() | Возвращает или задает количество пространства (в пунктах), добавляемое ниже содержимого ячейки. |
| [get_FitText](./get_fittext/)() | Если **true**, помещает текст в ячейку, сжимая каждый абзац до ширины ячейки. |
| [get_HideMark](./get_hidemark/)() | Возвращает видимость маркера ячейки. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Указывает, как ячейка объединяется горизонтально с другими ячейками в строке. |
| [get_LeftPadding](./get_leftpadding/)() | Возвращает или задает количество пространства (в пунктах), добавляемое слева от содержимого ячейки. |
| [get_Orientation](./get_orientation/)() | Возвращает или задает ориентацию текста в ячейке таблицы. |
| [get_PreferredWidth](./get_preferredwidth/)() | Возвращает или задает предпочтительную ширину ячейки. |
| [get_RightPadding](./get_rightpadding/)() | Возвращает или задает количество пространства (в пунктах), добавляемое справа от содержимого ячейки. |
| [get_Shading](./get_shading/)() | Возвращает объект [Shading](../../aspose.words/shading/), который относится к форматированию затенения ячейки. |
| [get_TopPadding](./get_toppadding/)() | Возвращает или задает количество пространства (в пунктах), добавляемое выше содержимого ячейки. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Возвращает или задает вертикальное выравнивание текста в ячейке. |
| [get_VerticalMerge](./get_verticalmerge/)() | Указывает, как ячейка объединяется с другими ячейками по вертикали. |
| [get_Width](./get_width/)() | Получает ширину ячейки в пунктах. |
| [get_WrapText](./get_wraptext/)() | Если **true**, переносить текст в ячейке. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Сеттер для [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Сеттер для [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Устанавливает видимость метки ячейки. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Сеттер для [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Сеттер для [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Сеттер для [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Сеттер для [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Сеттер для [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Сеттер для [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Сеттер для [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Сеттер для [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Сеттер для [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Сеттер для [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Устанавливает количество пространства (в пунктах), добавляемого слева/сверху/справа/снизу к содержимому ячейки. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как построить таблицу с пользовательскими границами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Установка параметров форматирования таблицы для DocumentBuilder
// будет применять их к каждой строке и ячейке, которые мы добавляем с его помощью.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Изменение форматирования будет применено к текущей ячейке,
// и к любым новым ячейкам, которые мы создаём с помощью билдера позже.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Увеличьте высоту строки, чтобы разместить вертикальный текст.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Показывает, как изменить формат строк и ячеек в таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Используйте свойство "RowFormat" первой строки, чтобы изменить форматирование
// содержимого всех ячеек в этой строке.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Используйте свойство "CellFormat" первой ячейки в последней строке, чтобы изменить форматирование содержимого этой ячейки.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Показывает, как изменить форматирование ячейки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Используйте свойство "CellFormat" ячейки, чтобы задать форматирование, изменяющее внешний вид этой ячейки.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## См. также

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
