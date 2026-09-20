---
title: "Класс Aspose::Words::TableStyle"
linktitle: "TableStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::TableStyle. Представляет стиль таблицы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 67000
url: /ru/cpp/aspose.words/tablestyle/
---
## TableStyle class


Представляет стиль таблицы. Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Сравнивает с указанным стилем. Styles Istds сравниваются только для встроенных стилей. Значения по умолчанию стилей не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца сравниваются рекурсивно. |
| [get_Aliases](../style/get_aliases/)() | Получает все псевдонимы этого стиля. Если у стиля нет псевдонимов, возвращается пустой массив строк. |
| [get_Alignment](./get_alignment/)() | Указывает выравнивание для стиля таблицы. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Получает или задает флаг, указывающий, разрешено ли разбивать текст в строке таблицы на разрыв страницы. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Указывает, переопределяется ли этот стиль автоматически на основе соответствующего значения. |
| [get_BaseStyleName](../style/get_basestylename/)() | Получает/устанавливает имя стиля, на котором основан этот стиль. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ ячеек по умолчанию для стиля. |
| [get_BottomPadding](./get_bottompadding/)() | Получает или задает количество пространства (в пунктах), добавляемого под содержимым ячеек таблицы. |
| [get_BuiltIn](../style/get_builtin/)() | True, если этот стиль является одним из встроенных стилей в MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | Получает или задает величину пространства (в пунктах) между ячейками. |
| [get_ColumnStripe](./get_columnstripe/)() | Получает или задает количество столбцов, включаемых в чередование, когда стиль указывает чередование нечётных/чётных столбцов. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Коллекция условных стилей, которые могут быть определены для этого стиля таблицы. |
| [get_Document](../style/get_document/)() | Получает документ‑владельца. |
| [get_Font](../style/get_font/)() | Получает символьное форматирование стиля. |
| [get_IsHeading](../style/get_isheading/)() | True, когда стиль является одним из встроенных стилей Heading. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Указывает, показывается ли этот стиль в быстрой галерее [Style](../style/) в пользовательском интерфейсе MS Word. |
| [get_LeftIndent](./get_leftindent/)() | Получает или задает значение, представляющее левый отступ таблицы. |
| [get_LeftPadding](./get_leftpadding/)() | Получает или задает количество пространства (в пунктах), добавляемого слева от содержимого ячеек таблицы. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Получает/задаёт имя [Style](../style/), связанного с этим. Возвращает пустую строку, если стили не связаны. |
| [get_List](../style/get_list/)() | Получает список, определяющий форматирование этого стиля списка. |
| [get_ListFormat](../style/get_listformat/)() | Обеспечивает доступ к свойствам форматирования списка стиля абзаца. |
| [get_Locked](../style/get_locked/)() const | Указывает, заблокирован ли этот стиль. |
| [get_Name](../style/get_name/)() const | Получает или устанавливает имя стиля. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Получает/устанавливает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного указанным стилем. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Получает форматирование абзаца стиля. |
| [get_Priority](../style/get_priority/)() const | Получает/устанавливает целочисленное значение, представляющее приоритет сортировки стилей в панели задач Styles. |
| [get_RightPadding](./get_rightpadding/)() | Получает или задает количество пространства (в пунктах), добавляемого справа от содержимого ячеек таблицы. |
| [get_RowStripe](./get_rowstripe/)() | Получает или задает количество строк, включаемых в чередование, когда стиль указывает чередование нечётных/чётных строк. |
| [get_SemiHidden](../style/get_semihidden/)() const | Получает/устанавливает, скрывается ли стиль в галерее Стилей и на панели задач Стилей. |
| [get_Shading](./get_shading/)() | Получает объект [Shading](../shading/), который относится к форматированию затенения ячеек таблицы. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [get_Styles](../style/get_styles/)() const | Получает коллекцию стилей, к которым принадлежит этот стиль. |
| [get_TopPadding](./get_toppadding/)() | Получает или задает количество пространства (в пунктах), добавляемого над содержимым ячеек таблицы. |
| [get_Type](../style/get_type/)() const | Получает тип стиля (абзацный или символьный). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Получает/устанавливает, отображается ли используемый в текущем документе стиль в галерее Стилей и на панели задач Стилей. Истина, когда используемый стиль должен отображаться в галерее Стилей. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Указывает вертикальное выравнивание ячеек. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Удаляет указанный стиль из документа. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Сеттер для [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Сеттер для [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Сеттер для [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Сеттер для [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Сеттер для [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Сеттер для [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Сеттер для [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Сеттер для [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Сеттер для [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Сеттер для [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Сеттер для [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Сеттер для [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Сеттер для [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Сеттер для [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Сеттер для [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Сеттер для [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Сеттер для [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как создать пользовательские настройки стиля для таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Установка свойств стиля таблицы может влиять на свойства самой таблицы.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## См. также

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
