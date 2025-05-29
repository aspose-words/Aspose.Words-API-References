---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words para .NET
description: Descubra el método OleFormat Save para almacenar eficientemente los datos de objetos incrustados en su flujo de datos. ¡Mejore la gestión de datos fácilmente!
type: docs
weight: 160
url: /es/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

Guarda los datos del objeto incrustado en la secuencia especificada.

```csharp
public void Save(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Dónde guardar los datos del objeto. |

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidOperationException | Se lanza si intenta guardar un objeto vinculado. |

## Observaciones

Es responsabilidad del llamante disponer del flujo.

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

---

## Save(*string*) {#save_1}

Guarda los datos del objeto incrustado en un archivo con el nombre especificado.

```csharp
public void Save(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo para guardar los datos del objeto OLE. |

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidOperationException | Se lanza si intenta guardar un objeto vinculado. |

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
