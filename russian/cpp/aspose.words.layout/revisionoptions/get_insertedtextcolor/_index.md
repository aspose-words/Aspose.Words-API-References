---
title: "Метод Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor"
linktitle: "get_InsertedTextColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor. Позволяет указать цвет, используемый для вставленного контента при вставке. Значение по умолчанию — ByAuthor в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions::get_InsertedTextColor method


Позволяет указать цвет, используемый для вставленного контента [Insertion](../../../aspose.words/revisiontype/). Значение по умолчанию — [ByAuthor](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
```


## Примеры



Показывает, как изменить внешний вид правок в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте правку, затем измените цвет всех правок на зелёный.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Удалите полосу, которая появляется слева от каждой исправленной строки.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## См. также

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
