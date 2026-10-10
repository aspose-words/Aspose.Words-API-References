---
title: "Forms2OleControlCollection"
linktitle: "Forms2OleControlCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de objetos Forms2OleControl en Java."
type: docs
weight: 350
url: /es/java/com.aspose.words/forms2olecontrolcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Forms2OleControlCollection implements Iterable
```

Representa una colección de objetos [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

Para obtener más información, visite el artículo de documentación [ Working with Ole Objects ][Working with Ole Objects].

 **Examples:** 

Muestra cómo acceder a un control OLE incrustado en un documento y a sus controles secundarios.

```

 Document doc = new Document(getMyDir() + "OLE ActiveX controls.docm");

 // Shapes store and display OLE objects in the document's body.
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("6e182020-f460-11ce-9bcd-00aa00608e01", shape.getOleFormat().getClsid().toString());

 Forms2OleControl oleControl = (Forms2OleControl) shape.getOleFormat().getOleControl();

 // Some OLE controls may contain child controls, such as the one in this document with three options buttons.
 Forms2OleControlCollection oleControlCollection = oleControl.getChildNodes();

 Assert.assertEquals(3, oleControlCollection.getCount());

 Assert.assertEquals("C#", oleControlCollection.get(0).getCaption());
 Assert.assertEquals("1", oleControlCollection.get(0).getValue());

 Assert.assertEquals("Visual Basic", oleControlCollection.get(1).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(1).getValue());

 Assert.assertEquals("Delphi", oleControlCollection.get(2).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(2).getValue());
 
```


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Obtiene el objeto [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) en un índice especificado. |
| [getCount()](#getCount) | Obtiene el recuento de objetos en la colección. |
| [iterator()](#iterator) | Obtiene el enumerador. |
### get(int index) {#get-int}
```
public Forms2OleControl get(int index)
```


Obtiene el objeto [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) en un índice especificado.

 **Examples:** 

Muestra cómo acceder a un control OLE incrustado en un documento y a sus controles secundarios.

```

 Document doc = new Document(getMyDir() + "OLE ActiveX controls.docm");

 // Shapes store and display OLE objects in the document's body.
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("6e182020-f460-11ce-9bcd-00aa00608e01", shape.getOleFormat().getClsid().toString());

 Forms2OleControl oleControl = (Forms2OleControl) shape.getOleFormat().getOleControl();

 // Some OLE controls may contain child controls, such as the one in this document with three options buttons.
 Forms2OleControlCollection oleControlCollection = oleControl.getChildNodes();

 Assert.assertEquals(3, oleControlCollection.getCount());

 Assert.assertEquals("C#", oleControlCollection.get(0).getCaption());
 Assert.assertEquals("1", oleControlCollection.get(0).getValue());

 Assert.assertEquals("Visual Basic", oleControlCollection.get(1).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(1).getValue());

 Assert.assertEquals("Delphi", oleControlCollection.get(2).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(2).getValue());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) - [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el recuento de objetos en la colección.

 **Examples:** 

Muestra cómo acceder a un control OLE incrustado en un documento y a sus controles secundarios.

```

 Document doc = new Document(getMyDir() + "OLE ActiveX controls.docm");

 // Shapes store and display OLE objects in the document's body.
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("6e182020-f460-11ce-9bcd-00aa00608e01", shape.getOleFormat().getClsid().toString());

 Forms2OleControl oleControl = (Forms2OleControl) shape.getOleFormat().getOleControl();

 // Some OLE controls may contain child controls, such as the one in this document with three options buttons.
 Forms2OleControlCollection oleControlCollection = oleControl.getChildNodes();

 Assert.assertEquals(3, oleControlCollection.getCount());

 Assert.assertEquals("C#", oleControlCollection.get(0).getCaption());
 Assert.assertEquals("1", oleControlCollection.get(0).getValue());

 Assert.assertEquals("Visual Basic", oleControlCollection.get(1).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(1).getValue());

 Assert.assertEquals("Delphi", oleControlCollection.get(2).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(2).getValue());
 
```

**Returns:**
int - Recuento de objetos en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Obtiene el enumerador.

**Returns:**
java.util.Iterator
