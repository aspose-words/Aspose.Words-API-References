---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: Aspose.Words para .NET
description: Descubra la propiedad OleFormat SourceItem, identifique y administre fácilmente partes vinculadas de su archivo fuente con esta funcionalidad de cadena esencial.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

Obtiene o establece una cadena que se utiliza para identificar la parte del archivo de origen que se está vinculando.

```csharp
public string SourceItem { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

Por ejemplo, si el archivo de origen es un libro de Microsoft Excel, el`SourceItem` La propiedad podría devolver "Workbook1!R3C1:R4C2" si el objeto OLE contiene solo unas pocas celdas de la hoja de cálculo.

## Ejemplos

Muestra cómo insertar objetos OLE vinculados y no vinculados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Incruste un dibujo de Microsoft Visio en el documento como un objeto OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Inserta un enlace al archivo en el sistema de archivos local y lo muestra como un ícono.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Al insertar objetos OLE se crean formas que almacenan estos objetos.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Si una forma contiene un objeto OLE, tendrá una propiedad "OleFormat" válida,
// que podemos utilizar para verificar algunos aspectos de la forma.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Si el objeto contiene datos OLE, podemos acceder a él mediante un flujo de datos.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Ver también

* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
