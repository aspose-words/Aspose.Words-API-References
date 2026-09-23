---
title: "Frameset"
linktitle: "Frameset"
second_title: "Aspose.Words per Java"
description: "Rappresenta una pagina di frame o un singolo frame su una pagina di frame in Java."
type: docs
weight: 353
url: /it/java/com.aspose.words/frameset/
---

**Inheritance:**
java.lang.Object
```
public class Frameset
```

Rappresenta una pagina di frame o un singolo frame su una pagina di frame.

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Remarks:** 

Se la proprietà [getChildFramesets()](../../com.aspose.words/frameset/\#getChildFramesets) contiene elementi, questa istanza è una pagina di frame, altrimenti è un singolo frame.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getChildFramesets()](#getChildFramesets) | Ottiene la raccolta di frame figli e pagine di frame. |
| [getFrameDefaultUrl()](#getFrameDefaultUrl) | Ottiene l'URL della pagina web o il nome file del documento da visualizzare in questo frame. |
| [isFrameLinkToFile()](#isFrameLinkToFile) | Ottiene un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato. |
| [isFrameLinkToFile(boolean value)](#isFrameLinkToFile-boolean) | Imposta un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato. |
| [setFrameDefaultUrl(String value)](#setFrameDefaultUrl-java.lang.String) | Imposta l'URL della pagina web o il nome file del documento da visualizzare in questo frame. |
### getChildFramesets() {#getChildFramesets}
```
public FramesetCollection getChildFramesets()
```


Ottiene la raccolta di frame figli e pagine di frame.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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


Ottiene l'URL della pagina web o il nome file del documento da visualizzare in questo frame.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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
java.lang.String - L'URL della pagina web o il nome file del documento da visualizzare in questo frame.
### isFrameLinkToFile() {#isFrameLinkToFile}
```
public boolean isFrameLinkToFile()
```


Ottiene un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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
boolean - Un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato.
### isFrameLinkToFile(boolean value) {#isFrameLinkToFile-boolean}
```
public void isFrameLinkToFile(boolean value)
```


Imposta un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore che indica se la pagina web o il nome file del documento specificato nella proprietà [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) è una risorsa esterna a cui il frame è collegato. |

### setFrameDefaultUrl(String value) {#setFrameDefaultUrl-java.lang.String}
```
public void setFrameDefaultUrl(String value)
```


Imposta l'URL della pagina web o il nome file del documento da visualizzare in questo frame.

 **Examples:** 

Mostra come accedere ai frame nella pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | L'URL della pagina web o il nome file del documento da visualizzare in questo frame. |

