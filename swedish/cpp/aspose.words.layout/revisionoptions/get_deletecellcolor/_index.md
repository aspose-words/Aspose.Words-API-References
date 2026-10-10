---
title: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor metod"
linktitle: "get_DeleteCellColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor metod. Tillåter att ange färgen som ska användas för borttagna celler Deletion. Standardvärdet är Pink i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Tillåter att ange färgen som ska användas för borttagna celler [Deletion](../../../aspose.words/revisiontype/). Standardvärdet är [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
```


## Exempel



Visar hur man arbetar med färg för infogning/borttagning av cellrevision.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Se även

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
