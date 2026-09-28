---
title: "Aspose::Words::Document::get_DefaultTabStop метод"
linktitle: "get_DefaultTabStop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_DefaultTabStop метод. Получает или задает интервал (в пунктах) между стандартными табуляциями в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Получает или задает интервал (в пунктах) между стандартными табуляциями.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
