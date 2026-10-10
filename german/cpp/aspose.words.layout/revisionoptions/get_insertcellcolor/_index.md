---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor method"
linktitle: "get_InsertCellColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor method. Ermöglicht die Angabe der Farbe, die für eingefügte Zellen (Insertion) verwendet wird. Der Standardwert ist Blue in C++."
type: docs
weight: 4500
url: /de/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Ermöglicht die Angabe der Farbe, die für eingefügte Zellen [Insertion](../../../aspose.words/revisiontype/) verwendet wird. Der Standardwert ist [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Beispiele



Zeigt, wie man mit Einfügen/Löschen-Zell-Revision-Farbe arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Siehe auch

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
