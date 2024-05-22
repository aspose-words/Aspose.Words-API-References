---
title: Forms2OleControlCollection
linktitle: Forms2OleControlCollection
second_title: Aspose.Words for Java
description: Represents collection of Forms2OleControl objects in Java.
type: docs
weight: 326
url: /java/com.aspose.words/forms2olecontrolcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Forms2OleControlCollection implements Iterable
```

Represents collection of [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) objects.

To learn more, visit the [ Working with Ole Objects ][Working with Ole Objects] documentation article.

 **Examples:** 

Shows how to access an OLE control embedded in a document and its child controls.

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
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index. |
| [getCount()](#getCount) | Gets count of objects in the collection. |
| [iterator()](#iterator) | Gets enumerator. |
### get(int index) {#get-int}
```
public Forms2OleControl get(int index)
```


Gets [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.

 **Examples:** 

Shows how to access an OLE control embedded in a document and its child controls.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) - [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets count of objects in the collection.

 **Examples:** 

Shows how to access an OLE control embedded in a document and its child controls.

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
int - Count of objects in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gets enumerator.

**Returns:**
java.util.Iterator
