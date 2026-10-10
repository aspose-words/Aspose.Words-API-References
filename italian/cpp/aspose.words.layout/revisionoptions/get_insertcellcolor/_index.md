---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor metodo"
linktitle: "get_InsertCellColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor metodo. Consente di specificare il colore da utilizzare per le celle inserite Insertion. Il valore predefinito è Blue in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Consente di specificare il colore da utilizzare per le celle inserite [Insertion](../../../aspose.words/revisiontype/). Il valore predefinito è [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Esempi



Mostra come lavorare con il colore di revisione delle celle inserite/eliminate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Vedi anche

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
