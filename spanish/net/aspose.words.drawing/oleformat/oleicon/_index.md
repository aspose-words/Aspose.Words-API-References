---
title: OleFormat.OleIcon
second_title: Referencia de API de Aspose.Words para .NET
description: OleFormat propiedad. Obtiene el aspecto de dibujo del objeto OLE. Cuando verdadero  el objeto OLE se muestra como un icono. cuando falso  el objeto OLE se muestra como content.
type: docs
weight: 70
url: /es/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Obtiene el aspecto de dibujo del objeto OLE. Cuando **verdadero** , el objeto OLE se muestra como un icono. cuando **falso** , el objeto OLE se muestra como content.

```csharp
public bool OleIcon { get; }
```

### Observaciones

Aspose.Words no permite establecer esta propiedad para evitar confusiones. Si pudiera cambiar el aspecto de dibujo en Aspose.Words, Microsoft Word seguiría mostrando el objeto OLE en su aspecto de dibujo original hasta que edite o actualice el objeto OLE en Microsoft Word.

### Ejemplos

Muestra cómo insertar objetos OLE vinculados y no vinculados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Incruste un dibujo de Microsoft Visio en el documento como un objeto OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Inserte un enlace al archivo en el sistema de archivos local y muéstrelo como un icono.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// La inserción de objetos OLE crea formas que almacenan estos objetos.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Si una forma contiene un objeto OLE, tendrá una propiedad "OleFormat" válida,
// que podemos usar para verificar algunos aspectos de la forma.
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

// Si el objeto contiene datos OLE, podemos acceder a él usando una secuencia.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Ver también

* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../oleformat/)
* asamblea [Aspose.Words](../../../)


