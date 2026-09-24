---
title: "Forms2OleControlCollection"
linktitle: "Forms2OleControlCollection"
second_title: "Aspose.Words Java için"
description: "Java'da Forms2OleControl nesnelerinin koleksiyonunu temsil eder."
type: docs
weight: 350
url: /tr/java/com.aspose.words/forms2olecontrolcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Forms2OleControlCollection implements Iterable
```

[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) nesnelerinin koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için, [ Working with Ole Objects ][Working with Ole Objects] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgede gömülü OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen bir dizinde [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) nesnesini alır. |
| [getCount()](#getCount) | Koleksiyondaki nesnelerin sayısını alır. |
| [iterator()](#iterator) | Yineleyiciyi alır. |
### get(int index) {#get-int}
```
public Forms2OleControl get(int index)
```


Belirtilen bir dizinde [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) nesnesini alır.

 **Examples:** 

Bir belgede gömülü OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) - [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki nesnelerin sayısını alır.

 **Examples:** 

Bir belgede gömülü OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

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
int - Koleksiyondaki nesnelerin sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Yineleyiciyi alır.

**Returns:**
java.util.Iterator
