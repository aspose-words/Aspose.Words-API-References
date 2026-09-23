---
title: "Forms2OleControlCollection"
linktitle: "Forms2OleControlCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Forms2OleControl-Objekten in Java dar."
type: docs
weight: 350
url: /de/java/com.aspose.words/forms2olecontrolcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Forms2OleControlCollection implements Iterable
```

Stellt eine Sammlung von [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) Objekten dar.

Um mehr zu erfahren, besuchen Sie den [ Working with Ole Objects ][Working with Ole Objects] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man auf ein in einem Dokument eingebettetes OLE-Steuerelement und dessen untergeordnete Steuerelemente zugreift.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Liefert das [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) Objekt an einem angegebenen Index. |
| [getCount()](#getCount) | Liefert die Anzahl der Objekte in der Sammlung. |
| [iterator()](#iterator) | Liefert einen Enumerator. |
### get(int index) {#get-int}
```
public Forms2OleControl get(int index)
```


Liefert das [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) Objekt an einem angegebenen Index.

 **Examples:** 

Zeigt, wie man auf ein in einem Dokument eingebettetes OLE-Steuerelement und dessen untergeordnete Steuerelemente zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) - [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.
### getCount() {#getCount}
```
public int getCount()
```


Liefert die Anzahl der Objekte in der Sammlung.

 **Examples:** 

Zeigt, wie man auf ein in einem Dokument eingebettetes OLE-Steuerelement und dessen untergeordnete Steuerelemente zugreift.

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
int – Anzahl der Objekte in der Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Liefert einen Enumerator.

**Returns:**
java.util.Iterator
