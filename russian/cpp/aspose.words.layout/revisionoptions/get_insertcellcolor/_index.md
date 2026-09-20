---
title: "Метод Aspose::Words::Layout::RevisionOptions::get_InsertCellColor"
linktitle: "get_InsertCellColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Layout::RevisionOptions::get_InsertCellColor. Позволяет указать цвет, используемый для вставленных ячеек при вставке. Значение по умолчанию — Blue в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Позволяет указать цвет, используемый для вставленных ячеек [Insertion](../../../aspose.words/revisiontype/). Значение по умолчанию — [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Примеры



Показывает, как работать с цветом ревизии вставки/удаления ячеек.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## См. также

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
