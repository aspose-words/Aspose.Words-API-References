---
title: "Método Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor"
linktitle: "get_DeleteCellColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor método. Permite especificar el color que se usará para las celdas eliminadas Deletion. El valor predeterminado es Pink en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Permite especificar el color que se usará para las celdas eliminadas [Deletion](../../../aspose.words/revisiontype/). El valor predeterminado es [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
