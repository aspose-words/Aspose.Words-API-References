---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words para .NET
description: Personaliza tu hoja de cálculo con la propiedad DeleteCellColor de RevisionOptions. Define fácilmente un color único para las celdas eliminadas, mejorando la claridad y la organización.
type: docs
weight: 20
url: /es/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Permite especificar el color que se utilizará para las celdas eliminadasDeletion . El valor predeterminado esPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Ejemplos

Muestra cómo trabajar con la función de inserción/eliminación de color de revisión de celda.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Ver también

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
