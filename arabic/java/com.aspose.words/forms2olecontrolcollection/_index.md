---
title: "Forms2OleControlCollection"
linktitle: "Forms2OleControlCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من كائنات Forms2OleControl في Java."
type: docs
weight: 350
url: /ar/java/com.aspose.words/forms2olecontrolcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Forms2OleControlCollection implements Iterable
```

يمثل مجموعة من كائنات [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Ole Objects ][Working with Ole Objects].

 **Examples:** 

يعرض كيفية الوصول إلى عنصر تحكم OLE مضمّن في مستند وعناصر التحكم التابعة له.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يحصل على كائن [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) عند فهرس محدد. |
| [getCount()](#getCount) | يحصل على عدد الكائنات في المجموعة. |
| [iterator()](#iterator) | يحصل على المُعدِّد. |
### get(int index) {#get-int}
```
public Forms2OleControl get(int index)
```


يحصل على كائن [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) عند فهرس محدد.

 **Examples:** 

يعرض كيفية الوصول إلى عنصر تحكم OLE مضمّن في مستند وعناصر التحكم التابعة له.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[Forms2OleControl](../../com.aspose.words/forms2olecontrol/) - [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) object at a specified index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد الكائنات في المجموعة.

 **Examples:** 

يعرض كيفية الوصول إلى عنصر تحكم OLE مضمّن في مستند وعناصر التحكم التابعة له.

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
int - عدد الكائنات في المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يحصل على المُعدِّد.

**Returns:**
java.util.Iterator
