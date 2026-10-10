---
title: "Metodo Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor"
linktitle: "get_DeleteCellColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor method. Consente di specificare il colore da utilizzare per le celle eliminate Deletion. Il valore predefinito è Pink in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Consente di specificare il colore da utilizzare per le celle eliminate [Deletion](../../../aspose.words/revisiontype/). Il valore predefinito è [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
