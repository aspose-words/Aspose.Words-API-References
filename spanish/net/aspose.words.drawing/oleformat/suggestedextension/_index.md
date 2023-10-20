---
title: OleFormat.SuggestedExtension
linktitle: SuggestedExtension
articleTitle: SuggestedExtension
second_title: Aspose.Words para .NET
description: OleFormat SuggestedExtension propiedad. Obtiene la extensión de archivo sugerida para el objeto incrustado actual si desea guardarlo en un archivo en C#.
type: docs
weight: 120
url: /es/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Obtiene la extensión de archivo sugerida para el objeto incrustado actual si desea guardarlo en un archivo.

```csharp
public string SuggestedExtension { get; }
```

## Ejemplos

Muestra cómo extraer objetos OLE incrustados en archivos.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// El objeto OLE de la primera forma es una hoja de cálculo de Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Nuestro objeto no se actualiza automáticamente ni está bloqueado para recibir actualizaciones.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Si planeamos guardar el objeto OLE en un archivo en el sistema de archivos local,
// podemos usar la propiedad "SuggestedExtension" para determinar qué extensión de archivo aplicar al archivo.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// A continuación se muestran dos formas de guardar un objeto OLE en un archivo en el sistema de archivos local.
// 1 - Guárdalo a través de una secuencia:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Guárdalo directamente en un nombre de archivo:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Ver también

* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
