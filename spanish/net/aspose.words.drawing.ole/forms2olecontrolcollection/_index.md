---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Ole.Forms2OleControlCollection, su solución para administrar objetos Forms2OleControl de manera eficiente en el procesamiento de documentos.
type: docs
weight: 1470
url: /es/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Representa la colección de[`Forms2OleControl`](../forms2olecontrol/) objetos.

Para obtener más información, visite el[Trabajar con objetos Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) Artículo de documentación.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Obtiene el recuento de objetos en la colección. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Obtiene[`Forms2OleControl`](../forms2olecontrol/) objeto en un índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Obtiene el enumerador. |

## Ejemplos

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

* class [Forms2OleControl](../forms2olecontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
