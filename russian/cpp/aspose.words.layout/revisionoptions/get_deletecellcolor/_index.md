---
title: "Метод Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor"
linktitle: "get_DeleteCellColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor метод. Позволяет указать цвет, используемый для удалённых ячеек Deletion. Значение по умолчанию — Pink в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Позволяет указать цвет, используемый для удалённых ячеек [Deletion](../../../aspose.words/revisiontype/). Значение по умолчанию — [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
