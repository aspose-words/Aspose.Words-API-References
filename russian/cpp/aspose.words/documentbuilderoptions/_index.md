---
title: "Класс Aspose::Words::DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::DocumentBuilderOptions. Позволяет задавать дополнительные параметры процесса построения документа в C++."
type: docs
weight: 22500
url: /ru/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Позволяет задавать дополнительные параметры для процесса построения документа.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Истина, если форматирование, применяемое к содержимому таблицы, не влияет на форматирование последующего содержимого. Значение по умолчанию — **true**. |
| [get_DesignMode](./get_designmode/)() const | Соответствует режиму «Design Mode» в Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Сеттер для [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Соответствует режиму «Design Mode» в Microsoft Word. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как игнорировать форматирование таблицы для последующего содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Добавляет содержимое перед таблицей.
// Размер шрифта по умолчанию — 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Изменяет размер шрифта внутри таблицы.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Если ContextTableFormatting равно true, то форматирование таблицы не применяется к последующему содержимому.
// Если ContextTableFormatting равно false, то форматирование таблицы применяется к последующему содержимому.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
