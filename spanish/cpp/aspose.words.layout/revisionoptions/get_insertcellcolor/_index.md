---
title: "Método Aspose::Words::Layout::RevisionOptions::get_InsertCellColor"
linktitle: "get_InsertCellColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Layout::RevisionOptions::get_InsertCellColor. Permite especificar el color que se usará para las celdas insertadas Inserción. El valor predeterminado es Blue en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Permite especificar el color que se usará para las celdas insertadas [Inserción](../../../aspose.words/revisiontype/). El valor predeterminado es [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Ejemplos



Muestra cómo trabajar con el color de revisión de inserción/eliminación de celdas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Ver también

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
