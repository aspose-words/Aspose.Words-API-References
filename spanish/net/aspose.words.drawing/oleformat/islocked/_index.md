---
title: OleFormat.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words para .NET
description: Descubra la propiedad OleFormat IsLocked, controle los vínculos de objetos OLE y mejore la integridad de los datos evitando actualizaciones no deseadas. ¡Obtenga más información ahora!
type: docs
weight: 50
url: /es/net/aspose.words.drawing/oleformat/islocked/
---
## OleFormat.IsLocked property

Especifica si el vínculo al objeto OLE está bloqueado para actualizaciones.

```csharp
public bool IsLocked { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo extraer objetos OLE incrustados en archivos.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

//El objeto OLE en la primera forma es una hoja de cálculo de Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

//Nuestro objeto no se actualiza automáticamente ni está bloqueado para actualizaciones.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Si planeamos guardar el objeto OLE en un archivo en el sistema de archivos local,
//Podemos usar la propiedad "SuggestedExtension" para determinar qué extensión de archivo aplicar al archivo.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

A continuación se muestran dos formas de guardar un objeto OLE en un archivo en el sistema de archivos local.
// 1 - Guárdalo a través de una transmisión:
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
