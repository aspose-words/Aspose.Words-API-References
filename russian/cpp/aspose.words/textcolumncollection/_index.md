---
title: "Aspose::Words::TextColumnCollection класс"
linktitle: "TextColumnCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextColumnCollection класс. Коллекция объектов TextColumn, представляющих все колонки текста в разделе документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 71000
url: /ru/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Коллекция объектов [TextColumn](../textcolumn/), представляющих все колонки текста в разделе документа. Чтобы узнать больше, посетите статью документации [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() | Возвращает количество колонок в разделе документа. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | True, если колонки текста имеют одинаковую ширину и равномерно распределены. |
| [get_LineBetween](./get_linebetween/)() | Когда **true**, добавляет вертикальную линию между колонками. |
| [get_Spacing](./get_spacing/)() | Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах. |
| [get_Width](./get_width/)() | Когда колонки равномерно распределены, получает ширину колонок. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает колонку текста по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Сеттер для [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Сеттер для [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Сеттер для [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Размещает текст в указанном количестве колонок. |
| static [Type](./type/)() |  |
## Примечания


Используйте [SetCount()](./setcount/) для установки количества колонок текста.

Чтобы сделать все колонки одинаковой ширины и равномерно распределенными, установите [EvenlySpaced](./get_evenlyspaced/) в **true** и укажите величину промежутка между колонками в [Spacing](./get_spacing/). MS Word автоматически рассчитает ширину колонок.

Если у вас [EvenlySpaced](./get_evenlyspaced/) установлено в **false**, необходимо указать ширину и промежуток для каждой колонки отдельно. Используйте индексатор для доступа к отдельным объектам [TextColumn](../textcolumn/).

При использовании пользовательских ширин колонок убедитесь, что сумма всех ширин колонок и промежутков между ними равна ширине страницы за вычетом левых и правых полей.

## Примеры



Показывает, как создать несколько равномерно распределенных колонок в разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
