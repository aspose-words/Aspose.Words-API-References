---
title: "Aspose::Words::ControlChar::Tab метод"
linktitle: "Таб"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ControlChar::Tab метод. Символ табуляции: \"\\x0009\" или \"\\t\" в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/controlchar/tab/
---
## ControlChar::Tab method


Символ табуляции: "\x0009" или "\t".

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
```


## Примеры



Показывает, как задать пользовательский интервал для позиций табуляций.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите табуляции каждые 72 пункта (1 дюйм).
builder->get_Document()->set_DefaultTabStop(72);

// Каждый символ табуляции перемещает последующий текст к ближайшей позиции табуляции.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## См. также

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
