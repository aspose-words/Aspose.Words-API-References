---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop метод"
linktitle: "RemoveTabStop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop метод. Удаляет таб‑стоп из уровня списка в C++."
type: docs
weight: 22500
url: /ru/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Удаляет табуляцию из уровня списка.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Примеры



Показывает, как очистить таб‑стоп уровня списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте список с форматированием по умолчанию
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Получите уровень списка и удалите его таб‑стоп
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## См. также

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
