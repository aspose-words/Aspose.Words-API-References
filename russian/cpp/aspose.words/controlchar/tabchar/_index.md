---
title: "Aspose::Words::ControlChar::TabChar поле"
linktitle: "TabChar"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ControlChar::TabChar поле. Символ табуляции: (char)9 или \"\\t\" в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Символ табуляции: (char)9 или "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
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
