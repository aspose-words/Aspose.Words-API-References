---
title: "FramesetCollection"
linktitle: "FramesetCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de instancias de la clase Frameset en Java."
type: docs
weight: 354
url: /es/java/com.aspose.words/framesetcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FramesetCollection implements Iterable
```

Representa una colección de instancias de la clase [Frameset](../../com.aspose.words/frameset/).

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Muestra cómo acceder a los marcos en la página.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Obtiene un frame o página de frames en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de frames o páginas de frames contenidos en la colección. |
| [iterator()](#iterator) | Devuelve un enumerador que recorre la colección. |
### get(int index) {#get-int}
```
public Frameset get(int index)
```


Obtiene un frame o página de frames en el índice especificado.

 **Examples:** 

Muestra cómo acceder a los marcos en la página.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[Frameset](../../com.aspose.words/frameset/) - A frame or frames page at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de frames o páginas de frames contenidos en la colección.

 **Examples:** 

Muestra cómo acceder a los marcos en la página.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Returns:**
int - El número de frames o páginas de frames contenidos en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un enumerador que recorre la colección.

**Returns:**
java.util.Iterator
