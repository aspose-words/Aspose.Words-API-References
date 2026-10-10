---
title: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor Methode"
linktitle: "get_DeleteCellColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor Methode. Ermöglicht die Angabe der Farbe, die für gelöschte Zellen Deletion verwendet wird. Standardwert ist Pink in C++."
type: docs
weight: 2500
url: /de/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Ermöglicht die Angabe der Farbe, die für gelöschte Zellen [Deletion](../../../aspose.words/revisiontype/). Standardwert ist [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
