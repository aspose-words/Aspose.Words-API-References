---
title: Forms2OleControlCollection.Count
second_title: Referencia de API de Aspose.Words para .NET
description: Forms2OleControlCollection propiedad. Obtiene el recuento de objetos de la colección.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

Obtiene el recuento de objetos de la colección.

```csharp
public int Count { get; }
```

### Ejemplos

Muestra cómo acceder a un control OLE incrustado en un documento y sus controles secundarios.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Las formas almacenan y muestran objetos OLE en el cuerpo del documento.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Algunos controles OLE pueden contener controles secundarios, como el de este documento con tres botones de opciones.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Ver también

* class [Forms2OleControlCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../forms2olecontrolcollection/)
* asamblea [Aspose.Words](../../../)


