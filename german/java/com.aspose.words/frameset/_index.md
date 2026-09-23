---
title: "Frameset"
linktitle: "Frameset"
second_title: "Aspose.Words für Java"
description: "Stellt eine Frames‑Seite oder einen einzelnen Frame auf einer Frames‑Seite in Java dar."
type: docs
weight: 353
url: /de/java/com.aspose.words/frameset/
---

**Inheritance:**
java.lang.Object
```
public class Frameset
```

Stellt eine Frames-Seite oder einen einzelnen Frame auf einer Frames-Seite dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Wenn die Eigenschaft [getChildFramesets()](../../com.aspose.words/frameset/\#getChildFramesets) Elemente enthält, ist diese Instanz eine Frames‑Seite, andernfalls ein einzelner Frame.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getChildFramesets()](#getChildFramesets) | Ruft die Sammlung von untergeordneten Frames und Frames‑Seiten ab. |
| [getFrameDefaultUrl()](#getFrameDefaultUrl) | Ruft die URL der Webseite oder den Dateinamen des Dokuments ab, das in diesem Frame angezeigt werden soll. |
| [isFrameLinkToFile()](#isFrameLinkToFile) | Ruft einen Wert ab, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist. |
| [isFrameLinkToFile(boolean value)](#isFrameLinkToFile-boolean) | Setzt einen Wert, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist. |
| [setFrameDefaultUrl(String value)](#setFrameDefaultUrl-java.lang.String) | Setzt die URL der Webseite oder den Dateinamen des Dokuments, das in diesem Frame angezeigt werden soll. |
### getChildFramesets() {#getChildFramesets}
```
public FramesetCollection getChildFramesets()
```


Ruft die Sammlung von untergeordneten Frames und Frames‑Seiten ab.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
[FramesetCollection](../../com.aspose.words/framesetcollection/) - The collection of child frames and frames pages.
### getFrameDefaultUrl() {#getFrameDefaultUrl}
```
public String getFrameDefaultUrl()
```


Ruft die URL der Webseite oder den Dateinamen des Dokuments ab, das in diesem Frame angezeigt werden soll.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
java.lang.String - Die URL der Webseite oder der Dateiname des Dokuments, das in diesem Frame angezeigt werden soll.
### isFrameLinkToFile() {#isFrameLinkToFile}
```
public boolean isFrameLinkToFile()
```


Ruft einen Wert ab, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
boolean - Ein Wert, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist.
### isFrameLinkToFile(boolean value) {#isFrameLinkToFile-boolean}
```
public void isFrameLinkToFile(boolean value)
```


Setzt einen Wert, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein Wert, der angibt, ob die in der Eigenschaft [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) angegebene Web‑Seiten‑URL oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist. |

### setFrameDefaultUrl(String value) {#setFrameDefaultUrl-java.lang.String}
```
public void setFrameDefaultUrl(String value)
```


Setzt die URL der Webseite oder den Dateinamen des Dokuments, das in diesem Frame angezeigt werden soll.

 **Examples:** 

Zeigt, wie man Frames auf der Seite zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die URL der Webseite oder der Dateiname des Dokuments, das in diesem Frame angezeigt werden soll. |

