---
title: "Класс Aspose::Words::TextColumn"
linktitle: "TextColumn"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::TextColumn. Представляет одну текстовую колонку. TextColumn является членом коллекции TextColumnCollection. Коллекция TextColumn включает все колонки в разделе документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 70000
url: /ru/cpp/aspose.words/textcolumn/
---
## TextColumn class


Представляет одну текстовую колонку. [TextColumn](./) является членом коллекции [TextColumnCollection](../textcolumncollection/). Коллекция [TextColumn](./) включает все колонки в разделе документа. Чтобы узнать больше, посетите статью документации [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Получает или задает расстояние между этой колонкой и следующей колонкой в пунктах. Не требуется для последней колонки. |
| [get_Width](./get_width/)() | Получает или задает ширину текстовой колонки в пунктах. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Сеттер для [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Сеттер для [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Примечания


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Когда создаётся новый [TextColumn](./), его ширина и интервал устанавливаются в ноль.

## Примеры



Показывает, как создать колонки с неравномерным интервалом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Определите количество места, доступного для размещения колонок.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Установите первую колонку узкой.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Установите вторую колонку так, чтобы она занимала оставшееся доступное пространство в пределах полей страницы.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
