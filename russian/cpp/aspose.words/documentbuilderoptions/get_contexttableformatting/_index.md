---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting метод"
linktitle: "get_ContextTableFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting метод. True, если форматирование, применённое к содержимому таблицы, не влияет на форматирование последующего содержимого. Значение по умолчанию — true в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Истина, если форматирование, применяемое к содержимому таблицы, не влияет на форматирование последующего содержимого. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


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

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
