---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words para .NET
description: Personaliza tu hoja de cálculo con la propiedad InsertCellColor en RevisionOptions. Elige el color que prefieras para las celdas insertadas (el predeterminado es azul).
type: docs
weight: 50
url: /es/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Permite especificar el color que se utilizará para las celdas insertadasInsertion . El valor predeterminado esBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
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
