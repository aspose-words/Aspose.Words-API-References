---
title: "Aspose::Words::TextColumnCollection::get_LineBetween method"
linktitle: "get_LineBetween"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextColumnCollection::get_LineBetween method. Когда true, добавляет вертикальную линию между колонками в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


Когда **true**, добавляет вертикальную линию между колонками.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Примеры



Показывает, как разделить колонки вертикальной линией.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Настройте объект PageSetup текущего раздела, чтобы разбить текст на несколько колонок.
// Установите свойство "LineBetween" в "true", чтобы добавить разделительную линию между колонками.
// Установите свойство "LineBetween" в "false", чтобы оставить пространство между колонками пустым.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## См. также

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
